
# Universal Template 
 
This prompt utilizes a structured XML-tagged architecture to separate core components—Role, Task, Context, and Output—for enhanced model comprehension. It combines persona adoption with explicit Chain of Thought reasoning to ensure logical, high-quality responses, while enforcing strict formatting constraints for consistent results.

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
