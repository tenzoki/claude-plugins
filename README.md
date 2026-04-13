# tenzoki claude plugins

A collection of Claude Code plugins for AI agent orchestration, writing, and style analysis.

## Quick start

Add the marketplace and install a plugin — two commands, done.

```bash
# In Claude Code, add the marketplace
/plugin marketplace add tenzoki/claude-plugins

# Install a plugin
/plugin install fusion@tenzoki-plugins
/plugin install stilwerk@tenzoki-plugins
```

## Available plugins

| Plugin | Description |
|--------|-------------|
| [**fusion**](https://github.com/tenzoki/fusion) | AI agent orchestration framework with 12 specialized agents, compliance guard, churn detection, and live monitoring. |
| [**stilwerk**](https://github.com/tenzoki/stilwerk) | Style analysis, authorship attribution, and text transformation. Combines quantitative stylometry with AI-assisted qualitative analysis. |

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview) v2.0.12 or higher
- Node.js 18+ (for fusion's TypeScript hooks)
- Python 3.10+ (for stilwerk's CLI tools, fusion's monitor)

## Installing plugins

After adding the marketplace, you can browse available plugins:

```bash
# See what's available
/plugin

# Install by name
/plugin install stilwerk@tenzoki-plugins

# Verify installation
/help
```

Stilwerk's commands will show up as `/stilwerk:analyze`, `/stilwerk:transform`, etc.

## Updating

Claude Code checks for marketplace updates automatically. To force an update:

```bash
/plugin marketplace update tenzoki-plugins
```

## Removing

```bash
# Remove a plugin
/plugin uninstall stilwerk@tenzoki-plugins

# Remove the entire marketplace
/plugin marketplace remove tenzoki-plugins
```

## Plugin development

Each plugin follows the standard Claude Code plugin structure:

```
plugin-name/
├── .claude-plugin/
│   └── plugin.json      # Plugin manifest (required)
├── commands/             # Slash commands
├── skills/               # Agent skills
├── agents/               # Subagent definitions
├── hooks/                # Event handlers
└── README.md
```

For details on building plugins, see the [official plugin docs](https://code.claude.com/docs/en/plugins).

## License

See each plugin's directory for its respective license.