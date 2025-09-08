

**Why this wording & structure?**

The prompt sets explicit process and format rules so the assistant’s replies are consistent and actionable. The ordered sections (symptom → causes → progressive hints → tests → debugging steps) model how a human tutor diagnoses and teaches debugging without giving the answer away.

The three-tier hint system scaffolds learning: each hint increases specificity so students can attempt solving with increasing support, preserving learning while preventing accidental spoiling.

**How it avoids giving the solution**

It enforces an explicit “no full corrected code” rule and requires hints to be non-revealing (suggesting what to inspect, not how to fix).

The progressive hint escalation guards against accidentally giving away the fix too early: the assistant gives conceptual nudges before pointing at lines, and never supplies replacement code unless explicitly asked (and then only after a refusal/default warning).

**How it encourages student-friendly feedback**

It mandates an encouraging tone and asks the assistant to invite the student to try tests and report back.

It provides actionable debugging steps and small tests so students can experiment and confirm the fix themselves, which builds debugging skill rather than dependence.

**Reasoning (required answers)**

**1. What tone and style should the AI use when responding?**

Tone: friendly, patient, non-judgmental, encouraging. Avoid condescension. Praise attempts and small wins.

Style: structured and concise. Use short sections and bullet lists. For beginners, use plain English and analogies; for advanced users, be concise and use precise technical terms.

**2. How should the AI balance between identifying bugs and guiding the student?**

Prioritize diagnosis (what symptom and likely categories of causes). Then guide through Socratic hints (high-level → specific) so the student actively finds the fix. The assistant should reveal the minimal necessary information to let the student test hypotheses, but stop short of giving direct code fixes. If the student requests more help, reveal the next hint; do not move straight to the solution.

**3. How would you adapt this prompt for beginner vs. advanced learners?**

For beginners: Expand the “Conceptual explanation” section to include short, plain-language analogies (e.g., “Think of a loop index like a counter that starts at 0 and counts items — if it goes one too far it tries to access an item that doesn’t exist.”). Add explicit commands they can paste and run (print(x), assert isinstance(x, list)). Provide more intermediate scaffolding, e.g., example debug prints. Use simpler language and slower escalation of hints.

For advanced learners: Be more terse. Focus on invariants, edge cases, complexity, and unit tests. Offer pointers to profiling, pdb, or pytest idioms. Allow the assistant to use more technical synonyms and to propose short property-based tests or invariants to assert. Still avoid pasting full fixes.
