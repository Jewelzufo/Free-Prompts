# LangChain Prompt Template - 01

```python
from langchain.prompts import PromptTemplate

# Define the template stringtemplate_str = """
<role>{role} expert in {domain}</role>
<task>Your mission is to {task}.</task>
<web_search="{query}">
</web_search>

<chain_of_thought>
{chain_of_thought}
</chain_of_thought>

<output format="Markdown">
{output}
</output>
"""

# Create the PromptTemplate, listing every variable that will be supplied
prompt_template = PromptTemplate(
    input_variables=[
        "role",
        "domain",
        "task",
        "query",
        "chain_of_thought",
        "output",
    ],
    template=template_str,
)

# Example usage:
# filled_prompt = prompt_template.format(
#     role="Data",
#     domain="Science",
#     task="summarize the latest findings on quantum entanglement",
#     query="quantum entanglement 2024 breakthrough",
#     chain_of_thought="1. Read the search results...\n2. Identify key points...\n3. Synthesize...",
#     output="# Summary\n- Point 1\n- Point 2",
# )
# print(filled_prompt)
```

---

# How it works

- `{role}`:	The professional role (e.g., “Data Scientist”)	Inside <role>…</role>

- `{domain}`:	The field of expertise (e.g., “Machine Learning”)	Same <role> tag
  
- `{task}`:	The specific mission or instruction	Inside <task>…</task>

- `{query}`:	The web‑search query to be executed	Inside <web_search="{query}">
  
- `{chain_of_thought}`:	The reasoning process that interprets search results, cites sources, and builds the answer	Inside <chain_of_thought>…</chain_of_thought>

- `{output}`:	The final answer, already formatted as Markdown	Inside <output format="Markdown">…</output>
