---
name: prepare-meeting
description: Prepare and save a short sourced card before a catch-up with a friend, with remembered context, possible questions, and a supported follow-up. Use when the user asks to prepare for a meeting or create a preparation card.
---

# Prepare a meeting card

Follow [vault access](../../references/vault-access.md). Read the vault workflow's preparation and questions section and its preparation-card template. A preparation request authorizes saving a card in the selected vault's Prep folder.

Use [read-person-notes](../read-person-notes/SKILL.md) to retrieve current source evidence, keeping the intermediate recap brief. Use [thoughtful-questions](../thoughtful-questions/SKILL.md) to choose up to two questions. Read those files as procedures if the host cannot invoke another skill directly; do not spawn agents or require a particular vendor tool.

Use the meeting date and occasion from the request. If the date is unknown, label it unspecified and use today's date only for the filename and preparation date. Do not invent a meeting date. Resolve an ambiguous person, but proceed without optional meeting details.

Save a card under 250 words excluding sources. Include two or three useful reminders if evidence supports them, up to two questions, and an optional thing to share or follow up on. Missing sections may be omitted. Every specific factual premise must link to an original note. Keep uncertainty compact, and omit disputed or private premises from questions.

Use a fresh filename when a card already exists. Preserve user annotations and label the new card as a dated snapshot. A requested demo must be clearly fictional and use only its designated sources. Follow the vault's corrections workflow for affected old cards when a source change becomes apparent.

Check that each source link resolves from the saved card. Return a clickable Markdown link to the saved card, source coverage, and any material gap. If saving failed, provide the draft and clearly state that no card was saved.
