Python Screening Task 2 – Debugging Assistant Prompt
📂 Repository Contents

PROMPT.md → Contains the structured natural language prompt for the AI debugging assistant.

README.md → Contains reasoning, design choices, and submission details.

🎯 Task Objective

The objective of this task is to design a prompt for an AI assistant that helps students debug their Python code without revealing the correct solution.

The AI should:

Analyze buggy Python code.

Offer structured, constructive hints.

Encourage debugging and learning.

Avoid giving away the full solution.

📝 Design Choices

Why I worded it the way I did:
I used a clear, step-by-step structure to ensure the AI always provides consistent, useful feedback. The wording focuses on analyzing problems, offering progressive hints, and including teaching moments instead of giving a direct fix.

How I ensured it avoids giving the solution:
The prompt explicitly states that the assistant must not provide corrected code by default. Guidance is broken into three levels of hints (conceptual → specific → most specific), so the student gets help in stages. The AI is also required to point out possible error categories instead of directly replacing code.

How it encourages helpful, student-friendly feedback:
The assistant is instructed to maintain a friendly, patient tone, provide small test cases, suggest debugging actions, and invite the student to respond with results. This creates an interactive and supportive experience similar to working with a tutor.

❓ Reasoning Questions

1. What tone and style should the AI use when responding?

Tone: friendly, patient, encouraging, non-judgmental.

Style: structured and concise. Use plain English for beginners, precise technical terms for advanced learners.

2. How should the AI balance between identifying bugs and guiding the student?

First, identify the symptom and possible causes.

Then, guide the student using progressive hints.

Avoid giving the direct solution — only provide the minimum guidance needed for the student to progress.

3. How would you adapt this prompt for beginner vs. advanced learners?

Beginners: Provide more detailed explanations, analogies, and suggest simple debug actions (like print() statements).

Advanced learners: Use concise technical language, suggest debugging tools (pdb, pytest), and focus on invariants, profiling, and edge cases.

🚀 How to Use

Clone or download this repository.

Open PROMPT.md to view the designed debugging prompt.

Use it directly with an AI assistant (like ChatGPT) as the instruction set for how it should behave.

📌 Submission Notes

This repository is prepared for Python Screening Task 2 (FOSSEE) submission.

It contains:

PROMPT.md – The designed AI debugging assistant prompt.

README.md – Full reasoning and design explanation.
