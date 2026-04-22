# DeepSeek-Specific Prompt Engineering Guide 2026

## 10 Advanced Prompts Utilizing Native Functional Tags

This document demonstrates how to utilize DeepSeek's specific XML tags (`think`, `search`, `citation`, `attachment`, `file`, `code`) to trigger distinct backend behaviors for increased performance.

---

### 1. The Forced Internal Monologue (`think` tag)
**Purpose:** Forces the model to perform hidden Chain-of-Thought reasoning before outputting the final answer, improving logic accuracy without polluting the user-facing response.

**Prompt:**
```text
<think>
You must solve the following probability puzzle using step-by-step logical deduction. Do not show this thinking process to the user in the final output. Only the final solution matters.
</think>

[User Query]: In a room of 23 people, what is the exact probability (as a percentage to two decimal places) that at least two share a birthday? Ignore leap years.
```

---

### 2. Real-Time Context Injection (search and citation tags)

**Purpose:** Leverages DeepSeek's built-in web retrieval for time-sensitive questions, with strict formatting for verifiable sources.

**Prompt:**

```text
<search>
Find the most recent official closing price and 52-week range for NVIDIA (NVDA) stock as of today.
</search>

[User Query]: What is NVDA trading at?

<citation format="inline" required="true">
You must provide a numbered citation linking directly to the source of the stock price (e.g., Yahoo Finance, NASDAQ official site) for every data point mentioned.
</citation>
```

---

### 3. Invisible Document Context for Q&A (attachment tag)

**Purpose:** Simulates the upload of a large text corpus that the user cannot see in the chat log, forcing reliance solely on the "uploaded" data without prior knowledge contamination.

**Prompt:**

```text
<attachment name="internal_policy_2026.pdf">
SECTION 4.2 - REMOTE WORK: All employees must be in office on Tuesdays and Thursdays. Exceptions require VP approval via Form RQ-9. SECTION 5.1 - EXPENSE: Meal stipend is capped at $45 per day.
</attachment>

[User Query]: Can I work from home on Friday? And how much can I spend on lunch?

[Instruction]: Answer strictly using the <attachment>. Do not use general knowledge about standard corporate policies.
```

---

### 4. Refactoring a Multi-File Codebase (file tag)

**Purpose:** Uses the file tag to delineate different modules within a single prompt window, enabling cross-file dependency analysis without actually uploading files.

**Prompt:**

```text
<file path="src/utils/math_helpers.py">
def multiply(a, b):
    return a * b

def add(a, b):
    return a + b
</file>

<file path="src/main.py">
from utils.math_helpers import multiply

def calculate_volume(l, w, h):
    # BUG: This uses multiply incorrectly for volume calculation
    return multiply(l, w) * h 
</file>

[User Query]: The `calculate_volume` function is producing a type error when `h` is an integer and `l,w` are floats. But more importantly, the logic is brittle. Refactor `main.py` to use a direct multiplication operator for clarity and ensure the import structure remains intact.
```

---

### 5. Forced Syntax Highlighting for Technical Specs (code tag)

**Purpose:** Uses the code tag with language specification to ensure output is strictly formatted as a consumable data structure (JSON) without any conversational filler text.

**Prompt:**

```text
<code language="json" output-only="true">
Generate a JSON schema for a "Smart Home Device" object. It must include: deviceId (string), firmwareVersion (semver string), sensors (array of objects with type and unit), and a boolean for online status.
</code>

[User Query]: I need the schema for my API docs. No explanations, just the JSON block.
```

---

### 6. Comparative Reasoning with Forced Uncertainty (think and search)

**Purpose:** Combines internal reasoning with external data to navigate conflicting information.

**Prompt:**

```text
<think>
Weigh the reliability of historical scientific consensus vs. recent 2025-2026 study data. Prioritize recent <search> results if they contradict older knowledge.
</think>

<search query="latest studies on daily aspirin use for primary prevention 2025 2026">
</search>

[User Query]: Is taking a baby aspirin daily still recommended for healthy 60-year-olds to prevent a first heart attack?

<citation>
Cite specific medical journals or guidelines (e.g., AHA, USPSTF) from the search results.
</citation>
```

---

### 7. The "Strict Guardrails" Prompt (file and think)

**Purpose:** Uses a file tag to load a system prompt/ruleset that the model must follow explicitly, mimicking a custom GPT configuration.

**Prompt:**

```text
<file path="system_instruction.txt">
MODE: BULLET-POINT ONLY.
RULE 1: Never use the word "the".
RULE 2: Format all responses as unordered lists.
RULE 3: If a question requires a paragraph, respond with "INVALID QUERY".
</file>

<think>
Audit the user query against RULE 1 in system_instruction.txt before generating response.
</think>

[User Query]: Explain the theory of relativity to me.
```

---

### 8. Data Extraction from Unstructured Log (attachment and code)

**Purpose:** Simulates parsing a messy log file into a structured Python dictionary.

**Prompt:**

```text
<attachment name="error_log.txt">
2026-04-22 10:32:15 ERROR: Connection timeout to DB_01.
2026-04-22 10:33:01 WARN: Memory usage 85%.
2026-04-22 10:33:45 ERROR: Connection timeout to DB_01.
</attachment>

[User Query]: Count the frequency of each error type.

<code language="python" output-only="true">
Provide a Python dictionary named `error_counts` that summarizes the above log file. Do not write a script to parse it; just output the final dictionary object.
</code>
```

---

### 9. Interactive Document Redlining (file and think)

**Purpose:** Uses file for version control comparison and think for legal/compliance analysis.

**Prompt:**

```text
<file path="contract_v1.txt">
The Seller agrees to deliver the Goods by April 1st, 2026.
</file>

<file path="contract_v2_draft.txt">
The Seller agrees to use best efforts to deliver the Goods by April 1st, 2026, barring unforeseen supply chain disruptions.
</file>

<think>
Analyze the liability shift between V1 and V2. V1 implies a strict deadline. V2 introduces a force majeure loophole.
</think>

[User Query]: As the Buyer, explain why I should reject V2 in one sentence, and then show the exact text change using diff syntax.
```

---

### 10. Multi-Modal Context Synthesis (search, citation, code)

**Purpose:** A complex workflow prompt for a research assistant task requiring data discovery, verification, and structured computational output.

**Prompt:**

```text
<search>
Identify the GDP of Germany, France, and Italy for the most recent fiscal year available.
</search>

<citation format="footnote">
Provide a source for each country's GDP figure.
</citation>

[User Query]: Create a comparative summary.

<code language="csv">
After your summary, output the exact data in a comma-separated value format with headers: "Country", "GDP_USD_Trillion", "Year".
</code>

<think>
Ensure the CSV formatting is perfectly aligned with standard RFC 4180 specifications.
</think>
```

---

**Note on DeepSeek Tag Behavior**

- `<think>`: DeepSeek treats this as a hidden scratchpad. Content within these tags is not shown to the user by default in the API streaming response (though the UI may expose it with a toggle).
- `<search>`: Triggers the backend tool call. DeepSeek's search is deeply integrated with its reasoning core.
- `<citation>`: DeepSeek natively supports inline citation formatting better when explicitly prompted via XML tags.

```