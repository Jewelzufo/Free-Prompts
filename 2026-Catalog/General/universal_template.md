
# Universal Template 

This template can be used with LLMs to produce quality outputs. Replace the `{placeholders}` with your own relevant data for your use case. 

<br>

## Template

```markdown
<role>{role} expert in {domain}</role>
<task>Your mission is to {task}.</task>
<search="{Domain Docs}">
<think>Step-by-step reasoning here.</think>
<output format="Markdown">
{FINAL ANSWER}
</output>
```