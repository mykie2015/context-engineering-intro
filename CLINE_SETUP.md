# Cline Setup Guide

## Prerequisites

1. **Install VS Code**: Download from [code.visualstudio.com](https://code.visualstudio.com)
2. **Install Cline Extension**: Search for "Cline" in VS Code Extensions marketplace
3. **Configure API Keys**: Set up your preferred AI provider (Claude, OpenAI, etc.)

## Quick Setup

### 1. Install Cline
```bash
# Open VS Code
code .

# Go to Extensions (Ctrl+Shift+X)
# Search for "Cline"
# Install the extension
```

### 2. Configure API Keys
- Open Cline settings in VS Code
- Add your API key for your preferred provider
- Choose your model (Claude 3.5 Sonnet recommended)

### 3. Open This Template
```bash
# Clone the repository
git clone https://github.com/coleam00/Context-Engineering-Intro.git
cd Context-Engineering-Intro

# Open in VS Code
code .
```

### 4. Start Using Cline
- Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac)
- Type "Cline" and select "Cline: New Task"
- Or use the Cline sidebar that appears

## First Steps with the Template

### 1. Let Cline Read the Context
When you start Cline, it will automatically read the project files. The `.vscode/settings.json` file is configured to:
- Enable codebase context
- Set custom instructions to follow the project rules
- Provide optimal settings for Context Engineering

### 2. Edit Your Feature Request
Edit `INITIAL.md` with your specific feature requirements:
```markdown
## FEATURE:
Build a simple CLI tool that processes CSV files

## EXAMPLES:
Check the examples/ folder for patterns

## DOCUMENTATION:
- Python CSV documentation
- Click library for CLI

## OTHER CONSIDERATIONS:
- Handle large files efficiently
- Provide progress feedback
```

### 3. Ask Cline to Generate a PRP
Simply say: **"Please create a PRP for the feature described in INITIAL.md"**

Cline will:
1. Read your feature request
2. Research the codebase
3. Find relevant documentation
4. Create a comprehensive PRP

### 4. Ask Cline to Implement
Say: **"Please implement the PRP you just created"**

Cline will follow the PRP step-by-step, including:
- Creating the code structure
- Implementing the functionality
- Running tests and validation
- Fixing any issues

## Tips for Success

### 1. Be Specific in INITIAL.md
The more specific you are, the better the results:
- Include exact requirements
- Reference specific patterns to follow
- Mention libraries and technologies to use

### 2. Use the Examples Folder
- Add relevant code examples
- Show patterns you want followed
- Include both good and bad examples

### 3. Validate Frequently
- Ask Cline to run tests regularly
- Check that validation commands work
- Iterate on feedback

### 4. Follow the Context Engineering Method
- Always provide comprehensive context
- Use validation loops
- Reference existing patterns
- Include error handling

## Common Commands

### Starting a New Feature
```
"Please create a PRP for the feature in INITIAL.md"
```

### Implementing a Feature
```
"Please implement the PRP you just created"
```

### Running Tests
```
"Please run the tests and fix any failures"
```

### Updating Documentation
```
"Please update the README with the new feature"
```

## Troubleshooting

### Cline Doesn't Follow Patterns
- Ensure examples are clear and well-documented
- Add more detail to `AI_ASSISTANT_RULES.md`
- Reference specific files and patterns

### Implementation Fails
- Check that validation commands are executable
- Ensure examples are working and current
- Break down complex features into smaller steps

### Context is Missing
- Add more examples to the `examples/` folder
- Include relevant documentation links
- Capture gotchas in `AI_ASSISTANT_RULES.md`

## Advanced Usage

### Custom Instructions
You can modify `.vscode/settings.json` to add project-specific instructions:
```json
{
  "cline.customInstructions": "Follow the project rules defined in AI_ASSISTANT_RULES.md. Always read project documentation before starting work. Use the examples/ folder for reference patterns. Follow the Context Engineering methodology as described in CLINE_INSTRUCTIONS.md. [Add your custom instructions here]"
}
```

### Multiple Projects
Create separate folders for different projects, each with their own:
- `AI_ASSISTANT_RULES.md`
- `examples/` folder
- `PRPs/` directory
- Project-specific configuration

---

**Remember**: Context Engineering is about providing AI assistants with everything they need to succeed. The more context you provide, the better the results! 