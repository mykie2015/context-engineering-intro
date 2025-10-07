# Setup Guide

This template works with both **Claude Code** (CLI) and **Cline** (VS Code extension).

## For Claude Code CLI

### Prerequisites
- Install [Claude Code](https://docs.anthropic.com/en/docs/claude-code/quickstart)

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/coleam00/Context-Engineering-Intro.git
   cd Context-Engineering-Intro
   ```

2. Claude Code will automatically read `CLAUDE.md` and use the commands in `.claude/commands/`

3. Configure permissions (optional):
   ```bash
   # Edit .claude/settings.local.json if needed
   # This file is in .gitignore (user-specific)
   ```

### Usage
```bash
# Generate a PRP
/generate-prp INITIAL.md

# Execute a PRP
/execute-prp PRPs/your-feature.md
```

---

## For Cline in VS Code

### Prerequisites
- Install [VS Code](https://code.visualstudio.com/)
- Install the [Cline extension](https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev)

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/coleam00/Context-Engineering-Intro.git
   cd Context-Engineering-Intro
   ```

2. Open in VS Code:
   ```bash
   code .
   ```

3. Cline will automatically:
   - Read `CLAUDE.md` for project rules (configured in `.vscode/settings.json`)
   - Load custom commands from `.clinerules/`

4. Configure VS Code settings (optional):
   ```json
   // .vscode/settings.json is pre-configured, but you can customize:
   {
     "cline.customInstructions": "Follow the project rules defined in CLAUDE.md...",
     "cline.alwaysAllowReadOnly": true
   }
   ```

### Usage
Open the Cline panel in VS Code and type:
```bash
# Generate a PRP
/generate-prp INITIAL.md

# Execute a PRP
/execute-prp PRPs/your-feature.md
```

---

## Customization

### Global Rules (CLAUDE.md)
Both tools read this file. Customize it with:
- Project conventions
- Testing requirements
- Code style preferences
- Module organization patterns

### Custom Commands
- **Claude Code**: Edit files in `.claude/commands/`
- **Cline**: Edit files in `.clinerules/`

Both use markdown format and support passing arguments.

### Examples Folder
Add code examples in `examples/` that both tools can reference:
- API client patterns
- Test patterns
- Architecture patterns
- Integration patterns

---

## Slash Command Syntax

Both tools support custom slash commands with slight syntax differences:

**Claude Code:**
```markdown
# Command file: .claude/commands/my-command.md
Feature file: $ARGUMENTS
```

**Cline:**
```markdown
# Command file: .clinerules/my-command.md
Feature file: {{ARGUMENTS}}
```

The template includes both formats for the provided commands.

---

## Tips for Both Tools

1. **Start with INITIAL.md**: Describe your feature clearly
2. **Provide examples**: Both tools learn from code patterns
3. **Use validation gates**: Include test commands in PRPs
4. **Leverage documentation**: Link to API docs in INITIAL.md
5. **Iterate**: Generate PRP → Review → Execute → Refine

---

## Troubleshooting

### Claude Code
- Ensure commands are in `.claude/commands/`
- Check `.claude/settings.local.json` for permissions

### Cline
- Ensure custom commands are in `.clinerules/`
- Check `.vscode/settings.json` has correct customInstructions
- Verify Cline extension is installed and activated

---

## Resources

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Cline Extension](https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev)
- [Context Engineering Best Practices](https://www.philschmid.de/context-engineering)