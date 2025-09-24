# Claude Code Configuration - Workspace Git Sync Agent

## Project Context

**Project Name**: workspace-git-sync-agent
**Development Method**: BMAD (Breakthrough Method for AI-driven Agile Development)
**Repository**: https://github.com/DAESA24/workspace-git-sync-agent
**Current Phase**: Post-BMAD Installation - Ready for Explore Phase

## Project Overview

This project creates a specialized Claude sub-agent for automated workspace configuration management. The agent monitors workspace files, applies multi-layer validation, and commits changes to GitHub with intelligent, contextual commit messages.

### Core Problem
Manual Git workflow management creates friction in AI-assisted development. Existing automation tools lack the reliability validation needed for safe autonomous operation.

### Solution Approach
Focus on **outcome validation** rather than confidence prediction - verify that Git operations actually succeed and provide rollback mechanisms when they don't.

## Development Guidelines

### BMAD Phase Workflow
The project follows BMAD methodology with three phases:

1. **Explore Phase** (Current): Research agent architecture, validation patterns, and existing solutions
2. **Plan Phase**: Design comprehensive agent architecture with safety systems
3. **Execute Phase**: Implement agent with robust testing and deployment

### Key Development Principles
- **Safety First**: Multiple validation layers before any Git operations
- **Reliability Over Speed**: 100% verification of reported operations
- **Conservative Approach**: Only commit when high confidence with full validation
- **Learning Focused**: Document patterns for future AI automation projects

## Technical Requirements

### Validation Strategy (Multi-Layer)
```
Layer 1: File Whitelist (Primary Filter)
- .claude/* (Claude Code configurations)
- CLAUDE.md (project configuration)
- .gitignore (Git ignore rules)
- README.md (documentation)
- */README.md (project documentation)

Layer 2: Safety Checks (Critical)
- File size < 1MB
- No binary files (except specific image paths)
- Secrets scanning (API keys, tokens, passwords)
- JSON/YAML syntax validation

Layer 3: Change Analysis (Intelligence)
- Line changes < 100 lines per commit
- Text-based configuration changes only
- No new executable files

Layer 4: Confidence Scoring & Verification
- High confidence → Auto-commit with post-verification
- Medium/Low confidence → Log for manual review
- Failed verification → Automatic rollback
```

### Technology Stack
- **Runtime**: Node.js (BMAD compatibility requirement)
- **Package Manager**: npm for dependencies, npx for BMAD
- **File Monitoring**: chokidar library for cross-platform file watching
- **Git Operations**: simple-git library for programmatic Git control
- **Integration**: Claude Code tool integration, GitHub CLI compatibility

## File Structure Context

```
workspace-git-sync-agent/
├── .bmad-core/              # BMAD framework (75 files)
├── .claude/                 # Claude Code integration (34 files)
├── docs/                    # Project documentation
│   └── brief.md            # Detailed project requirements
├── explore/                 # Research and discovery phase
│   └── agent-architecture-research.md
├── plan/                    # Planning and design phase (TBD)
├── execute/                 # Implementation phase (TBD)
├── PROJECT_CHECKPOINT.md    # Development status and context
├── CLAUDE.md               # This configuration file
└── README.md               # Repository overview
```

## Development Context for Claude

### Current Status
- ✅ BMAD framework installed with complete agent ecosystem
- ✅ Claude Code integration configured with slash commands
- ✅ Repository setup with GitHub integration
- ✅ Initial documentation and project brief completed

### Immediate Next Steps
1. **Begin Explore Phase**: Research agent architecture patterns and validation systems
2. **Create PRD**: Use BMAD PM agent to develop comprehensive product requirements
3. **Architecture Design**: Use BMAD Architect agent for technical system design
4. **MVP Implementation**: Build core validation and Git automation functionality

### BMAD Integration Notes
- Use `/bmad-orchestrator` for phase management and workflow coordination
- Use `/pm` for requirements gathering and user story creation
- Use `/architect` for technical design and system architecture
- Use `/dev` for implementation planning and code development

## Success Metrics

### MVP Success Criteria
- **Reliability**: 100% of reported Git operations must actually complete
- **Safety**: Zero false positives (commits that shouldn't happen)
- **Accuracy**: 95%+ correct commit message generation
- **Recovery**: Complete rollback capability for failed operations

### Learning Objectives
- Establish reliable Claude sub-agent development patterns
- Create reusable validation frameworks for future automation
- Demonstrate Claude Code + GitHub CLI workflow integration
- Build foundational skills for AI-leveraged development scaling

## Key Files to Monitor

When working on this project, pay attention to these critical files:
- `PROJECT_CHECKPOINT.md` - Current development status and blocking issues
- `docs/brief.md` - Comprehensive project requirements and specifications
- `.bmad-core/` - BMAD framework files for methodology guidance
- `explore/` - Research outputs and architectural discoveries

## Agent Behavior Guidelines

### When Resuming Work
1. Always check `PROJECT_CHECKPOINT.md` for current status and blocking issues
2. Review recent commits to understand what was last completed
3. Identify current BMAD phase and appropriate next steps
4. Use BMAD agents (`/bmad-orchestrator`, `/pm`, `/architect`, `/dev`) for workflow guidance

### Safety Considerations
- Never commit without explicit user approval during development phase
- Always validate file changes meet whitelist requirements
- Test validation layers thoroughly before any automation
- Document all architectural decisions and validation logic

---

**Project Goal**: Create a reliable, safe, and intelligent workspace automation agent that serves as a foundation for advanced AI-assisted development patterns while solving real workflow friction.