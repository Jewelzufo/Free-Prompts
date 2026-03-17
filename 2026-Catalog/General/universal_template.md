
# Universal Template 
 
This prompt utilizes an XML-tagged agentic framework to structure the interaction flow. It defines a persona and objective, then explicitly invokes a Web Search action for real-time data retrieval. The architecture mandates Chain of Thought reasoning to synthesize search results before delivering a structured Markdown response.

<br>

## Template

```markdown
<role>{role} expert in {domain}</role>
<task>Your mission is to {task}.</task>
<web_search="{query}">
<think>Step-by-step reasoning here.</think>
<output format="Markdown">
{FINAL ANSWER}
</output>
```
