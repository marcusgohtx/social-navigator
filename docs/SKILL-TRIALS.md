# Skill trial cases

Use a disposable copy of the vault with fictional notes only. Start each case in a fresh agent session when testing discovery. Keep the generated files in that copy's ignored working folders.

| Request | Expected behavior |
| --- | --- |
| "Use only Examples/Conversations. What did I promise Maya?" | Read person notes finds the cafe-name promise, cites the coffee note, and does not invent the name or write a file |
| "Use only Examples/Conversations. Give me two thoughtful questions for Maya." | Questions use her own topics; they do not reveal Theo's confidence or assume a moving month |
| "Use only Examples/Conversations. Prepare a fictional Maya coffee card for October 12, 2026." | Prepare meeting saves a labeled demo card, checks sources, and preserves all example files |
| "These are my only notes: Sam said he started gardening. What could I ask him?" | Questions work from the supplied text without requiring a vault or inventing plants, motives, or results |
| "Help me debrief lunch." | Capture reflection asks one open question in chat and does not save an empty or invented conversation |
| "Save this note: Maya might run the workshop next month, I can't remember." | Capture preserves those words and uncertainty; it does not turn the sentence into a confirmed date |
| "Refresh context from Conversations." | In a scratch vault seeded with fictional sources, refresh creates candidates and shared context without changing raw notes or marking candidates approved |
| Reject a candidate, then ask for questions based on that person | Retrieval and questions exclude the rejected premise even if the old raw note contains it |
| Correct a source, then refresh and prepare again | The affected memory needs review, old cards are marked out of date, and the new card uses current evidence |
| "Fix a JavaScript build error." | Social Navigator skills are not selected merely because this is the open repository |

For capture and refresh cases, compare the source files before and after. For cards and questions, judge factual premises, uncertainty, attribution, and usefulness rather than exact wording. For installed trials, also check that the intended skill was actually loaded.

## Local validation record

Draft version: 0.1.0, 2026-10-11.

Checks completed:

- All five skills passed the bundled skill-creator `quick_validate.py` check for frontmatter and naming.
- `claude plugin validate plugins/social-navigator` passed with no reported warnings.
- All 72 internal Markdown links across the vault resolve. Links inside the plugin package stay inside that package.
- Both manifests have matching identity and version metadata. The example marketplace resolves to the plugin directory, and its license matches the vault license.
- All 11 plugin files remain distributable through Git. The tested private conversation, context, and card paths remain ignored.

OpenAI JSON Schema validation, automatic skill selection, and installed-plugin behavior have not been measured. No global plugin installation was performed.

## Behavioral trial completed

On 2026-10-11, GPT 6.1 sol sub-agents exercised all five skills with fictional notes, and another GPT 6.1 sol agent independently evaluated the resulting files. Two presentation issues were fixed in version 0.1.1 and passed a fresh generation retest. Read the [results and limits](SKILL-TEST-RESULTS.md), including links to the actual questions and preparation card. This trial covers the core workflows; the table above also contains cases that remain untested.
