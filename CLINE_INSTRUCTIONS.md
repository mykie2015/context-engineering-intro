# Cline Instructions for Context Engineering Template

## Project Overview
This is a Context Engineering template designed to help AI coding assistants (like you, Cline) implement features with comprehensive context and validation loops.

## Core Workflow

### 1. Start with Context
- **ALWAYS** read `AI_ASSISTANT_RULES.md` first for project rules and constraints
- Check `INITIAL.md` for the current feature request
- Review `examples/` folder for reference patterns
- Understand the project structure and existing conventions

### 2. Generate a PRP (Product Requirements Prompt)
Instead of the old `/generate-prp` command, follow this process:

1. **Research the codebase** for similar patterns
2. **Search for relevant documentation** and examples online
3. **Create a comprehensive PRP** using `PRPs/templates/prp_base.md` as template
4. **Save the PRP** in `PRPs/` directory with a descriptive name

### 3. Execute the PRP
Instead of the old `/execute-prp` command:

1. **Read the PRP thoroughly** to understand all requirements
2. **Create an implementation plan** using clear steps
3. **Execute each step** with proper validation
4. **Run tests and validations** at each stage
5. **Iterate until all success criteria are met**

## Key Principles

### Context is King
- Include ALL necessary documentation, examples, and caveats
- Reference existing code patterns to follow
- Capture library quirks and gotchas
- Provide executable validation commands

### Validation Loops
- Always provide executable tests/lints that can be run
- Fix failures iteratively
- Never skip validation steps
- Ensure code quality meets project standards

### Information Dense
- Use keywords and patterns from the codebase
- Reference specific files and line numbers when possible
- Include error handling strategies
- Document integration points

## File Structure Guidelines

- `AI_ASSISTANT_RULES.md` - Project rules and constraints (READ FIRST)
- `INITIAL.md` - Current feature request template
- `examples/` - Reference code patterns
- `PRPs/` - Product Requirements Prompts
- `PRPs/templates/` - PRP templates

## Working with Features

### Step 1: Understand the Request
```bash
# Read the current feature request
cat INITIAL.md

# Check for examples
ls examples/

# Review project rules
cat AI_ASSISTANT_RULES.md
```

### Step 2: Research and Plan
- Search codebase for similar implementations
- Find relevant documentation and APIs
- Identify patterns to follow
- Note potential gotchas

### Step 3: Create PRP
- Use `PRPs/templates/prp_base.md` as starting point
- Include comprehensive context
- Add validation commands
- List implementation tasks in order

### Step 4: Implement
- Follow the PRP step by step
- Run validation commands frequently
- Test each component as you build
- Iterate based on test results

## Example Workflow

1. **Start**: `cat INITIAL.md` to understand what needs to be built
2. **Research**: Explore codebase and find similar patterns
3. **Plan**: Create a PRP with comprehensive context
4. **Build**: Implement following the PRP guidelines
5. **Validate**: Run tests and fix issues
6. **Complete**: Ensure all success criteria are met

## Quality Standards

- Follow all rules in `AI_ASSISTANT_RULES.md`
- Write comprehensive tests
- Use existing patterns and conventions
- Include proper error handling
- Document integration points
- Validate with executable commands

## Remember
- This template is designed to prevent AI failures through comprehensive context
- Always read the full context before starting
- Use the examples folder as your primary reference
- Follow the validation loops religiously
- Context Engineering is 10x better than prompt engineering! 