# Skills for Social Navigator

Drafted 2026-10-11. The first bundle covers the complete note-to-meeting loop.

| Skill | Example request | Result |
| --- | --- | --- |
| [Read person notes](../plugins/social-navigator/skills/read-person-notes/SKILL.md) | "What did I promise Maya?" | A source-linked answer in chat |
| [Thoughtful questions](../plugins/social-navigator/skills/thoughtful-questions/SKILL.md) | "What could I ask Maya that shows I remember what matters to her?" | Two natural questions with reasons and sources |
| [Prepare meeting](../plugins/social-navigator/skills/prepare-meeting/SKILL.md) | "Prepare me for coffee with Maya next Monday." | A short card saved in Prep |
| [Refresh context](../plugins/social-navigator/skills/refresh-context/SKILL.md) | "Update what we know from the new conversation notes." | Updated people and shared-context pages |
| [Capture reflection](../plugins/social-navigator/skills/capture-reflection/SKILL.md) | "Save this rough account of lunch with Theo." | A new source note preserving the user's account |

The first two skills work independently for a quick question. Prepare meeting uses their procedures to produce a card. Context refresh and note capture write only what the user requested.

## What makes a question useful

For this prototype, a useful question can show that you remembered, invite a story, help someone celebrate, or offer support. The [question guide](../plugins/social-navigator/skills/thoughtful-questions/references/question-guide.md) includes sample wording and common mistakes. These are drafting principles, not a claim that a skill can guarantee closeness or improve mental health.

For the fictional Maya notes, candidates include:

- "How's the workshop preparation going?" It follows up on something she mentioned.
- "What would you like people to take away from the workshop?" It invites her perspective without assuming how she feels.

Both premises come from the [coffee note](../Examples/Conversations/2026-10-03%20Maya%20coffee.md). A different meeting or a new note may call for different questions. Questions about a disputed moving month or Theo's confidence are excluded.

## Try the drafts without installation

Open this vault as the agent's project and send:

> Use only Examples/Conversations. Suggest two questions for my fictional coffee with Maya. Answer in chat.

Codex reads the vault's AGENTS.md as project instructions; Claude Code reads CLAUDE.md, which imports it. Those instructions point to the matching skill file. You do not need to name the instruction files in your request. Open this vault as the project so the host can find them. This direct routing does not require plugin installation. Installed-plugin discovery and automatic skill selection still need separate validation.

Host behavior checked against [OpenAI's project instruction guide](https://developers.openai.com/codex/guides/agents-md) and [Anthropic's memory and imports guide](https://code.claude.com/docs/en/memory), 2026-10-14.

Recent Claude Code versions can also read AGENTS.md directly. The one-line CLAUDE.md import remains for older versions and sessions where that support is unavailable; it contains no duplicate guide for the user to read.

## Plugin packaging

The package is [plugins/social-navigator](../plugins/social-navigator/README.md). Its OpenAI portable manifest and Claude Code manifest reference the same default `skills/` layout. Shared supporting content lives inside the package. The vault and its personal notes remain separate from an installed plugin's cache.

For a Claude Code session started from this vault:

```sh
claude --plugin-dir ./plugins/social-navigator
```

Then use a command such as:

```text
/social-navigator:prepare-meeting Use only Examples/Conversations. Prepare a fictional Maya coffee card for 2026-10-12.
```

For Codex desktop, the [example marketplace file](codex-marketplace.example.json) points at the plugin. For a fresh vault without an existing catalog, copy it to `.agents/plugins/marketplace.json` relative to the vault root, then restart the app and check the plugin listing. If that file already exists, merge the plugin entry instead of replacing the catalog. This draft has not changed your installed plugins or user settings. A skills folder under `plugins/` alone is not the normal `.agents/skills` discovery location.

The current [OpenAI packaging guide](https://developers.openai.com/plugins/build/plugins) documents portable manifests and repository marketplaces. Anthropic documents [local plugin loading and namespaced skill commands](https://code.claude.com/docs/en/plugins/create). See [documentation notes](SKILL-DOCS.md) for the dated source record and compatibility limits.

## Additional content to consider after the trial

- A follow-through skill could find promises and draft a short check-in for the user to review. Sending would require a separate explicit request.
- A reconnecting guide could offer low-pressure openings after a long gap, with no assumption that the friend is upset.
- A repair-conversation guide could help the user acknowledge a specific mistake and hear the other person's account, without assigning motives.
- A preferences note could record the user's preferred card length, tone, and topics they want to avoid. Keep personal preferences in the private vault rather than public skill files.

These are proposals, not installed or drafted skills. Try the five core skills before adding more commands.

## Validation

Run the [skill trial cases](SKILL-TRIALS.md) against the fictional notes. Structural checks cover frontmatter, manifests, and file references. Behavioral quality, automatic selection, and tool-specific discovery require separate trials.

The first [GPT 6.1 sol behavioral trial](SKILL-TEST-RESULTS.md) is complete. It exercised all five skills with independent evaluation and a fresh retest after link fixes. Automatic selection and installed-plugin discovery remain unverified.
