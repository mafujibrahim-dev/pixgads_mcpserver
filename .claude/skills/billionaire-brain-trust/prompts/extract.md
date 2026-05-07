# Framework Extraction Prompt

Given:
- The user's question (verbatim)
- The selected route (e.g., `offer`)
- The two operator reference files for that route

Extract the following, applied to the user's specific situation:

## Instructions

1. **Do not summarise the framework generically.** Apply it to what the user actually said.

2. **For each operator in the stack**, identify:
   - Which of their top 3 frameworks is most relevant to this question?
   - What specific decision heuristic applies?
   - What failure mode should the user be warned about?

3. **Output format per operator**:

```
### [Operator Name]

**Framework**: [Framework name from their reference file]

**Applied**: [How this framework maps to the user's specific situation — 2–4 sentences, using their own words/context where possible]

**Heuristic**: [The specific if/then rule that applies here]

**Watch out for**: [The failure mode most likely to trip them up]
```

4. **Conflict check**: After extracting both operators, answer:
   - Do they recommend the same path, complementary paths, or conflicting paths?
   - If conflicting, state the trade-off explicitly so the user can choose

5. **Do not invent frameworks** that are not in the reference files. If neither operator has a directly relevant framework, say so and recommend a route switch.
