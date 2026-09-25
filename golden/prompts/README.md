# Prompts Directory

This directory stores **prompt templates** and **LLM‑related artifacts** used by the AI Resume Builder.

## Purpose
- Centralize prompt engineering assets.
- Ensure consistency and reproducibility of AI‑generated content.
- Provide versioning and change tracking for prompts.

## Contents
- `system‑prompts/` – System‑level instructions for LLM interactions.
- `user‑prompts/` – User‑facing prompt templates (e.g., resume tailoring, ATS optimization).
- `few‑shot/` – Few‑shot examples for in‑context learning.
- `evaluation/` – Evaluation criteria and rubrics for prompt outputs.

## Rules
1. **Prompts are code**: Treat prompts as source code; version them, review changes, and test them.
2. **No secrets in prompts**: Never embed API keys, personal data, or other secrets in prompt files.
3. **Constitution compliance**: All prompts must adhere to the truthfulness and user‑control principles in the constitution.
4. **Testing**: Prompt changes should be validated with automated or manual evaluation before deployment.

## Usage
- Reference prompts by their relative path in the codebase.
- Update prompts when product behavior changes.
- Use the `golden/CHECKLIST.md` to verify prompt changes before merging.

---

**Version**: [PROMPTS_001] | **Last Reviewed**: [DATE]