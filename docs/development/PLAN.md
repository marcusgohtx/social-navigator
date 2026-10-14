# Social Navigator prototype plan

Selected direction: 2026-10-10. Local prototype, ready for a personal trial.

Updated 2026-10-11 with [five draft skills and a plugin package](../SKILLS.md), using current OpenAI and Anthropic documentation. The skills cover person-note retrieval, thoughtful questions, preparation cards, context refresh, and reflection capture. Skill frontmatter, Claude's manifest validator, and internal-link checks passed. A [GPT 6.1 sol behavioral trial](../SKILL-TEST-RESULTS.md) passed independent review after two presentation fixes and a fresh retest. Installed-host trials remain outstanding.

## The question

Can a folder of rough Markdown notes and a file-capable AI agent produce a useful preparation card without requiring the user to maintain a structured database?

The user writes in Obsidian. Their agent reads the same files on request, maintains source-linked context, answers questions, and saves short preparation cards. The downloadable repository supplies the folder structure, instructions, templates, and fictional examples.

## The everyday loop

1. Start with what you already know about a friend in `Conversations`. This is a person note; its written date is not an invented conversation date.
2. Add a new raw conversation reflection after each catch-up. Optional prompts help, but names in ordinary prose and approximate dates are enough.
3. Ask the agent to refresh context. It updates people and shared-context pages, preserving links, attribution, uncertainty, and user annotations.
4. Before a meeting, ask for a preparation card. The agent checks the original notes and saves reminders, up to two questions, and an optional contribution. Ask follow-up questions in chat whenever useful.
5. After meeting, add a note about what happened. If a card helped or got something wrong, record that too.

Obsidian is the editor and navigator. The agent is the processor. Markdown files are the storage and output. There is no scheduler or background indexing in this prototype.

## Scope of the first version

Implemented in this prototype:

- Portable vault folders with empty personal working areas.
- Plain-language agent instructions plus a Claude Code import of the same instructions.
- Templates for existing knowledge, conversation reflections, AI context, and preparation cards.
- A fictional worked example with two friends, a shared workplace, a conflicting date, an unknown detail, and a confidence that must stay out of the other friend's card.
- Workflows for retrieval, refresh, approval, rejection, corrections, missing sources, and forgetting.
- Git exclusions for personal working folders and a license for free distribution.
- Five SKILL.md workflows, a question guide, shared vault-access instructions, portable OpenAI and Claude Code plugin manifests, and fictional skill trial cases.

Deliberately deferred: listening, live coaching, message import, embeddings, a database, automatic agents, and custom AI authentication. Add something only if the plain-file trial exposes a need. The user's existing agent supplies model access; this project does not promise free model usage.

## Source and memory decisions

Raw notes remain the user's record. AI writes to separate context and card folders. Earlier discussions required user review of derived memories; retain that rule through Candidates, Approved, and Rejected sections. A card can be prepared immediately from the raw notes, with source checks, without a separate approval session.

The agent may reorganize derived context during a requested refresh, but it preserves user annotations and decisions. Shared context attributes each person's account and does not distribute private information between people. Unknown dates and conflicting claims remain visible. A later note does not automatically win a conflict.

Freshness is procedural. The agent checks sources on every preparation request and marks affected old cards when it encounters changes. There is no automatic source-change detector, deletion monitor, or enforced provenance engine. Cards state when they were prepared and should be refreshed before reuse. This limitation is acceptable for a small first vault; evaluate it in the trial.

## Milestones

| Stage | Work | Completion criterion |
| --- | --- | --- |
| 1. Portable prototype | Build the vault, instructions, templates, worked example, and distribution files | Copy the folder elsewhere and follow its links without this parent project |
| 2. Agent and Obsidian trial | Run the fictional prompt in fresh Codex and Claude Code sessions; open output in Obsidian | Both agents save readable, sourced cards; original notes are unchanged; no fictional/personal mixing |
| 3. Three real catch-ups | Use a private copy with two or three friends | Record useful suggestions, errors, note-taking effort, and whether preparation was worth doing |
| 4. Public template | Review only distributable files and publish the standalone folder to GitHub | Fresh download opens as a vault, contains no real notes, and documents tested tools |

This standalone folder is the public prototype repository. Its distribution contains empty personal folders and fictional examples. The parent workspace contains an older experiment and local runtime data and is outside the public repository.

## How to evaluate it

Use [Try it](../TRY%20IT.md) for the fictional and edge-case checks. Then, after each real catch-up, jot down whether you used a suggestion, what helped, and what felt wrong or awkward. Optionally rate awkwardness, satisfaction, and feeling uplifted separately from 1 to 5. These are personal usefulness signals, not evidence of a clinical effect.

Pay attention to retrieval misses, incorrect identities, stale reminders, unwanted disclosure across friends, and time spent managing files. If the first trial works, improve the smallest recurring friction. If it does not, revise the card and note workflow before adding infrastructure.

## Provenance

This plan adopts the Markdown and Obsidian direction requested on 2026-10-10. It carries forward earlier discussions about source preservation, approved memories, uncertainty, and short preparation cards. It replaces the earlier browser-app implementation plan. The old experiment stays in the parent project for reference and is not a dependency of this folder.


## Website demo, 2026-10-14

The public landing page now demonstrates a fixed fictional note-to-prep flow in the browser. It has no LLM, personal input, or backend storage. The output folder is Prep. START_HERE.md is the single human quickstart; agent instructions load through their host conventions. The prior GPT 6.1 sol trial used package v0.1.1; this UI and folder rename do not constitute a new model trial.
