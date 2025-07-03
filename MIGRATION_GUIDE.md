# Migration Guide: From Claude Code to Cline

## Overview

This Context Engineering template has been updated to work with **Cline VS Code extension** instead of Claude Code. This migration guide explains the changes and how to adapt your workflow.

## What Changed

### 1. File Structure Changes
```bash
# REMOVED (Claude Code specific)
.claude/
├── commands/
│   ├── generate-prp.md
│   └── execute-prp.md
└── settings.local.json

# ADDED/UPDATED (Cline compatible)
.vscode/
└── settings.json              # Updated for Cline
AI_ASSISTANT_RULES.md         # Renamed from CLAUDE.md
CLINE_INSTRUCTIONS.md         # New workflow instructions
CLINE_SETUP.md               # Setup guide
MIGRATION_GUIDE.md           # This file
```

### 2. Command Changes
| Old (Claude Code) | New (Cline) |
|-------------------|-------------|
| `/generate-prp INITIAL.md` | "Please create a PRP for the feature in INITIAL.md" |
| `/execute-prp PRPs/your-feature.md` | "Please implement the PRP you just created" |

### 3. Configuration Changes
- **Old**: `.claude/settings.local.json` with bash permissions
- **New**: `.vscode/settings.json` with Cline-specific settings

## Migration Steps

### Step 1: Update Your Environment
```bash
# 1. Install VS Code (if not already installed)
# Download from https://code.visualstudio.com

# 2. Install Cline Extension
# Go to Extensions in VS Code
# Search for "Cline" and install

# 3. Configure API Keys
# Open Cline settings and add your API key
```

### Step 2: Update Your Repository
```bash
# Pull the latest changes
git pull origin main

# Or if you forked the original template:
git remote add upstream https://github.com/coleam00/Context-Engineering-Intro.git
git pull upstream main
```

### Step 3: Update Your Workflow

#### Old Workflow (Claude Code)
1. Edit `INITIAL.md`
2. Run `/generate-prp INITIAL.md`
3. Run `/execute-prp PRPs/your-feature.md`

#### New Workflow (Cline)
1. Edit `INITIAL.md`
2. Ask Cline: "Please create a PRP for the feature in INITIAL.md"
3. Ask Cline: "Please implement the PRP you just created"

### Step 4: Review Updated Files
- `AI_ASSISTANT_RULES.md` (renamed from `CLAUDE.md`)
- `CLINE_INSTRUCTIONS.md` (new workflow guide)
- `README.md` (updated for Cline)
- `.vscode/settings.json` (Cline configuration)

## Benefits of Migration

### 1. Better Integration
- Native VS Code integration
- Improved codebase context awareness
- Better file navigation and editing

### 2. Enhanced Features
- Real-time collaboration
- Better diff viewing
- Integrated terminal and testing

### 3. Improved Workflow
- More natural conversation flow
- Better error handling
- Clearer validation loops

## Key Differences

### Command Structure
- **Claude Code**: Used slash commands (`/command`)
- **Cline**: Uses natural language requests

### Context Handling
- **Claude Code**: Manual context loading
- **Cline**: Automatic codebase context with `.vscode/settings.json`

### Validation
- **Claude Code**: Manual validation execution
- **Cline**: Integrated validation with better error reporting

## Best Practices for Cline

### 1. Be Explicit
Instead of: "Build a web scraper"
Use: "Please create a PRP for building an async web scraper using BeautifulSoup as described in INITIAL.md"

### 2. Reference Context
- Point to specific files: "Follow the pattern in examples/api_client.py"
- Reference rules: "Make sure to follow the testing rules in AI_ASSISTANT_RULES.md"

### 3. Validate Frequently
- "Please run the tests and fix any failures"
- "Please check that all validation commands pass"

### 4. Use the Examples Folder
- Add relevant code examples
- Reference them in your requests
- Keep them updated with current patterns

## Troubleshooting

### Common Issues

#### 1. Cline Not Following Patterns
**Problem**: Cline doesn't follow your project patterns
**Solution**: 
- Add more examples to the `examples/` folder
- Update `AI_ASSISTANT_RULES.md` with specific rules
- Reference patterns explicitly in your requests

#### 2. Missing Context
**Problem**: Cline seems to miss important context
**Solution**:
- Check `.vscode/settings.json` configuration
- Ensure `cline.codebaseContextOn` is `true`
- Add more detail to `AI_ASSISTANT_RULES.md`

#### 3. Validation Failures
**Problem**: Validation commands don't work
**Solution**:
- Check that commands are executable
- Update PRPs with correct validation steps
- Test validation commands manually first

### Getting Help

1. **Read the Documentation**
   - `CLINE_INSTRUCTIONS.md` - Detailed workflow
   - `CLINE_SETUP.md` - Setup guide
   - `README.md` - Complete overview

2. **Check Examples**
   - Review `PRPs/EXAMPLE_multi_agent_prp.md`
   - Look at `PRPs/templates/prp_base.md`

3. **Community Support**
   - GitHub Issues for template problems
   - Cline Discord/Community for extension issues

## Summary

The migration from Claude Code to Cline maintains all the core Context Engineering principles while providing a better, more integrated development experience. The workflow is now more natural and conversational, while still maintaining the comprehensive context and validation loops that make Context Engineering so effective.

**Key Takeaway**: The methodology remains the same - provide comprehensive context, use validation loops, and reference existing patterns. Only the interface has changed from slash commands to natural language requests.

---

**Need help?** Check the other documentation files or create an issue in the repository. 