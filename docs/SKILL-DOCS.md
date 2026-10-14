# Official skill documentation used

Checked 2026-10-11 against the live documentation. These notes concern packaging and invocation, not the effectiveness of the social guidance.

## OpenAI

- [Build skills](https://developers.openai.com/plugins/build/skills) describes SKILL.md files with names, descriptions, instructions, and optional resources. Skills may work without an MCP server. The five drafts use only file access supplied by the agent.
- [Package your plugin](https://developers.openai.com/plugins/build/plugins) now documents a portable root `plugin.json` with the Agent Plugins schema and automatic `skills/` discovery. It also documents the older `.codex-plugin/plugin.json` compatibility format. This draft uses the portable format, so it does not need that compatibility file or a `skills` field in its root manifest. Repository marketplace paths resolve from the repository root; the example catalog follows that convention.
- [Codex skill discovery](https://developers.openai.com/codex/skills) distinguishes local skills under `.agents/skills` from plugin distribution. Placing a SKILL.md anywhere in a repository does not itself register it. Our direct-file trial is distinct from installed skill discovery.

## Anthropic

- [Extend Claude with skills](https://code.claude.com/docs/en/skills) documents YAML frontmatter, descriptions for selection, supporting resources, and manual invocation. The drafts use the shared `name` and `description` fields and leave ordinary model selection enabled. They avoid vendor-specific shell interpolation or delegation fields.
- [Plugin manifest reference](https://code.claude.com/docs/en/plugins-reference) documents `.claude-plugin/plugin.json` and the default `skills/` directory. The Claude manifest has the same name and version as the portable manifest, with no custom skill paths.
- [Create a plugin](https://code.claude.com/docs/en/plugins/create) documents `claude plugin validate`, session loading with `--plugin-dir`, and commands such as `/plugin-name:skill-name`. The README uses that local development route without installing globally.

## Implementation judgment and limits

The skills separate retrieval, question drafting, card creation, context maintenance, and source capture because those are distinct user requests. That separation is a product choice. Vendor documentation does not validate the question guide or guarantee that agents obey its instructions.

The plugin expects a selected Social Navigator vault and delegates storage conventions to that vault's instructions. Installing it into a cloud chat does not grant access to a local folder. No Obsidian community plugin, MCP server, or automatic watcher is included.

Validation results are recorded in [SKILL-TRIALS.md](SKILL-TRIALS.md). Published documentation can be newer than an installed agent. Check actual loading separately; do not infer compatibility from a valid manifest alone.
