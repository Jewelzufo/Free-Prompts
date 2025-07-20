<!-- Description -->
<div align="center">
  <h1>Prompt Techniques Guide</h1>
</div>

<!-- Image -->
<div align="center">
  <img src="https://t2informatik.de/en/wp-content/uploads/sites/2/2024/01/prompt-engineering.jpg" alt="Prompt Engineering Stock Image" height="300" width="450"/>
</div>

---

<!-- Overview -->
This document provides a comprehensive guide to various prompting techniques for interacting with text generation models. It includes detailed descriptions of 50 different methods to craft prompts, each accompanied by a template that uses placeholders. The placeholders can be replaced with specific content to tailor prompts to your needs.

Additionally, a guide on how to use these placeholders is provided in a table format at the end of the document, ensuring clarity and ease of use.

<!-- Author information -->
*Julian A. Gonzalez, 2025*

<div align="center">
  <h2>Techniques:</h2>
</div>

<!-- List of Techniques -->
1. **Zero-Shot Prompting:**
>   - **Prompt Template:** "Answer the following question about `{subject}` without any examples provided: `{question}`."
2. **Few-Shot Prompting:**
>   - **Prompt Template:** "Provide examples of `{topic}` in the following format: `{example_format}`. Now answer the question: `{question}`."
3. **Chain of Thought (CoT) Prompting:**
>   - **Prompt Template:** "Explain your reasoning step-by-step before answering the question: `{question}`."
4. **Self-Consistency:**
>   - **Prompt Template:** "Generate `{number}` different answers to the question `{question}` and explain which one is most consistent."
5. **Tree-of-Thoughts (ToT) Prompting:**
>   - **Prompt Template:** "Explore multiple approaches to solve `{problem}` and present them in a tree structure."
6. **Graph-of-Thoughts (GoT) Prompting:**
>   - **Prompt Template:** "Map out the relationships between concepts in `{subject}` and present them as a graph."
7. **System 2 Attention Prompting:**
>   - **Prompt Template:** "Carefully analyze `{issue}` by considering all angles and potential biases."
8. **Thread of Thought (ThoT) Prompting:**
>   - **Prompt Template:** "Develop a narrative around `{topic}` by connecting related ideas in a coherent thread."
9. **Hallucination Mitigation:**
>   - **Prompt Template:** "Provide strategies for mitigating hallucinations in responses about `{subject}`."
10. **Synthetic Prompting:**
>    - **Prompt Template:** "Create a synthetic scenario involving `{context}` and describe how to handle it."
11. **Scaling Laws in Prompt Engineering:**
>    - **Prompt Template:** "Explain how scaling affects prompt responses in `{application_area}`."
12. **Prompting-Based Data Programming:**
>    - **Prompt Template:** "Design a prompt to extract `{relation}` from documents about `{domain}`."
13. **Commonsense-Aware Prompting:**
>    - **Prompt Template:** "Generate a dialogue that incorporates common sense about `{scenario}`."
14. **Progressive Prompting:**
>    - **Prompt Template:** "Create a sequence of prompts for learning about `{subject_area}` incrementally."
15. **Knowledge-Base Prompting:**
>    - **Prompt Template:** "Retrieve information about `{topic}` from the model's knowledge base."
16. **Declarative Language Model Calls:**
>    - **Prompt Template:** "Create a self-improving pipeline for `{process_name}` focusing on `{specific_outcome}`."
17. **Prompt Hacking and Vulnerabilities:**
>    - **Prompt Template:** "Identify vulnerabilities in responses to queries about `{scenario}`."
18. **AI Integration in the Workplace:**
>    - **Prompt Template:** "Discuss how AI can be integrated into tasks related to `{industry_or_task}`."
19. **Contextual Prompting:**
>    - **Prompt Template:** "Provide an answer to `{question}` considering the following context: `{context}`."
20. **Role-Based Prompting:**
>    - **Prompt Template:** "Assume the role of `{role}` and answer the question: `{question}`."
21. **Contrastive Prompting:**
>    - **Prompt Template:** "Compare and contrast `{concept_1}` and `{concept_2}` in the context of `{subject}`."
22. **Analogical Prompting:**
>    - **Prompt Template:** "Explain `{complex_concept}` using an analogy related to `{familiar_concept}`."
23. **Iterative Prompting:**
>    - **Prompt Template:** "Refine the response to `{initial_prompt}` based on feedback: `{feedback}`."
24. **Meta-Prompting:**
>    - **Prompt Template:** "Generate a new prompt that effectively elicits information about `{topic}`."
25. **Reverse Prompting:**
>    - **Prompt Template:** "Identify what prompt might have generated the following response: `{response}`."
26. **Multi-Turn Prompting:**
>    - **Prompt Template:** "Engage in a multi-turn dialogue about `{topic}` starting with: `{initial_question}`."
27. **Conditional Prompting:**
>    - **Prompt Template:** "If `{condition}` is true, then answer `{question}`; otherwise, ask for clarification."
28. **Creative Prompting:**
>    - **Prompt Template:** "Write a creative story about `{theme}` that includes elements of `{element_1}` and `{element_2}`."
29. **Debate Prompting:**
>    - **Prompt Template:** "Present arguments both for and against the statement: `{statement}`."
30. **Summarization Prompting:**
>    - **Prompt Template:** "Summarize the following text about `{topic}` in `{word_count}` words: `{text}`."
31. **Instructional Prompting:**
>    - **Prompt Template:** "Provide step-by-step instructions for completing `{task}`."
32. **Reflective Prompting:**
>    - **Prompt Template:** "Reflect on the implications of `{event_or_decision}` and discuss potential outcomes."
33. **Predictive Prompting:**
>    - **Prompt Template:** "Predict how `{variable}` might affect `{outcome}` in the future."
34. **Explanatory Prompting:**
>    - **Prompt Template:** "Explain the concept of `{concept}` in simple terms suitable for a `{audience}`."
35. **Elaborative Prompting:**
>    - **Prompt Template:** "Expand on the idea of `{idea}` with detailed examples and explanations."
36. **Comparative Analysis:**
>    - **Prompt Template:** "Compare `{item_1}` and `{item_2}` in terms of `{criteria}`."
37. **Cause and Effect Prompting:**
>    - **Prompt Template:** "Analyze the causes and effects of `{phenomenon}`."
38. **Hypothetical Scenario Prompting:**
>    - **Prompt Template:** "Describe what would happen if `{hypothetical_situation}` occurred."
39. **Procedural Prompting:**
>    - **Prompt Template:** "Outline the procedure for accomplishing `{goal}`."
40. **Evaluative Prompting:**
>    - **Prompt Template:** "Evaluate the effectiveness of `{method_or_tool}` in achieving `{objective}`."
41. **Descriptive Prompting:**
>    - **Prompt Template:** "Describe the characteristics of `{entity_or_place}` in detail."
42. **Narrative Prompting:**
>    - **Prompt Template:** "Write a narrative about `{event}` from the perspective of `{character}`."
43. **Persuasive Prompting:**
>    - **Prompt Template:** "Create a persuasive argument for `{position}` regarding `{issue}`."
44. **Interview Simulation Prompting:**
>    - **Prompt Template:** "Simulate an interview with `{personality}` asking questions about `{topic}`."
45. **Brainstorming Prompting:**
>    - **Prompt Template:** "Generate ideas for `{project_or_concept}` that incorporate `{requirement}`."
46. **Problem-Solving Prompting:**
>    - **Prompt Template:** "Propose solutions to the problem of `{problem}` considering `{constraints}`."
47. **Feedback Request Prompting:**
>    - **Prompt Template:** "Provide constructive feedback on `{submission_or_idea}` focusing on `{aspect}`."
48. **Prioritization Prompting:**
>    - **Prompt Template:** "Help prioritize the following tasks based on `{criteria}`: `{list_of_tasks}`."
49. **Scenario Analysis Prompting:**
>    - **Prompt Template:** "Analyze the potential outcomes of `{scenario}` considering `{variables}`."
50. **Decision-Making Prompting:**
>    - **Prompt Template:** "Help decide between `{option_1}` and `{option_2}` based on `{factors}`."

