# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

SuperClaude is a configuration framework that enhances Claude Code with specialized commands, cognitive personas, and development methodologies. This is a configuration-driven framework rather than traditional source code - it consists of YAML configuration files, Markdown command definitions, and template patterns.

## Installation and Setup Commands

### Installation
```bash
# Install SuperClaude framework
./install.sh                    # Install to ~/.claude/
./install.sh --dir /custom/path # Install to custom location
./install.sh --update          # Update existing installation
./install.sh --verify-checksums # Verify installation integrity
```

### Framework Testing
```bash
# Verify installation works
/load                          # Load project context
/analyze --code --think        # Test basic analysis
/analyze --persona-architect   # Test persona system
```

### Update and Maintenance
```bash
# Update framework
./install.sh --update --backup

# Verify integrity
./install.sh --verify-checksums

# Uninstall
./install.sh --uninstall
```

## Architecture Overview

SuperClaude follows a modular, template-driven architecture:

### Configuration Structure
```
.claude/
├── shared/                    # Framework-wide configurations
│   ├── superclaude-core.yml      # Core philosophy & token economy
│   ├── superclaude-personas.yml  # 9 cognitive personas
│   ├── superclaude-rules.yml     # Standards & practices
│   └── superclaude-mcp.yml       # MCP server integration
├── commands/                  # 18 specialized commands
│   ├── analyze.md, build.md, etc. # Individual command definitions
│   └── shared/                    # Shared command patterns
│       ├── flag-inheritance.yml   # Universal flag system
│       ├── universal-constants.yml # Symbols & abbreviations
│       └── [24 pattern files]     # Architecture, security, quality patterns
└── settings.local.json       # Local configuration
```

### Template System
- **@include references**: Template engine for configuration reuse
- **Flag inheritance**: Universal flags available on all commands  
- **Pattern libraries**: Shared behaviors for consistency
- **Token optimization**: 70% reduction through template reuse

## Core Design Principles

### Evidence-Based Standards
- All claims must be backed by testing, metrics, or documentation
- Prohibited language: "best|optimal|faster|secure|better|always|never"
- Required language: "may|could|potentially|measured|documented"
- Example: "Metrics show 15% performance improvement" (not "improved performance")

### Token Economy
- UltraCompressed mode (`--uc`) for 70% token reduction
- Symbol system: → | & : » ∀ ∃ ∴ ∵ for efficient communication
- Structure priority: YAML > Tables > Lists > Prose
- Auto-compression when context >75% usage

### Security & Quality
- Project directory restrictions prevent external access
- Git safety: Uncommitted changes warnings, branch validation
- Progressive quality gates: Validation → Implementation → Testing
- OWASP Top 10 compliance patterns

## Command System

### 18 Specialized Commands
Commands are organized by development lifecycle:

**Analysis & Investigation**
- `/analyze` - Code and system analysis
- `/scan` - Security and validation audits
- `/troubleshoot` - Debugging and issue resolution

**Development & Building** 
- `/build` - Project builder with stack templates
- `/design` - System architecture and patterns
- `/dev-setup` - Development environment configuration

**Quality & Improvement**
- `/test` - Testing framework with coverage
- `/improve` - Enhancement and optimization
- `/review` - AI-powered code review
- `/cleanup` - Project maintenance

**Operations & Deployment**
- `/deploy` - Application deployment
- `/migrate` - Database and code migrations
- `/git` - Git workflow management

**Documentation & Workflow**
- `/document` - Documentation creation
- `/explain` - Code explanations
- `/estimate` - Project estimation
- `/task` - Task management
- `/load` - Project context loading
- `/spawn` - Parallel task execution

### Universal Flags (Available on All Commands)
```bash
# Planning & Execution
--plan              # Plan before execution
--dry-run           # Preview changes
--force             # Override safety checks

# Thinking Depth
--think             # Standard analysis
--think-hard        # Deeper analysis  
--ultrathink        # Maximum depth

# Token Management
--uc, --ultracompressed  # 70% token reduction
--no-mcp            # Disable external servers

# MCP Server Control
--c7                # Context7 (library docs)
--seq               # Sequential (complex reasoning)
--magic             # Magic (UI components)  
--pup               # Puppeteer (browser automation)
--all-mcp           # Enable all MCP servers

# Cognitive Personas
--persona-architect     # Systems design thinking
--persona-frontend      # UX-focused development
--persona-backend       # Server systems focus
--persona-security      # Security-first analysis
--persona-analyzer      # Root cause analysis
--persona-qa            # Quality assurance
--persona-performance   # Optimization focus
--persona-refactorer    # Code quality improvement
--persona-mentor        # Knowledge sharing
```

## Cognitive Personas

SuperClaude includes 9 specialized personas that provide domain-specific approaches:

### Persona Characteristics
Each persona has distinct:
- **Identity & Core Beliefs**: Fundamental perspective
- **Decision Framework**: How they prioritize concerns
- **Risk Profile**: Conservative vs aggressive preferences
- **Success Metrics**: Domain-specific quality measures  
- **MCP Preferences**: Which external servers they prefer
- **Problem-Solving Style**: Methodological approaches

