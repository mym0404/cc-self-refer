<div align="center">
  <img src="assets/logo.svg" alt="cc-self-refer" width="100%" max-width="800px" />
</div>

# cc-self-refer

**Claude Code Self-Reference Helper** - The missing backend for intelligent development workflows with AI assistance.

## What is cc-self-refer?

`cc-self-refer` is a high-performance Node.js CLI that powers Claude Code's self-referential development capabilities. It enables projects to maintain their own context, specification repository, and development patterns that Claude can reference and build upon across sessions.

## Why do you need this?

### The Problem

- **Context Loss**: AI conversations lose context between sessions
- **Repeated Explanations**: You constantly re-explain project architecture, decisions, and patterns
- **Specifications Scattered**: Technical specifications, code patterns, and planning documents are spread across different tools
- **Inefficient Workflows**: No systematic way to build and reference project-specific specifications

### The Solution

`cc-self-refer` creates a **persistent, searchable specification layer** for your projects that Claude Code can intelligently reference:

- 📋 **Strategic Plans**: Document and iterate on high-level project planning
- 📄 **Session History**: Preserve development context across Claude sessions
- 🧩 **Code Patterns**: Build a library of reusable, project-specific code templates
- 📋 **Technical Specifications**: Maintain system requirements, constraints, and architectural decisions
- 🔍 **Intelligent Search**: Find relevant information instantly with semantic search

## Quick Setup

### 1. Run Initialization Commands

```shell
# Download commands & other stuffs for self refer structure
npx -y cc-self-refer init-setup-project
```

### 2. Run your **claude-code** in your project root and pass this prompt.

```shell
The following commands will print the prompt out for setting up claude code self referring context management system.

Run `npx -y cc-self-refer init-get-prompt` and follow instructions step by step.
```

That's it! Your project now has intelligent self-reference capabilities.

## What Gets Created

After running `/init-claude`, your project will have:

```
your-project/
├── CLAUDE.md              # 📜 Project Overview for Claude and command usages (merged if exists)
├── .claude/
│   ├── commands/           # 🎯 Claude Code Commands
│   │   ├── plan-create.md # Create strategic plans
│   │   ├── plan-edit.md   # Edit existing plans
│   │   ├── plan-resolve.md# View and load plans
│   │   ├── page-save.md   # Session management
│   │   ├── page-refer.md  # Load session context
│   │   ├── spec-refer.md # Access technical specifications
│   │   ├── spec.md # Interactive specification planning
│   │   ├── pattern-use.md # Apply code patterns
│   │   └── pattern-create.md     # Save new patterns
│   │
│   ├── plans/             # 📋 Strategic Plans & Architecture
│   │   └── [numbered plans like: 001-user-authentication.md]
│   │
│   ├── pages/             # 📄 Session History & Context
│   │   └── [numbered sessions like: 001-login-implementation.md]
│   │
│   ├── patterns/     # 🧩 Reusable Code Templates
│   │   └── [numbered patterns like: 001-react-hook.md]
│   │
│   └── specs/         # 📋 Technical Specification Repository
│       └── [numbered entries like: 001-api-limits.md]
└── [your project files]
```

## How Each Directory Works

### 📋 `.claude/plans/` - Strategic Planning

- **Purpose**: High-level project planning and architecture decisions
- **Usage**:
  - `/plan-create "Feature Name" "Description"` creates comprehensive planning documents
  - `/plan-edit "id|keyword" "modifications"` modifies existing plans
  - `/plan-resolve "id|keyword"` views and loads plans for reference
- **Content**: Implementation phases, success criteria, technical decisions, risk assessment
- **AI Benefit**: Claude references these plans to understand project direction and constraints

### 📄 `.claude/pages/` - Session Context

- **Purpose**: Preserve development context between Claude sessions
- **Usage**: Automatically captures session state; `/page-refer` to load previous context
- **Content**: Code changes, decisions made, problems solved, next steps
- **AI Benefit**: Eliminates need to re-explain project status each session

### 🧩 `.claude/patterns/` - Reusable Templates

- **Purpose**: Project-specific code patterns and templates
- **Usage**: `/pattern-create` to save patterns; `/pattern-use` to apply them
- **Content**: Component templates, utility functions, configuration patterns
- **AI Benefit**: Claude can apply your established patterns instead of generic solutions

### 📋 `.claude/specs/` - Technical Specifications

- **Purpose**: System requirements, technical specifications, and architectural constraints
- **Usage**: `/spec-refer` to access; `/spec` for interactive specification planning; manually curated technical specifications
- **Content**: Technical requirements, API specifications, performance requirements, compliance needs
- **AI Benefit**: Claude makes technically sound decisions aligned with your specifications

## Why This Works

Each directory serves a specific purpose in building **persistent AI context**:

1. **Plans** provide strategic direction
2. **Pages** maintain session continuity
3. **Patterns** ensure consistency
4. **Specifications** guide decision-making

The result: Claude becomes increasingly intelligent about your specific project over time.

---

## Todo

- Enhance search algorithm
- Spec Feature (drop knowledge)
- Each component can refer others
- Test
- Docs
- Guide files on init

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for development setup and contribution guidelines.

## License

MIT © 2025 MJ Studio