---

<div align="center">
<h2>How to Use Placeholders</h2>
</div>

| Placeholder Syntax         | Description                                                        | Example Usage                                                                                                                                 |
| -------------------------- | ------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `{subject}`                | Represents the subject or topic of interest in the prompt.         | `"Answer the following question about mathematics without any examples provided: What is 2+2?"`                                               |
| `{question}`               | The specific question you want the model to answer.                | `"What is the capital of France?"`                                                                                                            |
| `{topic}`                  | The topic or subject area being addressed in the prompt.           | `"Provide examples of renewable energy in the following format..."`                                                                           |
| `{example_format}`         | The format in which examples should be provided.                   | `"List format: 1. Example 1, 2. Example 2"`                                                                                                   |
| `{number}`                 | A numerical value used to specify the number of items or answers.  | `"Generate 5 different answers to the question..."`                                                                                           |
| `{problem}`                | The problem that needs to be solved.                               | `"Explore multiple approaches to solve climate change..."`                                                                                    |
| `{issue}`                  | An issue or topic that needs careful analysis.                     | `"Carefully analyze deforestation by considering all angles..."`                                                                              |
| `{role}`                   | The role that the model should assume.                             | `"Assume the role of a teacher and answer the question: What is photosynthesis?"`                                                             |
| `{concept_1}, {concept_2}` | Concepts to be compared or contrasted.                             | `"Compare and contrast renewable energy and fossil fuels..."`                                                                                 |
| `{complex_concept}`        | A complex concept that needs explaining via analogy.               | `"Explain quantum computing using an analogy related to baking."`                                                                             |
| `{familiar_concept}`       | A familiar concept used to explain a complex concept.              | `"Explain quantum computing using an analogy related to baking."`                                                                             |
| `{initial_prompt}`         | The initial prompt that will be refined.                           | `"Refine the response to 'Explain photosynthesis' based on feedback..."`                                                                      |
| `{feedback}`               | Feedback to refine the initial prompt.                             | `"Make it simpler and more engaging."`                                                                                                        |
| `{topic}`                  | The topic of interest for generating a new prompt.                 | `"Generate a new prompt that effectively elicits information about artificial intelligence."`                                                 |
| `{response}`               | A response for which you want to identify the original prompt.     | `"Identify what prompt might have generated the following response: 'Photosynthesis is the process by which green plants..."`                 |
| `{context}`                | The context to be considered when answering the question.          | `"Provide an answer to 'What is the best renewable energy source?' considering the following context: In a region with abundant sunlight..."` |
| `{condition}`              | A condition that determines how the question should be answered.   | `"If the user is a beginner, then answer 'What is machine learning?'..."`                                                                     |
| `{theme}`                  | The theme around which a creative story should be written.         | `"Write a creative story about adventure that includes elements of mystery and friendship."`                                                  |
| `{element_1}, {element_2}` | Elements to be included in the creative story.                     | `"Write a creative story about adventure that includes elements of mystery and friendship."`                                                  |
| `{statement}`              | A statement for which arguments are to be presented.               | `"Present arguments both for and against the statement: 'Social media is beneficial for society.'"`                                           |
| `{word_count}`             | The number of words in which the text should be summarized.        | `"Summarize the following text about renewable energy in 100 words..."`                                                                       |
| `{task}`                   | The task for which step-by-step instructions are needed.           | `"Provide step-by-step instructions for completing a software installation."`                                                                 |
| `{event_or_decision}`      | An event or decision to reflect on.                                | `"Reflect on the implications of the industrial revolution..."`                                                                               |
| `{variable}`               | A variable whose effect on the outcome is to be predicted.         | `"Predict how temperature might affect crop yield in the future."`                                                                            |
| `{concept}`                | A concept to be explained in simple terms.                         | `"Explain the concept of gravity in simple terms suitable for a child."`                                                                      |
| `{audience}`               | The target audience for the explanation.                           | `"Explain the concept of gravity in simple terms suitable for a child."`                                                                      |
| `{idea}`                   | The idea that needs to be expanded upon.                           | `"Expand on the idea of sustainable living with detailed examples..."`                                                                        |
| `{item_1}, {item_2}`       | Items to be compared.                                              | `"Compare solar energy and wind energy in terms of efficiency."`                                                                              |
| `{criteria}`               | The criteria for comparison.                                       | `"Compare solar energy and wind energy in terms of efficiency."`                                                                              |
| `{phenomenon}`             | The phenomenon whose causes and effects are to be analyzed.        | `"Analyze the causes and effects of global warming."`                                                                                         |
| `{hypothetical_situation}` | A hypothetical situation to describe.                              | `"Describe what would happen if humans could photosynthesize."`                                                                               |
| `{goal}`                   | The goal for which a procedure is needed.                          | `"Outline the procedure for accomplishing universal healthcare."`                                                                             |
| `{method_or_tool}`         | The method or tool to be evaluated.                                | `"Evaluate the effectiveness of solar panels in achieving energy independence."`                                                              |
| `{objective}`              | The objective that the method or tool aims to achieve.             | `"Evaluate the effectiveness of solar panels in achieving energy independence."`                                                              |
| `{entity_or_place}`        | The entity or place whose characteristics are to be described.     | `"Describe the characteristics of the Amazon rainforest in detail."`                                                                          |
| `{character}`              | The character from whose perspective a narrative is to be written. | `"Write a narrative about the fall of the Berlin Wall from the perspective of a journalist."`                                                 |
| `{position}`               | The position for which a persuasive argument is to be created.     | `"Create a persuasive argument for renewable energy regarding climate change."`                                                               |
| `{issue}`                  | The issue regarding which a persuasive argument is to be created.  | `"Create a persuasive argument for renewable energy regarding climate change."`                                                               |
| `{personality}`            | The personality to be interviewed in a simulated interview.        | `"Simulate an interview with Albert Einstein asking questions about his theories."`                                                           |
| `{project_or_concept}`     | The project or concept for which ideas are to be generated.        | `"Generate ideas for a sustainable city that incorporates green spaces and renewable energy."`                                                |
| `{requirement}`            | The requirement that the ideas should incorporate.                 | `"Generate ideas for a sustainable city that incorporates green spaces and renewable energy."`                                                |
| `{constraints}`            | The constraints to consider when proposing solutions.              | `"Propose solutions to the problem of plastic waste considering economic feasibility."`                                                       |
| `{submission_or_idea}`     | The submission or idea for which feedback is needed.               | `"Provide constructive feedback on my essay focusing on clarity and coherence."`                                                              |
| `{aspect}`                 | The aspect to focus on when providing feedback.                    | `"Provide constructive feedback on my essay focusing on clarity and coherence."`                                                              |
| `{list_of_tasks}`          | The list of tasks to be prioritized.                               | `"Help prioritize the following tasks based on urgency: Task 1, Task 2, Task 3."`                                                             |
| `{scenario}`               | The scenario whose potential outcomes are to be analyzed.          | `"Analyze the potential outcomes of a global shift to renewable energy..."`                                                                   |
| `{variables}`              | The variables to consider in scenario analysis.                    | `"Analyze the potential outcomes of a global shift to renewable energy considering economic and environmental factors."`                      |
| `{option_1}, {option_2}`   | Options to choose between in decision-making.                      | `"Help decide between solar power and wind power based on cost and efficiency."`                                                              |
| `{factors}`                | Factors to consider when making a decision.                        | `"Help decide between solar power and wind power based on cost and efficiency."`                                                              |
