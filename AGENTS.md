# AGENTS.md

## Project objective

This repository is used to build study notes for the **AWS Certified AI Practitioner (AIF-C01)** certification.

The work must be done across multiple iterations. In each iteration, the agent must:

1. start from the most up-to-date official AWS sources;
2. create or update Markdown notes in this repository;
3. keep the structure coherent and incremental;
4. clearly report what was completed and what remains.

## Language and references

- Write everything in **English** in this project.
- Always include a `References` section in notes.
- Always include explicit links for references, not just document names.
- When a statement depends on a recent AWS update, prefer official AWS links over secondary sources.

## Authoritative sources to use as the base

Use these primary sources, in this order:

1. Official AIF-C01 exam guide:
   `https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/ai-practitioner-01.html`
2. In-scope services list:
   `https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/aif-01-in-scope-services.html`
3. Exam guide revisions:
   `https://docs.aws.amazon.com/aws-certification/latest/ai-practitioner-01/aif-01-revisions.html`
4. Official AWS product documentation for the services mentioned in the guide.

For recent or newly added exam topics, always verify the official sources before writing:

- Amazon Bedrock AgentCore
- Kiro
- Strands Agents
- Amazon Q
- Amazon Quick
- Amazon Bedrock Prompt Management
- agentic AI
- Model Context Protocol (MCP)

## Update rules

- Do not assume that generative AI, agentic AI, or AWS service details are stable.
- If a section involves "latest", "new", "recent", "preview", "in scope", "exam update", or newly added services, verify online before writing.
- Always use absolute dates when mentioning official updates.
- If a feature is in preview, say so explicitly.
- Always distinguish between:
  - content clearly in scope for the exam;
  - useful background context that is not guaranteed exam scope.

## Repository structure

Use this structure:

- `notes/README.md`: notes index
- `notes/00-study-program.md`: study program and iteration roadmap
- `notes/01-*.md`, `notes/02-*.md`, ...: notes by domain or topic

If new files are needed, prefer ordered names with numeric prefixes.

## How to write the notes

- Write in English.
- Be concise but rigorous.
- Prefer lists, simple tables, and clear definitions.
- Avoid marketing language.
- Highlight distinctions that are likely to cause exam confusion:
  - AI vs ML vs deep learning vs GenAI vs agentic AI
  - training vs fine-tuning vs inference
  - prompt engineering vs context engineering
  - RAG vs fine-tuning vs in-context learning
  - guardrails vs IAM/policies vs governance
  - Bedrock vs SageMaker AI vs Kiro vs Strands vs AgentCore

## Recommended format for each notes file

Each new notes file should include these sections when relevant:

1. `Objective`
2. `Key concepts`
3. `AWS services to remember`
4. `Possible exam confusions`
5. `Flash questions`
6. `References`
7. `Last reviewed`

In `Last reviewed`, include the date of the latest source verification.

## Required iterative process

When working on this project:

1. read `notes/00-study-program.md`;
2. identify the next incomplete or outdated section;
3. verify the necessary official sources online;
4. update one coherent notes block per iteration unless the user asks otherwise;
5. update `notes/README.md` when adding new files;
6. in the final message, report:
   - files created or updated;
   - section covered;
   - sources verified;
   - any remaining gaps or follow-up items.

## Content constraints

- Do not invent technical details that are not confirmed by official sources.
- Do not copy large verbatim chunks from sources.
- Do not turn the notes into raw documentation dumps.
- Do not include out-of-scope services without labeling them clearly.

## Coverage priorities

Preferred order:

1. official exam guide and exam domains;
2. in-scope services;
3. recent guide revisions;
4. deeper coverage of new or high-probability exam topics;
5. quizzes, flashcards, and final review material.
