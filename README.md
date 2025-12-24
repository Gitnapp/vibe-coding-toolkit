# Vibe Coding Toolkit

A reusable collection of AI agent configurations, OpenSpec settings, and documentation rules for agentic vibe coding workflows.

## Overview

This toolkit provides a standardized setup for AI-assisted development across multiple AI coding tools:
- **Claude Code** (`.claude/`)
- **Gemini** (`.gemini/`)
- **Amazon Q / CodeWhisperer** (`.agent/`)
- **Factory** (`.factory/`)
- **Kilocode** (`.kilocode/`)
- **OpenCode** (`.opencode/`)
- **Kiro** (`.kiro/`)

## Quick Start

1. Copy the desired folders to your project root
2. Initialize OpenSpec: `npx openspec init`
3. Customize `openspec/project.md` for your project
4. Update `AGENTS.md` with project-specific instructions

## Structure

```
vibe-coding-toolkit/
├── README.md                    # This file
├── AGENTS.md.template           # Template for root agent instructions
├── CLAUDE.md.template           # Claude Code specific instructions
├── GEMINI.md.template           # Gemini specific instructions
│
├── .agent/                      # Amazon Q / CodeWhisperer workflows
│   └── workflows/
│       ├── openspec-apply.md
│       ├── openspec-archive.md
│       └── openspec-proposal.md
│
├── .claude/                     # Claude Code commands
│   ├── commands/
│   │   └── openspec/
│   │       ├── apply.md
│   │       ├── archive.md
│   │       └── proposal.md
│   └── settings.local.json.template
│
├── .factory/                    # Factory commands
│   └── commands/
│       ├── openspec-apply.md
│       ├── openspec-archive.md
│       └── openspec-proposal.md
│
├── .gemini/                     # Gemini commands
│   └── commands/
│       └── openspec/
│           ├── apply.toml
│           ├── archive.toml
│           └── proposal.toml
│
├── .kilocode/                   # Kilocode workflows
│   └── workflows/
│       ├── openspec-apply.md
│       ├── openspec-archive.md
│       └── openspec-proposal.md
│
├── .kiro/                       # Kiro steering rules
│   └── steering/
│       └── documentation-rules.md
│
├── .opencode/                   # OpenCode commands
│   ├── command/
│   │   ├── openspec-apply.md
│   │   ├── openspec-archive.md
│   │   └── openspec-proposal.md
│   └── package.json
│
├── openspec/                    # OpenSpec configuration
│   ├── AGENTS.md                # OpenSpec instructions for AI agents
│   ├── project.md.template      # Project context template
│   ├── specs/                   # Capability specifications
│   │   └── .gitkeep
│   └── changes/                 # Change proposals
│       └── .gitkeep
│
└── docs/                        # Documentation templates
    └── templates/
        ├── FOLDER.template.md
        ├── file-header.ts.template
        └── file-header.md.template
```

## Features

### 1. OpenSpec Integration
Spec-driven development workflow with:
- Change proposals (`proposal.md`, `tasks.md`, `design.md`)
- Capability specifications (`specs/`)
- Archive system for completed changes

### 2. Three-Layer Documentation
Hierarchical documentation system:
- **Layer 1 (Root)**: `AGENTS.md`, `openspec/project.md` - Global rules
- **Layer 2 (Folder)**: `FOLDER.md` in each directory - 3-line architecture
- **Layer 3 (File)**: Header comments - `@input`, `@output`, `@pos`

### 3. Multi-Agent Support
Unified commands across AI tools:
- `/openspec-proposal` - Create change proposals
- `/openspec-apply` - Implement approved changes
- `/openspec-archive` - Archive completed changes

## Usage

### Creating a Change Proposal
```bash
# Using Claude Code
/openspec-proposal add-user-authentication

# Using OpenSpec CLI
npx openspec list
npx openspec validate <change-id> --strict
```

### Implementing Changes
```bash
# Using any AI agent
/openspec-apply <change-id>
```

### Archiving Completed Changes
```bash
# Using any AI agent
/openspec-archive <change-id>

# Or via CLI
npx openspec archive <change-id> --yes
```

## Customization

### Project-Specific Instructions
Edit `AGENTS.md` to add:
- Project-specific conventions
- Tech stack details
- Custom workflows

### Documentation Rules
Edit `.kiro/steering/documentation-rules.md` to customize:
- File header format
- FOLDER.md structure
- Update triggers

## License

MIT - Feel free to use and modify for your projects.
