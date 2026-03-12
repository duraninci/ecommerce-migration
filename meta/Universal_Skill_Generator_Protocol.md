# Universal Skill Set Generator: Execution Protocol

## Overview
This document outlines the exact, step-by-step workflow the AI must follow when a user requests a new skill set using the Universal Skill Set Generator (USSG). This protocol ensures consistency, depth, and rigorous research integration regardless of the subject matter.

## Step 1: The Intake Interview (Prompting the User)
When a user initiates a request (e.g., "Generate a skill set on Quantum Computing"), the AI must first ask a standardized set of clarifying questions to calibrate the generation engine:

1.  **Target Module Count:** "How comprehensive should this be? (e.g., 20, 30, 40, or 50 modules?)"
2.  **Difficulty Level:** "Is the target audience Beginner, Intermediate, Advanced, or Expert?"
3.  **Primary Use Case:** "What will the end-user primarily do with this information? (e.g., academic research, practical application, business strategy?)"
4.  **Provided Context:** "Do you have any specific documents, data, or frameworks you want integrated into the base knowledge?"

## Step 2: Autonomous Deep Research
Once the parameters are set, the AI enters the research phase. It must not rely solely on its pre-existing training data. It must execute targeted web searches using the `search` tool to gather the most current information.

### Research Vectors:
*   **Vector 1 (Foundations):** Search for "canonical texts," "core principles," and "history of [Topic]."
*   **Vector 2 (Current State):** Search for "[Topic] trends 2025," "state of the art [Topic]," and "recent breakthroughs in [Topic]."
*   **Vector 3 (Data & Statistics):** Search for "market size [Topic]," "statistical analysis [Topic]," or relevant empirical data.
*   **Vector 4 (Controversies/Edge Cases):** Search for "debates in [Topic]," "limitations of [Topic]," or "future challenges [Topic]."

*Output of Step 2: A temporary "Knowledge Ledger" document storing key facts, URLs, and data points.*

## Step 3: Structural Blueprint Generation
The AI drafts the complete 20-50 module outline based on the Universal Module Taxonomy (see Architecture document).

### Blueprint Formatting Requirements:
*   Module Number and Title.
*   A one-sentence objective for the module.
*   A list of 3-5 core concepts to be covered.

*Action Required: The AI MUST present this blueprint to the user for approval or modification before proceeding to full generation.*

## Step 4: Iterative Module Generation (The Core Engine)
Upon user approval of the blueprint, the AI begins generating the modules sequentially. Because modules can be up to 10,000 words, they must be generated in batches (e.g., 5 modules at a time) to maintain quality and avoid token limits.

### The Interconnection Protocol
To ensure the skill set feels like a cohesive intelligence rather than a collection of disjointed essays, the AI must actively cross-reference.
*   **Forward Referencing:** In early modules, tease concepts that will be explored later (e.g., "While we will discuss the mathematical proofs in Module 24, it is important to understand the concept conceptually here...").
*   **Backward Referencing:** In later modules, recall foundational concepts (e.g., "Building upon the thermodynamic principles established in Module 3, we now apply them to...").

### Module Formatting Rules
Every module must follow a strict internal structure:
1.  **Overview:** A brief executive summary of the module.
2.  **Core Content:** The main body, broken into logical sub-sections (e.g., 4.1, 4.2, 4.3).
3.  **Data/Evidence:** Integration of statistics or case studies gathered during Step 2.
4.  **Actionable Takeaways:** A summary of how the user can apply this specific knowledge.

## Step 5: Compilation and Export
Once all modules are generated, the AI must compile them into a single master document.

### Openclaw Optimization Checks:
*   Ensure all headers use proper Markdown hierarchy (`#`, `##`, `###`).
*   Ensure all bolding is consistent for key terminology.
*   Ensure the table of contents is hyperlinked (if the output format supports it).

*Final Action: The AI delivers the completed master file to the user, ready for import into Openclaw.*
