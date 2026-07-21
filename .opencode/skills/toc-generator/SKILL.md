---
name: toc-generator
description: Use when generating or updating a Table of Contents for a markdown file. Triggers on phrases like "add table of contents", "generate TOC", "update TOC", "missing TOC entries", "add missing headings to TOC".
---

# TOC Generator

Generate or update a Table of Contents (TOC) for any markdown file, adding only missing entries.

## Workflow

### Step 1: Read the target file

Read the file the user specifies. The file will have:
- An existing TOC at the top (as a markdown list with anchor links)
- Content with headings below the TOC

### Step 2: Extract all headings from the file

Scan the entire file for markdown headings (`#`, `##`, `###`, `####`, `#####`). These are the topics that should appear in the TOC.

### Step 3: Compare existing TOC with actual headings

- Parse the existing TOC entries to extract which headings are already covered
- Identify headings that exist in the file content but are missing from the TOC

### Step 4: Generate missing TOC entries

For each missing heading, create a TOC entry using the **Quoted Word Concatenation** format:

```
- [Heading Name](#"Heading""Name")
```

Rules:
- Each word in the heading gets its own double quotes in the anchor
- Use Title Case for display text (clean up lowercase headings)
- Preserve indentation hierarchy based on heading level (`#` = no indent, `##` = no indent, `###` = 2 spaces, `####` = 4 spaces, `#####` = 4 spaces)
- Do NOT use hyphens in anchor links or headings
- Do NOT add HTML `<div>` tags

### Step 5: Insert into the TOC

- Insert new entries at the correct position in the existing TOC
- Maintain the order of headings as they appear in the file
- Leave exactly one blank line between the TOC and the content below

### Step 6: Verify

- Do NOT modify any content below the TOC
- Only add missing TOC entries, do not duplicate existing ones

## Example

**Existing TOC:**
```
- [Python](#"Python")
- [What Is Python](#"What""Is""Python")
```

**Heading found in file but missing from TOC:** `## File Handling`

**Add:**
```
- [File Handling](#"File""Handling")
```

**Result TOC:**
```
- [Python](#"Python")
- [What Is Python](#"What""Is""Python")
- [File Handling](#"File""Handling")
```

## Important Notes

- Read the `Prompt files/Table_of_contents.md` for vault-specific conventions
- Never modify content below the TOC section
- Preserve all existing TOC entries
- Use Obsidian-compatible anchor format (quoted words)
