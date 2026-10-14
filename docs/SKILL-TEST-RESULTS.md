# Fictional skill test results

Tested on 2026-10-11 using GPT 6.1 sol sub-agents for generation and independent evaluation. The final package version is 0.1.1.

The tested requests produced source-grounded answers, two usable questions, and a preparation card. Capture and context maintenance also passed the evaluator's review. Two presentation issues in the initial run were fixed and passed a fresh generation retest.

## Inspect the actual outputs

- [Generated questions and response transcript](../Examples/Skill%20trials/2026-10-11%20answers.md).
- [Generated preparation card for Maya](../Examples/Prep/2026-10-12%20Maya%20coffee%20-%20tested%20skills.md).

These are the fresh retest outputs, copied without rewriting the prose. Only relative link targets were rebased for their archived locations. The original hand-written example card remains a separate file.

## Method

Two isolated vaults received copies of the instructions, skills, templates, and three fictional raw notes. The generation vault received no existing AI context or example card. A GPT 6.1 sol producer read the skill files directly and completed these requests in order:

1. "Use only Examples/Conversations. What did I promise Maya?"
2. "Use only Examples/Conversations. Give me two thoughtful questions for coffee with Maya."
3. "Use only Examples/Conversations. Prepare a fictional Maya coffee card for October 12, 2026, and save it."

A second GPT 6.1 sol agent refreshed context in a separate fictional vault, captured the exact sentence "Maya might run the workshop next month, I can't remember.", then refreshed context from that new source.

An independent GPT 6.1 sol evaluator read the raw sources, applicable instructions, and resulting files. It had not seen the prewritten example card or a desired answer. It reviewed the maintenance artifacts without relying on the maintenance agent's self-assessment.

## Results by skill

| Skill | Observed result |
| --- | --- |
| Read person notes | Identified the cafe-name promise, cited the October 3 note, and distinguished its dated unsent status from unknown current fulfillment |
| Thoughtful questions | Offered a workshop update and a hobby question with supported premises, without invented feelings or private secondhand information |
| Prepare meeting | Saved a clearly fictional, dated card below 250 words excluding sources, with reminders, questions, and supported follow-ups |
| Capture reflection | Preserved the supplied sentence exactly, including uncertainty; labeled it existing knowledge without inventing a conversation date |
| Refresh context | Kept derived details as candidates, attributed differing dates, and kept Theo's confidence out of Maya's page and shared workplace context |

The newer uncertain workshop recollection did not overwrite the earlier booking or become a confirmed reschedule. The original fixture notes remained byte-for-byte unchanged, and the captured account matched the supplied text exactly. All 39 context-page links resolved in the maintenance trial.

## Fix and retest

The initial content passed, but the saved response transcript had three source links relative to the wrong directory. Its card-completion response also used a plain path rather than a clickable link. The evaluator treated these as concrete delivery problems, not evidence that the substantive question guidance was wrong.

Updated shared completion guidance now distinguishes chat links from links inside saved Markdown and requires link checks after saving or relocation. The preparation skill explicitly requires a clickable card link. Both plugin manifests were bumped from 0.1.0 to 0.1.1.

A fresh GPT 6.1 sol producer received an empty output vault with the updated instructions and the same raw notes and requests. The independent evaluator passed both fixes and found no new concrete content defect. All seven transcript links and seven card links resolved. The card had 187 visible words excluding its Sources section under the evaluator's counting method. The two question wordings varied between runs; both sets were supported by the notes.

The evaluator noted an optional wording improvement: add "If still needed" before the cafe-message action. The surrounding card already says current completion is unknown. We retained the agent's generated wording rather than adding a new rule for that stylistic preference.

## Limits

This is a small behavioral trial of explicitly loaded skill instructions, not a statistical quality benchmark. It does not verify automatic skill selection, installed plugin loading in Codex or Claude Code, Obsidian navigation, or future repeatability. The maintenance fixture had no approved memories or saved cards to invalidate; rejection handling, source deletion, stale-card updates, concurrent edits, and ambiguous identities remain separate trial cases.

No real friend notes, external services, or global plugin settings were used. The complete local trial artifacts remain under the parent project's ignored `.local/skill-trials/2026-10-11/` directory for inspection on the authoring device. Only the fictional retest outputs are archived here for distribution.
