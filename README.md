# AI Tool Prompts

A curated collection of specialized prompts for AI assistants to help with software development workflows, debugging, and code auditing.

## Overview

This repository contains structured prompts designed to guide AI assistants through specific tasks in software development. Each prompt is crafted to provide consistent, thorough, and actionable results.

## Directory Structure

### 📋 `create-workflow/`
A systematic approach to project development from initial concept to implementation:

- **`01-request.prompt`** - Idea refinement and project request development
- **`02-spec.prompt`** - Detailed specification creation
- **`03-plan.prompt`** - Implementation planning and architecture
- **`04-codegen.prompt`** - Code generation and implementation
- **`05-review.prompt`** - Code review and quality assurance

### 🐛 `debug-workflow/`
OODA loop-based debugging methodology:

- **`01-observe.prompt`** - Gather and analyze bug information
- **`02-orient.prompt`** - Context analysis and pattern recognition
- **`03-decide.prompt`** - Root cause analysis and solution planning
- **`04-act.prompt`** - Implementation and verification

### 🔍 `audit/`
Specialized auditing prompts for code quality and compliance:

- **`accessibility-audit.prompt`** - WCAG compliance and accessibility review
- **`general-security-audit.prompt`** - Security vulnerability assessment

## Usage

Each `.prompt` file contains structured instructions for AI assistants. To use:

1. Copy the prompt content
2. Provide to your AI assistant
3. The AI will ask for the required information (marked with `{{VARIABLE_NAME}}` placeholders)
4. Follow the iterative process outlined in each prompt

## Key Features

- **Structured workflows** - Step-by-step processes for complex tasks
- **Consistent output** - Standardized templates and formats
- **Comprehensive coverage** - From project inception to deployment
- **Quality assurance** - Built-in review and validation steps

## Contributing

When adding new prompts:
- Follow the existing naming convention
- Include clear input requirements
- Provide structured output templates
- Test with AI assistants for effectiveness

## License

See [LICENSE](LICENSE) file for details.
