# AI Tool Prompts

A curated collection of specialized prompts for AI assistants to help with software development workflows, debugging, code auditing, and project management.

## Overview

This repository contains structured prompts designed to guide AI assistants through specific tasks in software development. Each prompt is crafted to provide consistent, thorough, and actionable results. All prompts are now in Markdown format (`.md`) for better readability and documentation.

## Directory Structure

### 📋 `create/`
Project development and workflow management:

#### `create-5-step-workflow/`
A systematic approach to project development from initial concept to implementation:
- **`01-request.md`** - Idea refinement and project request development
- **`02-spec.md`** - Detailed specification creation
- **`03-plan.md`** - Implementation planning and architecture
- **`04-codegen.md`** - Code generation and implementation
- **`05-review.md`** - Code review and quality assurance

#### Additional Development Tools
- **`test-driven-development.md`** - TDD methodology and test creation guidance

### 🐛 `debugging/`
Comprehensive debugging and analysis tools:

#### `debug-workflow/`
OODA loop-based debugging methodology:
- **`01-observe.md`** - Gather and analyze bug information
- **`02-orient.md`** - Context analysis and pattern recognition
- **`03-decide.md`** - Root cause analysis and solution planning
- **`04-act.md`** - Implementation and verification

#### Additional Analysis Tools
- **`five-whys-analysis.md`** - Root cause analysis using the Five Whys technique

### 🔍 `audit/`
Specialized auditing prompts for code quality and compliance:
- **`accessibility-audit.md`** - WCAG compliance and accessibility review
- **`general-security-audit.md`** - Security vulnerability assessment

### 📚 `documentation/`
Documentation generation and maintenance:
- **`generate-api-documentation.md`** - API documentation creation and standards
- **`update-claude-json.md`** - Claude configuration file maintenance

### 🔧 `refactor/`
Code optimization and improvement:
- **`optimize-files.md`** - Performance optimization and code refactoring

### 🔗 `git-commands/`
Version control and collaboration tools:
- **`commit.md`** - Structured commit message creation
- **`create-pull-request.md`** - Pull request creation and best practices

## Usage

Each `.md` file contains structured instructions for AI assistants. To use:

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
