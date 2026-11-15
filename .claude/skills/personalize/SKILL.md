---
name: personalize
description: Write a version of each campaign email for every lead group in leads/leads.csv. Use when a campaign's emails are final and you want one copy per group.
argument-hint: "[campaign folder]"
context: fork
allowed-tools: Read, Glob, Grep, Write
---

# Personalize campaign emails per lead group

Campaign folder: $ARGUMENTS

## 1. Check the input

If no campaign folder was given (the line above is empty), **stop**. Use Glob on `campaigns/*/` to find the campaign folders and reply only with:

> Which campaign should I personalize? Run `/personalize <campaign folder>` with one of these:
> - campaigns/...

Write nothing in that case. Also stop if the folder has no `emails/*.md` files, and say so.

## 2. Gather what you need

1. **Groups:** read `leads/leads.csv` and collect the distinct values in the `group` column. Don't assume group names; use whatever the file contains. Read the folder's `leads/CLAUDE.md` too, if it describes the groups.
2. **Emails:** Glob `<campaign folder>/emails/*.md`. These are the originals. Never change them.
3. **Context:** read `brand/voice.md` and `<campaign folder>/plan.md` (if it exists) to learn what each group cares about and which words and claims are not allowed.

## 3. Write one version per email per group

For every original email and every group, write a copy to:

`<campaign folder>/groups/<group>/emails/<same file name>`

Each copy changes **only two things**:
- **The opening line,** the first sentence after the `{{first_name}}` greeting, rewritten so it speaks to that group.
- **One example,** one sentence or list item rewritten with an example that fits that group (for example, homework for parents, deep work for professionals, exam reading for students).

Everything else stays **exactly** as in the original, character for character:
- the `Subject:` and `Preview:` lines
- the `{{first_name}}` greeting
- the one link (same text and same URL)
- every other paragraph, list item and heading
- the sign-off and the two-line footer, as plain text

The new copy must still follow `.claude/rules/emails.md` and `brand/voice.md`. Use no avoided words and no forbidden claims, and keep the same voice. Write only the email: no notes, no subject options, no code blocks.

## 4. Reply with a short summary only

Don't show the emails. Reply with just:

- how many files you wrote (emails × groups), and where
- one example opening line per group, for example:
  - **parents:** "…"
  - **professionals:** "…"
  - **students:** "…"
