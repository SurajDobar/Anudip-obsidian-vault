```cmd
Use CODE_TO_NOTES.md. Target notes file: <path>. Source code file: <path>. Start topic from: <topic name>.
```

> [!WARNING] # ⚠️ STRICTLY FOR AI ASSISTANTS ⚠️
> ## THIS FILE IS FOR AI CONSUMPTION AND MODIFICATION ONLY.
> **DO NOT MANUALLY EDIT THIS DOCUMENT.**
> *Ignore this file if you are a human.*

# Project Instructions: Code To Notes Workflow

This file defines the standard method to convert class code into structured notes in this vault without repeatedly re-scanning style references.

## Source Style Reference (Fixed Pattern)

Use this structure pattern as the default note style:

1. Small topic-wise headings (`##### ...`) under the parent section (example: String operations).
2. One short explanation line per small topic.
3. One fenced `python` code block per small topic.
4. Include exact output inside the same code block using triple-quoted format:

```python
'''
Output:
 exact runtime output line(s)
'''
```

5. Keep wording simple, short, and revision-friendly.

## Code To Notes Conversion Workflow

When converting notebook/class code to notes:

1. **Read Target Note File First**
   - Find where new content must be appended (usually end of current topic section).
   - Do not rewrite unrelated sections.

2. **Extract Code Source**
   - Read code from the requested `.ipynb` (or provided source file).
   - Group code into logical micro-topics.

3. **Create Topic Blocks**
   - For each micro-topic:
     - Add `##### Topic Name`
     - Add 1 short explanation sentence.
     - Add clean runnable code.
     - Add exact output in triple-quoted comment block.

4. **Output Accuracy Rule**
   - Output must be exact to the shown/run code.
   - Keep print labels/output text consistent.

5. **Placement Rule**
   - Append new notes at the end of the requested topic unless user asks for another location.

## Formatting Rules

- Preserve Obsidian formatting and links.
- Keep markdown headings consistent.
- Do not add unnecessary prose or long theory.
- Prefer many small subtopics over one large block.
- Keep examples practical and easy to revise quickly.

## Safety Rules

- Never delete existing unrelated notes.
- Never change existing meaning unless user explicitly asks.
- If format conflict exists, follow latest direct user instruction over this file.
