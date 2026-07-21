---
description: Convert a Jupyter notebook into structured Obsidian notes using the CODE_TO_NOTES style.
agent: build
---

Convert notebook code into notes. Follow the code-to-notes skill instructions exactly.

**Source notebook:** $1
**Target notes file:** $2

Steps:
1. Read the target notes file first to understand existing structure.
2. Read the source `.ipynb` notebook and extract all code/markdown cells.
3. Group code into logical micro-topics.
4. For each micro-topic, append to the target file:
   - `##### Topic Name`
   - 1 short explanation sentence
   - Clean runnable python code block
   - Exact output in triple-quoted format: `'''Output:\n ...\n'''`
5. Do not rewrite or delete any existing content in the target file.
6. Keep wording short, simple, and revision-friendly.

If the user provides only $1 (notebook path), infer the target notes file from the vault structure (e.g., `python/Advanced Python.md` for `python/python ipynb/Advanced python ipynb/*.ipynb`).
