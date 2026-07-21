---
name: code-to-notes
description: Use when converting Jupyter notebook (.ipynb) code into structured Obsidian notes. Triggers on phrases like "convert to notes", "code to notes", "make notes from notebook", "update notes from ipynb".
---

# Code To Notes Conversion

Converts class code from `.ipynb` notebooks into structured, revision-friendly Obsidian notes.

## Note Style Pattern

1. Small topic-wise headings (`##### ...`) under parent section.
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

## Conversion Workflow

1. **Read Target Note File First** — find where new content must be appended (end of current topic section). Do not rewrite unrelated sections.
2. **Extract Code Source** — read code from the `.ipynb`. Group into logical micro-topics.
3. **Create Topic Blocks** — for each micro-topic:
   - `##### Topic Name`
   - 1 short explanation sentence
   - Clean runnable code
   - Exact output in triple-quoted comment block
4. **Output Accuracy** — output must match the shown/run code exactly. Keep print labels consistent.
5. **Placement** — append at end of requested topic unless user says otherwise.

## Formatting Rules

- Preserve Obsidian formatting and links.
- Keep markdown headings consistent.
- No unnecessary prose or long theory.
- Prefer many small subtopics over one large block.
- Keep examples practical and easy to revise quickly.

## Safety Rules

- Never delete existing unrelated notes.
- Never change existing meaning unless user explicitly asks.
