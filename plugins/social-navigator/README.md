# Social Navigator plugin draft

Five skills for a local Social Navigator Markdown vault. Version 0.1.1, updated 2026-10-11 after a GPT 6.1 sol behavioral trial.

- `read-person-notes` answers questions from source notes.
- `thoughtful-questions` suggests natural, considerate questions.
- `prepare-meeting` saves a short preparation card.
- `refresh-context` maintains people and shared-context notes.
- `capture-reflection` helps record a conversation or existing knowledge.

The plugin uses the host agent's file tools. Open your Social Navigator vault as the project, or give its path. The vault supplies `AGENTS.md`, `docs/WORKFLOWS.md`, and templates. This package alone does not create a vault or connect to files in a cloud chat.

`plugin.json` supplies the portable OpenAI package manifest. `.claude-plugin/plugin.json` supplies the Claude Code manifest. Both use the same `skills/` folders and shared references. No MCP servers, hooks, credentials, background processes, or private notes are bundled.

For Claude Code, run from your vault:

```sh
claude --plugin-dir ./plugins/social-navigator
```

Then try `/social-navigator:thoughtful-questions` followed by your request. If the plugin was copied elsewhere, pass its actual location instead. For OpenAI local discovery, register this plugin directory in a repository marketplace as described in the official packaging documentation.

Skill and manifest checks are structural validation, not a guarantee of good suggestions. Run the fictional behavior cases from the vault's plugin guide before using real notes. Keep this folder free of personal information when distributing it. See [LICENSE](LICENSE).
