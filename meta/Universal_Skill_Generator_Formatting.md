# Universal Skill Set Generator: Formatting & Openclaw Integration

## Overview
A 50-module, 500,000-word skill set is only useful if the target system (Openclaw) can ingest, parse, and retrieve the information efficiently. This document outlines the strict formatting specifications the USSG must follow to ensure seamless integration.

## 1. The Master Markdown Specification

Markdown (.md) is the primary output format, as it is lightweight, universally readable, and perfectly suited for AI context windows.

### Hierarchical Heading Strictness
Openclaw (and most LLMs) rely on heading hierarchies to understand document structure. The USSG must never skip heading levels.
*   `# H1` is reserved exclusively for the Master Title and Module Titles (e.g., `# Module 1: Introduction`).
*   `## H2` is used for the primary sections within a module (e.g., `## 1.1 The Core Concept`).
*   `### H3` is used for sub-sections (e.g., `### Historical Context`).
*   `#### H4` is the maximum depth allowed. Anything deeper should be formatted as a bolded list item.

### Semantic Bolding
The USSG must use bold text `**like this**` not for emphasis, but semantically:
1.  To highlight **New Terminology** the first time it is introduced.
2.  To highlight **Key Takeaways** or actionable commands.
3.  To define the "Key" in a key-value pair list.

### Tabular Data Representation
When presenting comparative data, timelines, or matrices (e.g., a Competitive Analysis matrix), the USSG must use standard Markdown tables rather than bulleted lists. Tables are easier for AI systems to parse as structured data.

```markdown
| Concept | Definition | Application |
| :--- | :--- | :--- |
| Alpha | The primary driver | Used in Phase 1 |
| Beta | The secondary metric | Used in Phase 3 |
```

## 2. Multi-Format Output Support

While Markdown is the default for Openclaw, the USSG is capable of generating the skill set in alternative formats if requested by the user.

*   **PDF Compilation:** If requested, the AI will use a tool (like `manus-md-to-pdf`) to convert the final Master Markdown file into a polished, readable PDF, complete with a generated Table of Contents.
*   **Segmented Files:** Instead of one massive master file, the user can request the skill set be delivered as a zip file containing 50 individual `.md` files (e.g., `module_01.md`, `module_02.md`), which is sometimes preferred for specific vector database ingestion.

## 3. Openclaw "System Prompt" Generation

To maximize the utility of the skill set within Openclaw, the USSG must generate a custom "System Prompt" or "Persona Directive" to accompany the content.

### The Persona Directive
The final output must include a block of text designed to be pasted into Openclaw's core instructions. This tells Openclaw *how* to use the massive document it has just ingested.

**Template:**
> "You are an Artificial Super Intelligence acting as the ultimate expert in [Subject]. You have ingested the [Subject] Master Skill Set. When answering user queries, you must: 1) Prioritize the frameworks and data provided in the skill set over your general training data. 2) Always cite the specific Module (e.g., 'According to Module 14...') when providing strategic advice. 3) Maintain a [Requested Difficulty Level] tone. 4) If a user asks a tactical question, guide them through the step-by-step methodologies outlined in Pillar III of your skill set."

## 4. The Token Optimization Strategy

To ensure Openclaw does not "hallucinate" or lose track of information due to context window limits:
*   **Redundancy Minimization:** The USSG must ensure that a concept explained deeply in Module 2 is only briefly referenced (with a pointer back to Module 2) in Module 40, rather than re-explained entirely.
*   **The Executive Index:** The very first section of the Master Document must be an "Executive Index"—a hyper-condensed, 2-page summary of the entire 50-module skill set, acting as a quick-reference guide for the AI's attention mechanism.
