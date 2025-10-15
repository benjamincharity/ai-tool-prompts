---
allowed-tools: Bash(find:*), Bash(grep:*), Bash(rg:*), Bash(ls:*), Read, Write, Edit, Grep, Glob, Task
argument-hint: [audit-type=full|security|duplication|validation|zod] [path]
description: Audits codebase for Zod validation coverage, security gaps, and code quality issues
model: claude-3-5-sonnet-20241022
---

## Context

- Current directory: !`pwd`
- Project structure: !`ls -la`
- TypeScript/JavaScript files: !`find . -type f \( -name "*.ts" -o -name "*.tsx" -o -name "*.js" -o -name "*.jsx" \) -not -path "*/node_modules/*" -not -path "*/dist/*" | head -20`
- Package dependencies: !`[ -f package.json ] && cat package.json | grep -A 20 '"dependencies"'`

## Audit Scope

Audit Type: ${1:-full}
Target Path: ${2:-.}

## Your Task

Perform a comprehensive codebase audit focusing on:

### Phase 1: Security Analysis
- Identify ALL missing input validations, especially Zod schemas
- Find unvalidated API endpoints and form handlers
- Detect exposed secrets, API keys, or sensitive data
- Spot authentication/authorization gaps
- Check for common vulnerabilities (XSS, SQL injection, CSRF)
- Verify environment variable validation

### Phase 2: Code Quality Assessment
- Find exact duplicates and near-duplicate code (>80% similarity)
- Identify dead code and unused exports
- Locate commented-out code blocks
- Spot orphaned files and abandoned features
- Detect inconsistent naming patterns
- Find magic numbers and hardcoded values

### Phase 3: Validation Coverage
- Every user input MUST have Zod validation
- All API responses MUST be validated
- Database query results MUST have schemas
- File uploads MUST be sanitized
- Environment variables MUST use schemas
- Form submissions MUST validate all fields

### Phase 4: Modernization Opportunities
- Identify legacy patterns needing updates
- Find opportunities for React/Next.js optimizations
- Detect outdated dependencies
- Spot over-engineered abstractions
- Locate performance bottlenecks

## Deliverables

Provide a structured report with:

### Critical Security Issues
- File paths and line numbers
- Specific vulnerability details
- Recommended fixes with code examples
- Priority: CRITICAL

### Code Duplication Report
- Duplicated code blocks with locations
- Consolidation strategies
- Estimated lines of code reduction
- Priority: HIGH

### Missing Validations
- Unvalidated endpoints/inputs
- Required Zod schemas
- Implementation examples
- Priority: CRITICAL

### Modernization Recommendations
- Legacy patterns to update
- Modern alternatives
- Migration strategies
- Priority: MEDIUM

### Metrics Summary
- Total files audited
- Security gaps identified
- Lines of duplicate code
- Missing validation schemas
- Estimated maintenance reduction %

## Open-Source Considerations

This audit assumes an open-source production codebase:
- No security through obscurity
- All code is publicly visible
- Clear, auditable validation logic
- Explicit security boundaries
- Well-documented threat model

## Installation

Create command directory:
```bash
mkdir -p .claude/commands
```

Create command file: `audit-codebase.md` in the commands directory

Copy the command content with YAML frontmatter format

**Usage:**
- `/audit-codebase` - Execute the full audit
- `/audit-codebase security` - Security-focused audit
- `/audit-codebase validation` - Validation coverage check

**Config Format:** Markdown file with YAML frontmatter

**Config Paths:**
- Project: `.claude/commands/audit-codebase.md`
- User: `~/.claude/commands/audit-codebase.md`

## Implementation Notes

When auditing:
1. Start with high-risk areas (auth, API, forms)
2. Use ripgrep for fast pattern matching
3. Check all file extensions, not just .ts/.tsx
4. Include configuration files in security scan
5. Verify all external data sources have validation

Prioritize findings by:
- CRITICAL: Security vulnerabilities, missing validations
- HIGH: Major duplication, abandoned code
- MEDIUM: Modernization opportunities
- LOW: Style inconsistencies