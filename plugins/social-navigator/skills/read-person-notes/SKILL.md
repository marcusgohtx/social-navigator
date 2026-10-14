---
name: read-person-notes
description: Retrieve and summarize what the user has recorded about a friend, including earlier conversations, shared context, and promises. Use for questions such as what do I know about Maya or what did I promise Theo. Answers in chat without changing notes.
---

# Read a person's notes

First follow [vault access](../../references/vault-access.md). Read the vault workflow's preparation and questions section for retrieval rules; this skill produces an answer, not a saved card.

Find the person from the user's request. Search names, known aliases, and links in Conversations and Context. Include relevant older notes, not just the most recent conversation. If two people share a name, resolve the identity before combining evidence. In demo mode, use only the explicitly selected fictional sources.

Read original notes behind useful context claims. Look for explicit rejections or corrections in the person's context page. Trace shared workplace or group claims to the person who supplied them. Preserve the difference between a friend's statement and the note author's impression.

Answer the actual question first. For a general overview, give a short recap, recent developments, and outstanding promises only where supported. Attach a source link and the date or date uncertainty to each remembered claim. For a promise, distinguish the original offer from evidence that it was fulfilled; an old promise is not automatically still outstanding.

If evidence conflicts, name the uncertainty and link the competing notes. Use an explicit later update as a timeline when the sources support that interpretation. Avoid a comprehensive personality profile or unsupported conclusions about feelings.

Finish with sources searched and any coverage limit in one short sentence. Say when nothing relevant was found. Do not create context pages, edit sources, or generate a card unless the user also requested that operation.
