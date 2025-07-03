# Context Engineering Template

A comprehensive template for getting started with Context Engineering - the discipline of engineering context for AI coding assistants so they have the information necessary to get the job done end to end.

> **Context Engineering is 10x better than prompt engineering and 100x better than vibe coding.**

## 🚀 Quick Start

```bash
# 1. Clone this template
git clone https://github.com/coleam00/Context-Engineering-Intro.git
cd Context-Engineering-Intro

# 2. Open in VS Code with Cline extension
code .

# 3. Let Cline read the project context
# Cline will automatically read AI_ASSISTANT_RULES.md and understand the project structure

# 4. Edit your initial feature request
# Edit INITIAL.md with your feature requirements

# 5. Ask Cline to generate a comprehensive PRP
# Simply ask: "Please create a PRP for the feature in INITIAL.md"

# 6. Ask Cline to execute the PRP
# Say: "Please implement the PRP you just created"
```

## 📚 Table of Contents

- [What is Context Engineering?](#what-is-context-engineering)
- [Template Structure](#template-structure)
- [Step-by-Step Guide](#step-by-step-guide)
- [Writing Effective INITIAL.md Files](#writing-effective-initialmd-files)
- [The PRP Workflow](#the-prp-workflow)
- [Using Examples Effectively](#using-examples-effectively)
- [Best Practices](#best-practices)

## What is Context Engineering?

Context Engineering represents a paradigm shift from traditional prompt engineering:

### Prompt Engineering vs Context Engineering

**Prompt Engineering:**
- Focuses on clever wording and specific phrasing
- Limited to how you phrase a task
- Like giving someone a sticky note

**Context Engineering:**
- A complete system for providing comprehensive context
- Includes documentation, examples, rules, patterns, and validation
- Like writing a full screenplay with all the details

### Why Context Engineering Matters

1. **Reduces AI Failures**: Most agent failures aren't model failures - they're context failures
2. **Ensures Consistency**: AI follows your project patterns and conventions
3. **Enables Complex Features**: AI can handle multi-step implementations with proper context
4. **Self-Correcting**: Validation loops allow AI to fix its own mistakes

## Template Structure

```
context-engineering-intro/
├── .vscode/
│   └── settings.json          # Cline configuration
├── PRPs/
│   ├── templates/
│   │   └── prp_base.md       # Base template for PRPs
│   └── EXAMPLE_multi_agent_prp.md  # Example of a complete PRP
├── examples/                  # Your code examples (critical!)
├── AI_ASSISTANT_RULES.md     # Global rules for AI assistant
├── CLINE_INSTRUCTIONS.md     # Specific instructions for Cline
├── INITIAL.md               # Template for feature requests
├── INITIAL_EXAMPLE.md       # Example feature request
└── README.md                # This file
```

## Step-by-Step Guide

### 1. Set Up Global Rules (AI_ASSISTANT_RULES.md)

The `AI_ASSISTANT_RULES.md` file contains project-wide rules that the AI assistant will follow in every conversation. The template includes:

- **Project awareness**: Reading planning docs, checking tasks
- **Code structure**: File size limits, module organization
- **Testing requirements**: Unit test patterns, coverage expectations
- **Style conventions**: Language preferences, formatting rules
- **Documentation standards**: Docstring formats, commenting practices

**You can use the provided template as-is or customize it for your project.**

### 2. Create Your Initial Feature Request

Edit `INITIAL.md` to describe what you want to build:

```markdown
## FEATURE:
[Describe what you want to build - be specific about functionality and requirements]

## EXAMPLES:
[List any example files in the examples/ folder and explain how they should be used]

## DOCUMENTATION:
[Include links to relevant documentation, APIs, or MCP server resources]

## OTHER CONSIDERATIONS:
[Mention any gotchas, specific requirements, or things AI assistants commonly miss]
```

**See `INITIAL_EXAMPLE.md` for a complete example.**

### 3. Generate the PRP

PRPs (Product Requirements Prompts) are comprehensive implementation blueprints that include:

- Complete context and documentation
- Implementation steps with validation
- Error handling patterns
- Test requirements

They are similar to PRDs (Product Requirements Documents) but are crafted more specifically to instruct an AI coding assistant.

**With Cline:**
Simply ask: "Please create a PRP for the feature described in INITIAL.md"

Cline will:
1. Read your feature request
2. Research the codebase for patterns
3. Search for relevant documentation
4. Create a comprehensive PRP in `PRPs/your-feature-name.md`

### 4. Execute the PRP

Once generated, ask Cline to implement the PRP:

**Say:** "Please implement the PRP you just created"

Cline will:
1. Read all context from the PRP
2. Create a detailed implementation plan
3. Execute each step with validation
4. Run tests and fix any issues
5. Ensure all success criteria are met

## Writing Effective INITIAL.md Files

### Key Sections Explained

**FEATURE**: Be specific and comprehensive
- ❌ "Build a web scraper"
- ✅ "Build an async web scraper using BeautifulSoup that extracts product data from e-commerce sites, handles rate limiting, and stores results in PostgreSQL"

**EXAMPLES**: Leverage the examples/ folder
- Place relevant code patterns in `examples/`
- Reference specific files and patterns to follow
- Explain what aspects should be mimicked

**DOCUMENTATION**: Include all relevant resources
- API documentation URLs
- Library guides
- MCP server documentation
- Database schemas

**OTHER CONSIDERATIONS**: Capture important details
- Authentication requirements
- Rate limits or quotas
- Common pitfalls
- Performance requirements

## The PRP Workflow

### How PRP Generation Works

Cline follows this process:

1. **Research Phase**
   - Analyzes your codebase for patterns
   - Searches for similar implementations
   - Identifies conventions to follow

2. **Documentation Gathering**
   - Searches for relevant API docs
   - Finds implementation examples
   - Identifies best practices

3. **PRP Creation**
   - Uses `PRPs/templates/prp_base.md` as foundation
   - Includes comprehensive context
   - Adds validation commands
   - Creates step-by-step implementation plan

4. **Quality Assurance**
   - Ensures all necessary context is included
   - Validates that implementation steps are clear
   - Confirms validation gates are executable

## Using Examples Effectively

### Structure Your Examples

```
examples/
├── basic_patterns/
│   ├── api_client.py         # HTTP client patterns
│   ├── database.py           # Database connection patterns
│   └── testing.py            # Test patterns
├── advanced_features/
│   ├── async_processing.py   # Async patterns
│   ├── error_handling.py     # Error handling patterns
│   └── authentication.py     # Auth patterns
└── project_specific/
    ├── your_domain_logic.py  # Domain-specific patterns
    └── integrations.py       # Integration patterns
```

### Example Guidelines

1. **Real, Working Code**: Examples should be runnable
2. **Well-Commented**: Explain why, not just what
3. **Pattern-Focused**: Show the approach, not just the solution
4. **Current**: Keep examples updated with your current patterns

## Best Practices

### For Context Engineering

1. **Be Comprehensive**: Include all necessary context
2. **Use Real Examples**: Reference actual code patterns
3. **Validate Everything**: Provide executable validation steps
4. **Iterate and Improve**: Refine PRPs based on results

### For Working with Cline

1. **Start Simple**: Begin with clear, specific requests
2. **Reference Context**: Point Cline to relevant files and patterns
3. **Validate Frequently**: Ask Cline to run tests and checks
4. **Be Iterative**: Build and test incrementally

### For Project Organization

1. **Keep Examples Updated**: Examples should reflect current practices
2. **Document Gotchas**: Capture common pitfalls in AI_ASSISTANT_RULES.md
3. **Use Descriptive Names**: Make file purposes clear
4. **Follow Conventions**: Stick to established patterns

## Advanced Features

### Multi-Agent Systems

See `PRPs/EXAMPLE_multi_agent_prp.md` for a complete example of how to build complex multi-agent systems using this template.

### Integration Patterns

The template supports various integration patterns:
- API integrations
- Database operations
- External service connections
- Authentication flows

### Testing Strategies

Built-in support for:
- Unit testing with pytest
- Integration testing
- Validation loops
- Error handling verification

## Troubleshooting

### Common Issues

1. **Cline doesn't follow patterns**: Ensure examples are clear and well-documented
2. **Implementation fails**: Check that validation commands are executable
3. **Context is missing**: Add more detail to AI_ASSISTANT_RULES.md and examples
4. **Tests don't pass**: Verify test patterns in examples folder

### Getting Help

1. Check `CLINE_INSTRUCTIONS.md` for detailed workflow
2. Review `PRPs/templates/prp_base.md` for PRP structure
3. Look at `PRPs/EXAMPLE_multi_agent_prp.md` for complex examples
4. Ensure `AI_ASSISTANT_RULES.md` contains all project rules

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add your improvements
4. Test with Cline
5. Submit a pull request

## License

This template is open source and available under the MIT License.

---

**Remember**: Context Engineering is about giving AI assistants everything they need to succeed. The more context you provide, the better the results!