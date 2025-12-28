# General XML Template for use with LLMs

<details>
  <li>12-28-25</li>
  <li>Version 1.0</li>
  <li>Julian A. Gonzalez</li>
</details>

## Purpose

The purpose of the XML prompt template is to organize complex information into distinct functional components, such as task instructions, requirements, and examples, to enhance the clarity, accuracy, and parsability of AI responses.

By providing clear delineation and a hierarchical structure, the template allows for the joint optimization of content and formatting, which reduces ambiguity and ensures the model follows specific rules without making incorrect assumptions.

This structured framework is particularly critical for achieving consistent, high-quality results when using smaller, locally-run models.

### Template 

```xml
General AI Prompt XML Template
<ai_prompt>
  <!-- The primary goal or task for the AI to perform -->
  <task> [Insert main task or question here] </task>

  <!-- Context about the user to help tailor the response -->
  <user_profile>
    <role> [Your profession or role] </role>
    <location> [Your location/region if relevant] </location>
    <language> [Preferred response language] </language>
  </user_profile>

  <!-- Specific instructions and context to reduce ambiguity -->
  <context>
    <instructions> [Detailed step-by-step guidance or background] </instructions>
    <restrictions> [Limitations, boundaries, or things to avoid] </restrictions>
  </context>

  <!-- Technical or stylistic requirements -->
  <requirements>
    <style> [Technical, casual, academic, etc.] </style>
    <content_types> [e.g., code, math, diagrams, bullet points] </content_types>
    <formatting> [Specific output format like Markdown, JSON, or HTML] </formatting>
  </requirements>

  <!-- Few-shot examples to illustrate desired patterns -->
  <few_shot_examples>
    <example>
      <input> [Sample input] </input>
      <output> [Sample output] </output>
    </example>
  </few_shot_examples>

  <!-- The actual data or question to be processed -->
  <query> {{ [Insert specific question or data here] }} </query>
</ai_prompt>
```

