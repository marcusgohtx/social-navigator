# Agent workflows

## Refresh context

1. Read the source notes in `Conversations`. Plain prose, missing frontmatter, approximate dates, and multiple people per note are valid. Separate when the note was written from when an event occurred. If the collection is too large to read fully, search it and disclose which files you read and the coverage limit.
2. Match people and shared entities against existing context pages. Read source links already on those pages, including older relevant notes. Use a distinguishing name in filenames when needed, such as `Alex Tan - climbing`. Resolve ambiguous identities with the user.
3. Update one page per person in `Context/People` and one per useful shared entity in `Context/Shared`. Use the [context template](../Templates/Context%20note.md). Include only details that may help future conversation preparation. A page about a workplace should link the people who mentioned it and attribute each account. Keep an individual's private concerns on their own page.
4. Put new or materially changed extractions under **Candidates** with source links. Keep **Approved**, **Rejected**, and **User annotations** separate. Preserve explicit decisions. Do not repeatedly propose unchanged rejected candidates. Approval survives only while the supporting evidence and meaning are unchanged.
5. Record the refresh date and the sources read. Check existing cards and context for references to changed or missing source material. Apply the corrections workflow when affected. Report the changed files and unresolved conflicts.

## Preparation and questions

1. Identify the person and meeting purpose from the request. If the date is absent, use the current date for the filename and state that the meeting date is unspecified. Do not block a casual preparation request on optional details. Ask when the person's identity is genuinely ambiguous.
2. Search raw notes for the person's name, known nicknames, linked people, and shared entities. Use context pages as an index, then read the relevant original notes. Look for changes and conflicts across dates. Do not rely on a context page, approval, or old card without checking sources again. Report limited coverage if you cannot read all relevant notes.
3. Select two or three useful reminders and at most two natural questions. Questions are suggestions, not remembered facts. Cite the evidence behind a specific premise. Include an optional thing the user could share or follow up on only when supported. Keep missing information explicit; with no relevant notes, use generic, clearly labeled questions.
4. For a question-only request, answer in chat with source links. Write files only if requested or needed for a requested refresh. For a card, use the [card template](../Templates/Preparation%20card.md), aim for under 250 words excluding sources, and save it under `Prep/YYYY-MM-DD Person occasion.md`. Avoid filename characters forbidden on Windows. If the filename exists, add `-2`, `-3`, and so on. Never silently replace a previous card.
5. Label the card as a snapshot checked on the generation date. List all raw sources used and link any prior card it replaces. State uncertainty and unresolved conflicts compactly. Omit disputed premises from suggested questions. Mark a previous card superseded only when a replacement has actually been saved, preserving user annotations.
6. Link the saved card in the response. Explain any important missing source or conflict. The user can read the Markdown directly in Obsidian.

## Corrections, conflicts, and forgetting

When the user edits a source note, use the current wording. Inspect context and cards for that source path and the affected claim. If you cannot tell which claim changed, treat every derived claim citing that note as needing review. Move affected approved memories back to candidates and mark affected cards **Out of date: source changed; refresh before use**. Do this during the requested operation; there is no watcher that catches edits automatically.

If a source disappeared or moved, search for the note before declaring it missing. Repair links only when the match is clear. Remove unsupported details from active context and mark dependent cards out of date. Do not reconstruct deleted facts from an old summary as though they still had evidence.

Distinguish a later life update from a correction. An explicit statement such as "I left Harbour in September" can describe a timeline. If two statements appear incompatible and the notes do not explain why, show both dates and links, ask a concise clarification, and omit the disputed claim from preparation. Continue with unrelated material.

Approving a memory means user acceptance, not independent verification. When the user rejects a candidate, record the decision and reason if given. Exclude that claim from preparation, including re-extraction from the same raw source, until the user changes the decision or clarifies that only its phrasing was wrong. If a claim was marked mistaken, do not use it through the direct-source rule.

When the user asks to forget a detail, remove it from derived context and saved cards within the authorized scope, including indirect paraphrases. Locate raw occurrences and tell the user whether they remain; edit raw notes only if their request authorizes that. Do not retain the forgotten detail in a rejection log. Explain that external chat history, backups, and provider storage are outside this vault operation.

Before rewriting an existing file, reread its current contents. Preserve user annotations and avoid overwriting edits made during your task. If concurrent edits make the intended change unclear, save a separate proposal and identify the conflict.
