# 🧠 Prompting GPT-5 vs Earlier Models — A Novice Walkthrough

> **Audience:** First-time or early users who want reliable, practical prompting habits for GPT-5, and how they differ from older GPT models.

---

## 📑 Table of Contents
1. [What’s New in GPT-5](#1-whats-actually-new-in-gpt-5-relevant-to-prompting)
2. [A Simple Prompt Shape That Works](#2-a-simple-prompt-shape-that-works)
3. [Prompting Differences: GPT-5 vs Older Models](#3-prompting-differences-gpt-5-vs-older-models)
4. [System Prompts](#4-system-prompts)
5. [GPT-5-Specific Tips That Save Time](#5-gpt-5-specific-tips-that-save-time)
6. [Pocket Patterns (Copy-Paste)](#6-pocket-patterns-copy-paste)
7. [Common Pitfalls](#7-common-pitfalls)
8. [Quick Diff vs Earlier GPTs](#8-quick-diff-vs-earlier-gpts)
9. [Final Takeaway](#-final-takeaway)

---

## 1) What’s *Actually* New in GPT-5 (Relevant to Prompting)

- **Much larger context window (~400k tokens)**  
  Lets you paste bigger briefs, longer chats, and more reference material without “forgetting” earlier parts.  
  *Source: [OpenAI GPT-5 intro](https://openai.com/index/introducing-gpt-5/)*

- **More steerable instruction following**  
  Stronger adherence to tone, verbosity, and tool-use instructions.  
  *Source: [OpenAI docs](https://openai.com/index/introducing-gpt-5-for-developers/)*

- **Text + image inputs**  
  Mix screenshots, diagrams, or UI mocks with text for integrated answers.  
  *Source: [El País coverage](https://elpais.com/tecnologia/2025-08-07/openai-lanza-gpt-5-su-modelo-mas-avanzado-de-inteligencia-artificial.html)*

- **Better tool calling & structured outputs**  
  More reliable JSON/structured responses for automation.

- **New “verbosity” control**  
  Set responses to *low / medium / high* without rewording your prompt.

> **Note:** There’s still **no cross-session memory by default** — the larger context only helps retention *within* a single conversation.

---

## 2) A Simple Prompt Shape That Works

**Format:**

[ROLE / CONTEXT] → [TASK & CONSTRAINTS] → [OUTPUT FORMAT]

**Example:**

ROLE: You are a friendly productivity coach.

TASK: Create a 5-day focus plan for a designer switching between Figma and code. CONSTRAINTS:

6 hours/day max

Include 2 short breaks per session

Cite any timeboxing techniques


OUTPUT: Markdown table with columns: Day | Sessions | Method | Notes

**Why it works:**
- Role + constraints improve steerability.
- Explicit output format reduces follow-up edits.

---

## 3) Prompting Differences: GPT-5 vs Older Models

### A) Be **Precise**, Not Necessarily Long
Short, clear constraints work better than verbose descriptions.

Example:

Goal: “One-page brief | Audience: execs | Tone: direct | Include: 3 risks + mitigations | Output: Markdown”

### B) Use **Parameters** for Style/Length
Adjust verbosity (*low / medium / high*) instead of rewriting prompts for shorter/longer answers.

### C) Prefer **Structured Outputs**
Request JSON or Markdown tables with required fields for predictable formats.

### D) Mix **Modalities**
Attach screenshots, diagrams, or other images with text in the same prompt.

---

## 4) System Prompts

**What are they?**  
System prompts set the assistant’s *rules, tone, and priorities* for the whole conversation. They’re processed before user prompts.

**Example:**

You are a helpful, careful assistant. Follow the user’s instructions unless unsafe or contradictory. Default to concise explanations. When uncertain, ask 1 clarifying question. Prefer Markdown. Use bullet points over long paragraphs.

**Why important in GPT-5:**
- GPT-5 is more steerable, so a well-written system prompt tends to stick.
- Combine system prompts with clear task formatting for maximum consistency.

---

## 5) GPT-5-Specific Tips That Save Time

1. **Start with scaffolding**  
   Use the `[ROLE / TASK / CONSTRAINTS / OUTPUT]` pattern.

2. **Leverage the big context**  
   Include briefs, style guides, and examples in one message. Refer to them by name.

3. **Use verbosity intentionally**  
   High for deep reports, low for quick responses.

4. **Request structured outputs**  
   e.g.  
   ```json
   { "decision": "...", "rationale": "...", "next_steps": ["..."] }

5. Prompt for clarification
Tell GPT-5: “If requirements conflict, ask one targeted question.”




---

6) Pocket Patterns (Copy-Paste)

Explain Twice (Simple + Technical):

Explain <topic> simply (5 bullets), then give a technical summary (5–8 bullets). Add 2 references.

Decision Helper:

Goal: choose between A and B.
Constraints: <list>.
Output: JSON with {winner, 3 pros/cons each, risks, first_step}.

Image + Text Analysis:

Given the attached image + text description, identify 3 issues and propose fixes. Output a Markdown checklist.

Coding Task:

You are a senior engineer. Generate a function that does <X>.
Output: code + tests. If assumptions are missing, ask 1 question first.
Return: { "files": [{"path": "...", "content": "..."}] }


---

7) Common Pitfalls

Contradictory instructions → Keep system, developer, and user prompts aligned.

Unbounded output → Specify length/format or set verbosity.

Unlabeled references → Label sections in large context and refer to them by name.



---

8) Quick Diff vs Earlier GPTs

Feature	GPT-4 & Earlier	GPT-5

Context Window	4k–32k tokens	~400k tokens
Steerability	Good	Much stronger
Verbosity Parameter	No	Yes
Multimodal Input	Limited	Text + Images
Structured Output	Partial	Improved JSON / tables



---

📌 Final Takeaway

With GPT-5, you’ll get the best results by:

Being explicit but brief

Using ROLE / TASK / CONSTRAINTS / OUTPUT

Leaning on structured outputs

Adjusting verbosity instead of re-prompting

Keeping system prompts tight and instructions consistent



---

