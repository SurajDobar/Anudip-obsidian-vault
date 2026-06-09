> [!WARNING] # ⚠️ STRICTLY FOR GEMINI ⚠️
> ## THIS FILE IS FOR AI CONSUMPTION AND MODIFICATION ONLY.
> **DO NOT MANUALLY EDIT THIS DOCUMENT.**
> *Ignore this file if you are a human.*

# Project Instructions: Obsidian Vault Management

This file contains foundational mandates for AI assistants working in this vault. These rules must be followed strictly for all note-editing tasks.

## TOC Generation Workflow

When asked to generate or update a Table of Contents (TOC) for a markdown file:

1.  **Safety Branching:** Always create a new git branch (e.g., `feature/add-[filename]-toc`) before making any edits.
2.  **Heading Standardization:** 
    *   Clean all headings in the file before generating the TOC.
    *   Remove trailing spaces and special characters (e.g., `:`, `%`, `&`, `_`).
    *   Ensure headings are consistent (Title Case preferred) to guarantee anchor reliability across Markdown viewers (like Obsidian).
3.  **Standard Markdown TOC:**
    *   Generate a standard Markdown list with anchor links using the **Quoted Word Concatenation** format for Obsidian compatibility (e.g., `- [Heading Name](#"Heading""Name")`).
    *   Do NOT use hyphens in the anchor link parentheses or in the actual headings.
    *   Do NOT use HTML `<div>` tags or complex styling unless explicitly requested.
4.  **Prepension:** Insert the TOC at the very top of the file.
5.  **Clean Separation:** Leave exactly one blank line between the TOC and the start of the original content.
6.  **Content Integrity:** Under no circumstances should the original content below the TOC be edited, summarized, or reformatted, except for the heading standardization described in step 2.

## General Engineering Standards
- Maintain the visual integrity of Obsidian callouts (e.g., `> [!summary]`).
- Ensure all Wikilinks (`[[link]]`) and image embeds (`![[image]]`) remain functional and unaltered.
