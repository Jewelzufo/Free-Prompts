# Manus Prompt Template: Code Debugging, Testing, and Refactoring

This template is designed to guide the Manus agent through a structured process of analyzing, debugging, testing, and refactoring a provided code snippet.

## 1. Objective

The primary objective is to transform the provided `[CODE_LANGUAGE]` code snippet from its current state into a fully functional, tested, and refactored version that adheres to modern best practices for the specified language.

## 2. Input

### 2.1. Code Snippet

Provide the complete code block that requires debugging and refactoring.

\`\`\`[CODE_LANGUAGE]
[PASTE CODE SNIPPET HERE]
\`\`\`

### 2.2. Expected Functionality

Describe the intended behavior and functionality of the code. Be specific about inputs, expected outputs, and any known edge cases.

[DESCRIBE EXPECTED FUNCTIONALITY HERE]

### 2.3. Known Issues (Optional)

List any known bugs, performance bottlenecks, or areas of concern in the current code.

[LIST KNOWN ISSUES HERE, OR STATE "None."]

## 3. Instructions for Manus Agent

The agent MUST follow these steps sequentially:

1.  **Initial Analysis & Debugging:**
    *   Identify all syntax errors, logical flaws, and runtime exceptions in the provided code.
    *   Determine the root cause of the code's failure to meet the **Expected Functionality**.
    *   Document the identified bugs and the proposed fixes.

2.  **Testing & Validation:**
    *   Develop a minimal set of test cases (unit tests or simple validation scripts) to confirm the **Expected Functionality**.
    *   Execute the original code against these tests (if possible) to demonstrate failure.
    *   Apply the proposed fixes and execute the corrected code against the same tests to demonstrate success.

3.  **Refactoring & Optimization:**
    *   Apply modern coding standards and best practices for `[CODE_LANGUAGE]`.
    *   Improve code readability, maintainability, and performance without altering the core **Expected Functionality**.
    *   Specifically focus on:
        *   Clear variable and function naming.
        *   Modularization and separation of concerns.
        *   Error handling and exception management.
        *   Efficiency improvements (e.g., algorithmic complexity).

## 4. Output Format

The final output MUST be structured as follows:

### 4.1. Debugging and Testing Summary

A concise, professional summary detailing the process. Use a Markdown table to present the key findings.

| Category | Description |
| :--- | :--- |
| **Original Bugs Found** | [List of all bugs found and fixed] |
| **Testing Strategy** | [Brief description of the tests used] |
| **Refactoring Focus** | [Key areas of refactoring, e.g., "Improved error handling and reduced algorithmic complexity."] |

### 4.2. Refactored Code

The complete, fully functional, tested, and refactored code snippet.

\`\`\`[CODE_LANGUAGE]
[PASTE REFACTORED CODE HERE]
\`\`\`

### 4.3. Test Cases (Optional but Recommended)

The test cases developed in Step 2 of the instructions, demonstrating the correctness of the **Refactored Code**.

\`\`\`[TEST_FRAMEWORK_OR_LANGUAGE]
[PASTE TEST CODE HERE]
\`\`\`

### 4.4. Detailed Change Log

A bulleted list of all significant changes made between the original and refactored versions, categorized by type (e.g., Bug Fixes, Refactoring, Optimization).

*   **Bug Fixes:**
    *   [Detail 1]
    *   [Detail 2]
*   **Refactoring:**
    *   [Detail 1]
    *   [Detail 2]
*   **Optimization:**
    *   [Detail 1]
    *   [Detail 2]
