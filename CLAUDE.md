# CLAUDE.md - AI Assistant Guide

**Repository**: test-claude-mcp
**Owner**: niknak88
**Purpose**: Testing and development with Claude Model Context Protocol (MCP)
**Last Updated**: 2025-11-14

---

## Table of Contents

1. [Repository Overview](#repository-overview)
2. [Codebase Structure](#codebase-structure)
3. [Development Workflows](#development-workflows)
4. [Conventions and Standards](#conventions-and-standards)
5. [AI Assistant Guidelines](#ai-assistant-guidelines)
6. [Testing Strategy](#testing-strategy)
7. [Deployment](#deployment)

---

## Repository Overview

### Purpose
This repository is designed for testing and developing applications using Claude's Model Context Protocol (MCP). It serves as a sandbox environment for experimenting with AI-assisted development workflows.

### Technology Stack
_To be populated as the project develops_

- **Languages**: TBD
- **Frameworks**: TBD
- **Build Tools**: TBD
- **Testing Frameworks**: TBD

### Current Status
🚧 **NEW REPOSITORY** - Currently empty and ready for initial development

---

## Codebase Structure

```
test-claude-mcp/
├── .git/                 # Git version control
├── CLAUDE.md            # This file - AI assistant guide
├── README.md            # User-facing documentation (to be created)
├── src/                 # Source code (to be created)
├── tests/               # Test files (to be created)
├── docs/                # Additional documentation (to be created)
└── config/              # Configuration files (to be created)
```

### Directory Conventions

When creating the project structure, follow these guidelines:

- **`src/`** - All production source code
  - Organize by feature or module
  - Keep files focused and single-purpose
  - Use clear, descriptive naming

- **`tests/`** - All test files
  - Mirror the structure of `src/`
  - Use `.test.*` or `.spec.*` naming convention
  - Include unit, integration, and e2e tests

- **`docs/`** - Detailed documentation
  - Architecture decision records (ADRs)
  - API documentation
  - Development guides

- **`config/`** - Configuration files
  - Environment-specific configs
  - Tool configurations
  - Never commit secrets (use `.env.example` instead)

---

## Development Workflows

### Git Workflow

#### Branch Naming Convention
- Feature branches: `feature/<description>`
- Bug fixes: `fix/<description>`
- Claude AI branches: `claude/<session-id>`
- Hotfixes: `hotfix/<description>`
- Releases: `release/<version>`

#### Commit Message Format
Follow conventional commits:

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types**: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

**Examples**:
```
feat(auth): add OAuth2 authentication
fix(api): resolve null pointer in user service
docs(readme): update installation instructions
```

#### Pull Request Process

1. Create feature branch from main
2. Develop and commit changes
3. Push to remote repository
4. Create PR with:
   - Clear title and description
   - Link to related issues
   - Test results
   - Screenshots (if UI changes)
5. Address review feedback
6. Squash and merge when approved

### Development Setup

_To be populated when dependencies are added_

```bash
# Clone the repository
git clone <repository-url>
cd test-claude-mcp

# Install dependencies
# (command to be added)

# Run tests
# (command to be added)

# Start development server
# (command to be added)
```

---

## Conventions and Standards

### Code Style

#### General Principles
- **Clarity over cleverness** - Write code that's easy to understand
- **DRY (Don't Repeat Yourself)** - Extract common patterns
- **KISS (Keep It Simple, Stupid)** - Avoid unnecessary complexity
- **YAGNI (You Aren't Gonna Need It)** - Don't add features prematurely

#### Naming Conventions
- **Variables**: descriptive, camelCase
- **Functions**: verb-based, camelCase
- **Classes**: PascalCase
- **Constants**: SCREAMING_SNAKE_CASE
- **Files**: kebab-case or match language conventions

#### File Organization
- One primary class/component per file
- Group related utilities together
- Keep files under 300 lines when possible
- Extract large functions into smaller, testable units

### Documentation Standards

#### Code Comments
- Explain **why**, not **what** (code shows what)
- Document complex algorithms
- Note non-obvious decisions
- Keep comments up-to-date with code changes

#### Function Documentation
Include for all public functions:
- Purpose/description
- Parameters and types
- Return value and type
- Exceptions/errors thrown
- Usage examples (for complex functions)

### Security Conventions

- **Never commit secrets** - Use environment variables
- **Validate all inputs** - Prevent injection attacks
- **Sanitize outputs** - Prevent XSS
- **Use prepared statements** - Prevent SQL injection
- **Keep dependencies updated** - Patch vulnerabilities
- **Implement proper authentication** - Secure endpoints
- **Use HTTPS** - Encrypt data in transit
- **Follow principle of least privilege** - Minimal permissions

---

## AI Assistant Guidelines

### When Working on This Repository

#### Before Starting Any Task

1. **Understand the context**
   - Read relevant code files
   - Check existing patterns and conventions
   - Review related issues/PRs
   - Understand the user's goals

2. **Plan the approach**
   - Use TodoWrite to break down complex tasks
   - Identify dependencies
   - Consider edge cases
   - Think about testing

3. **Verify assumptions**
   - Ask clarifying questions if unclear
   - Don't guess at requirements
   - Confirm technical approach for major changes

#### During Development

1. **Follow existing patterns**
   - Match the codebase style
   - Use established utilities and helpers
   - Don't introduce new patterns without reason

2. **Write secure code**
   - Validate inputs
   - Sanitize outputs
   - Avoid common vulnerabilities (OWASP Top 10)
   - Use parameterized queries
   - Handle errors properly

3. **Test thoroughly**
   - Write unit tests for new functions
   - Update tests when modifying code
   - Verify edge cases
   - Run full test suite before committing

4. **Document changes**
   - Add/update code comments
   - Update relevant documentation
   - Include clear commit messages
   - Note breaking changes

#### After Completing Work

1. **Review your changes**
   - Check for security issues
   - Verify tests pass
   - Ensure code follows conventions
   - Look for potential improvements

2. **Commit properly**
   - Write clear commit messages
   - Group related changes
   - Don't commit unrelated changes together

3. **Communicate clearly**
   - Summarize what was done
   - Explain key decisions
   - Note any issues or limitations
   - Suggest next steps if applicable

### AI-Specific Best Practices

#### Tool Usage
- Use **Read** before **Edit** or **Write**
- Prefer **Edit** over **Write** for existing files
- Use **Glob** and **Grep** efficiently for code search
- Leverage **Task** agents for complex explorations
- Run **Bash** commands for git, testing, building

#### Error Handling
- If you encounter an error, investigate before asking user
- Try alternative approaches
- Check for common issues (permissions, paths, dependencies)
- Provide context when reporting unsolvable issues

#### Communication
- Be concise but thorough
- Use code references with `file:line` format
- Explain technical decisions
- Don't over-explain obvious changes
- Ask questions when requirements are unclear

#### Code Quality
- Prioritize correctness over speed
- Consider performance implications
- Think about maintainability
- Don't over-engineer solutions
- Refactor when you see opportunities

---

## Testing Strategy

### Test Levels

#### Unit Tests
- Test individual functions/methods
- Mock external dependencies
- Fast execution
- High coverage target: >80%

#### Integration Tests
- Test component interactions
- Use test databases/services
- Verify data flow
- Critical paths must be covered

#### End-to-End Tests
- Test complete user workflows
- Use production-like environment
- Cover happy paths and critical errors
- Fewer tests, high value

### Testing Guidelines

1. **Write tests first** (TDD when appropriate)
2. **Test behavior, not implementation**
3. **Use descriptive test names**
4. **Keep tests independent**
5. **Don't test external libraries**
6. **Mock external services**
7. **Test edge cases and errors**
8. **Keep tests fast and reliable**

### Test Organization

```
tests/
├── unit/           # Unit tests mirroring src/
├── integration/    # Integration tests
├── e2e/           # End-to-end tests
├── fixtures/      # Test data
└── helpers/       # Test utilities
```

---

## Deployment

_To be populated when deployment strategy is determined_

### Environments
- **Development**: Local development
- **Staging**: Pre-production testing (TBD)
- **Production**: Live environment (TBD)

### Deployment Process
_To be defined_

### Monitoring and Logging
_To be defined_

---

## Quick Reference

### Common Commands
```bash
# To be populated with project-specific commands
```

### Important Files
- `CLAUDE.md` - This file, AI assistant guide
- `README.md` - User-facing documentation (to be created)
- `.gitignore` - Git ignore patterns (to be created)

### Useful Links
- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Conventional Commits](https://www.conventionalcommits.org/)

---

## Notes for Future Development

### When Adding New Features

1. Update this document with:
   - New directory structures
   - New conventions or patterns
   - Technology choices and rationale
   - Setup instructions
   - Testing requirements

2. Create ADRs (Architecture Decision Records) for:
   - Significant architectural choices
   - Technology selections
   - Pattern decisions
   - Trade-off analyses

3. Keep documentation in sync with code

### Maintenance Reminders

- Review and update this file quarterly
- Remove obsolete sections
- Add examples as patterns emerge
- Document lessons learned
- Update technology stack information

---

## Contributing

This repository follows the development workflows and conventions outlined above. When contributing:

1. Read this entire document
2. Follow established patterns
3. Write tests for new code
4. Update documentation
5. Create clear, focused commits
6. Submit PRs for review

---

**For AI Assistants**: This document is your primary guide for working with this repository. Always refer to it before starting work, and update it as the project evolves. When in doubt, ask the user for clarification rather than making assumptions.

**Last Updated**: 2025-11-14
**Document Version**: 1.0.0
