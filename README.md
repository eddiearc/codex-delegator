# Codex Delegator - Claude Code Agent Skill

> Enables Claude Code to automatically delegate complex tasks to OpenAI Codex CLI for AI-to-AI collaboration

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## What is This?

**Codex Delegator** is a **Claude Code Agent Skill** - a specialized module that extends Claude Code with the ability to automatically delegate complex, logic-intensive programming tasks to OpenAI's Codex CLI.

Think of it as giving Claude Code a specialized co-worker (Codex) for handling particularly challenging problems.

## What It Does

When you're working with Claude Code and encounter:
- 🔧 Complex backend logic implementations
- 🧮 Intricate algorithm optimizations
- 🐛 Persistent bugs that resist multiple fix attempts
- 🔄 Race conditions and concurrency issues
- 💡 Problems needing a fresh perspective

Claude Code can automatically invoke Codex to provide alternative solutions, leveraging the strengths of both AI systems.

## How It Works

```
You: "This payment processing bug keeps happening under high load,
     I've tried 3 different fixes"

  ↓

Claude Code: [Analyzes problem, recognizes delegation criteria]
"I'm going to use Codex to help debug this race condition..."

  ↓

Codex: [Analyzes with fresh perspective, generates solution]

  ↓

Claude Code: [Validates solution, runs tests, integrates]
"Here's the fix. The issue was a race condition in Redis cache updates..."
```

## Installation

### Prerequisites

1. **Claude Code** - Install from [claude.com/claude-code](https://claude.com/claude-code)
2. **OpenAI Codex CLI** - Install globally:
   ```bash
   npm i -g @openai/codex
   ```
3. **Authentication** - ChatGPT Plus/Pro/Business/Enterprise account OR OpenAI API key:
   ```bash
   codex auth
   ```

### Install the Skill

**Option 1: Download and Extract**
1. Download `codex-delegator.zip`
2. Extract to `~/.claude/skills/codex-delegator`
3. Restart Claude Code

**Option 2: Git Clone** (if developing)
```bash
cd ~/.claude/skills
git clone https://github.com/your-org/codex-delegator.git
```

## Usage Examples

### Example 1: Persistent Bug

```
You: "This race condition in my payment system has been
     failing 5% of transactions. I've tried adding
     transactions, increasing Redis TTL, and retry logic."

Claude Code: "I'm delegating this to Codex for a fresh
             analysis of the race condition..."

[Codex analyzes and fixes]

Claude Code: "Found the issue - your webhook handler and
             order service were competing for cache locks.
             Here's the fix using distributed locking..."
```

### Example 2: Algorithm Optimization

```
You: "My recommendation engine is too slow - 30 seconds
     for 10k items. Need to handle 100k+ items."

Claude Code: "This is a complex optimization problem.
             Using Codex to explore algorithmic improvements..."

[Codex optimizes]

Claude Code: "Reduced complexity from O(n²) to O(n log n)
             using spatial indexing. Now processes 100k
             items in under 1 second."
```

## Configuration

The skill uses intelligent decision-making to determine when delegation is beneficial. It automatically delegates when:

- ✅ Problem attempted 2+ times without resolution
- ✅ High logic complexity (nested conditions, complex state)
- ✅ Backend/algorithm heavy tasks
- ✅ Need for different problem-solving approach

## What's Inside?

```
codex-delegator/
├── SKILL.md                      # Main skill documentation
├── references/
│   └── execution_strategies.md   # Detailed Codex usage patterns
└── README.md                     # This file
```

## Requirements

- **Claude Code**: Latest version recommended
- **Codex CLI**: v0.58.0+
- **Node.js**: For Codex CLI installation
- **Git repository**: Codex works best in version-controlled projects
- **OpenAI Account**: ChatGPT Plus/Pro/Business/Enterprise OR API key

## Limitations

This skill is designed for complex problems. It's **not** used for:
- Simple CRUD operations
- Basic UI components
- Straightforward bug fixes (first attempt)
- Simple configuration changes
- General coding questions

## About Agent Skills

Agent skills are modular packages that extend Claude Code with specialized capabilities. They work by:

1. **Providing specialized knowledge** - Domain-specific workflows and best practices
2. **Tool integration** - Connecting Claude Code with external tools (like Codex)
3. **Automated decision-making** - Knowing when to apply specialized capabilities

Learn more about creating agent skills: [Claude Code Documentation](https://docs.anthropic.com/claude-code/skills)

## Contributing

Contributions welcome! This skill can be improved with:
- Additional delegation strategies
- More example scenarios
- Better decision-making criteria
- Performance optimizations

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built for [Claude Code](https://claude.com/claude-code) by Anthropic
- Uses [OpenAI Codex CLI](https://github.com/openai/codex)
- Inspired by the idea of AI collaboration and specialization

## Support

- 📖 [Documentation](./SKILL.md)
- 🐛 [Report Issues](https://github.com/your-org/codex-delegator/issues)
- 💬 [Discussions](https://github.com/your-org/codex-delegator/discussions)

---

**Made with ❤️ for the Claude Code community**