### Usage Patterns
```bash
# Architecture work
/design --api --ddd --persona-architect

# Frontend development  
/build --react --magic --persona-frontend

# Security review
/scan --security --owasp --persona-security

# Performance optimization
/improve --performance --persona-performance
```

### Auto-Activation
Personas automatically activate based on:
- File types: `.tsx/.jsx` → frontend, `.test.*` → qa
- Keywords: "slow/performance" → performance, "auth/secure" → security
- Import patterns: UI libraries → frontend, testing → qa

## MCP (Model Context Protocol) Integration

### External Server Capabilities
SuperClaude integrates with 4 MCP servers (must be installed separately):

**Context7** (`--c7`)
- Library documentation and code examples
- Auto-triggers on import detection
- Required for external library usage

**Sequential** (`--seq`) 
- Multi-step complex reasoning
- Best for architecture, debugging, system design
- High token cost but comprehensive analysis

**Magic** (`--magic`)
- UI component generation via 21st.dev
- React/Vue components, design systems
- Auto-suggests for UI-related tasks

**Puppeteer** (`--pup`)
- Browser automation and testing
- E2E testing, performance monitoring
- Low token cost, high reliability

### MCP Usage Examples
```bash
# Research patterns require Context7
/build --react --c7             # Look up React patterns

# Complex analysis with Sequential
/troubleshoot --investigate --seq   # Multi-step reasoning

# UI development with Magic
/build --component --magic      # Generate UI components

# Testing with Puppeteer
/test --e2e --pup              # Browser automation
```

## Development Workflows

### Common Command Chains
```bash
# Full-stack development
/load → /analyze --code → /design --api → /build --feature → /test --coverage → /deploy --staging

# Bug investigation
/troubleshoot --investigate --seq → /analyze --code --c7 → /improve → /test → /git

# Feature implementation
/analyze --code → /design --feature → /build --tdd → /test --coverage → /review --quality

# Security review
/scan --security --owasp → /analyze --architecture --seq → /improve --security → /test --security
```

### Quality Standards
- All external library usage requires Context7 lookup (`--c7`)
- Performance improvements must include metrics
- Security changes require OWASP validation  
- Features require test coverage and documentation
- Git commits should be atomic and well-documented

## Task Management

SuperClaude implements a two-tier task system:

### Level 1 Tasks (.claudedocs/tasks/)
- High-level features spanning multiple sessions
- Git branch integration
- Markdown documentation with progress tracking
- Session persistence and recovery

### Level 2 Todos (TodoWrite/TodoRead) 
- Real-time execution tracking within sessions
- JSON objects with status updates
- Immediate actionable steps
- Auto-completion detection

### Auto-Creation Triggers
Tasks automatically create when:
- Complexity: 6+ files, multi-step workflows, 30+ minute operations
- Risk level: Database changes, deployments, security operations
- Command patterns: Multiple targets, complex debugging scenarios

## Key Patterns for Development

### Evidence-Based Development
- Document all architectural decisions with rationale
- Provide metrics for performance claims
- Include testing evidence for quality improvements  
- Reference authoritative sources for implementations

### Token Optimization
- Use UltraCompressed mode (`--uc`) for complex projects
- Leverage @include templates for consistency
- Structured output: YAML > Tables > Lists > Prose
- Symbol substitution for common technical concepts

### Git Integration
- Commands integrate with Git workflow automatically
- Uncommitted changes trigger warnings before major operations
- Branch creation suggestions for feature work
- Atomic commits with standardized messages

### Error Recovery
- Checkpoint system for complex operations
- State restoration on session interruption  
- Graceful degradation when MCP servers unavailable
- Progressive fallback from external to native tools

## Troubleshooting

### Installation Issues
```bash
# Check installation
./install.sh --verify-checksums

# Reinstall if needed
./install.sh --force --backup

# Check permissions
ls -la ~/.claude/
```

### Command Issues
```bash
# Test basic functionality
/load
/analyze --code --think

# Test MCP integration (if servers installed)
/analyze --code --c7

# Test personas
/analyze --persona-architect
```

### Framework Debugging
```bash
# Enable introspection mode for framework troubleshooting
/troubleshoot --introspect

# Analyze framework patterns
/analyze --introspect --seq

# Optimize token usage
/improve --introspect --uc
```

## Contributing Guidelines

### Adding New Commands
1. Create command.md in `.claude/commands/`
2. Follow existing command structure pattern
3. Include universal flag inheritance: `@include shared/flag-inheritance.yml#Universal_Always`
4. Add command-specific flags and examples
5. Update command index and documentation

### Adding New Personas
1. Define persona in `.claude/shared/superclaude-personas.yml`
2. Include: identity, decision framework, risk profile, success metrics
3. Specify MCP preferences and problem-solving style
4. Add auto-activation triggers (file types, keywords)
5. Update persona flag inheritance system

### Pattern Development
1. Create reusable patterns in `.claude/commands/shared/`
2. Use @include reference system for consistency
3. Follow token optimization principles
4. Include validation and error handling
5. Document pattern usage and examples

This framework provides a sophisticated development environment that combines AI assistance with structured methodologies, specialized expertise, and token-efficient operations.