# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a collection of specialized AI prompts for software development workflows. The repository contains structured prompt templates organized into different categories for debugging, development workflows, auditing, and documentation tasks.

## Repository Structure

The repository follows a categorized structure:

- `create-workflow/` - 5-step project development workflow (request → spec → plan → codegen → review)
- `debugging/debug-workflow/` - OODA loop-based debugging methodology (observe → orient → decide → act)
- `audit/` - Code auditing prompts for accessibility and security
- `documentation/` - Documentation generation and maintenance prompts
- `refactor/` - Code optimization and refactoring prompts

## Prompt File Format

All `.prompt` files follow a consistent structure:
- Clear task overview and objectives
- Required inputs marked with `{{VARIABLE_NAME}}` placeholders
- Structured output templates in Markdown format
- Step-by-step process instructions
- Context sections for variable substitution

## Working with Prompts

When modifying or creating new prompts:
1. Follow the existing naming convention (`##-description.prompt` for workflows)
2. Include clear input requirements with placeholder variables
3. Provide structured output templates
4. Maintain consistent formatting and sections
5. Test prompts for clarity and effectiveness

## Key Principles

- Prompts should be self-contained and comprehensive
- Output templates ensure consistent formatting across usage
- Variable placeholders enable reusable prompt templates
- Iterative processes are built into multi-step workflows
- Quality assurance steps are integrated throughout workflows