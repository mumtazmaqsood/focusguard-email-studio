# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this studio is for

This is an email marketing studio for a small business. Here we plan email campaigns, write the emails, and tailor them for each group of customers. Our business is **FocusGuard**, an Android app (test version) that helps people spend less time on distracting sites and apps, for parents and adults alike.

We build the studio by following `ASSIGNMENT.md` (the Email Studio Lab course), one step at a time. Each step has a build prompt and then a check that runs in a fresh session. Don't build ahead of the current step. The course prompts use a sample brand (Kettlebird Tea and The Steep Club). Wherever a prompt names it, use FocusGuard instead.

## Brand voice

@brand/voice.md

## Folders

- `brand/`: the brand voice guide, which sets how our emails sound.
- `leads/`: made-up practice customers, split into groups.
- `campaigns/`: one folder per campaign, holding its plan and its emails.
- `notes/`: research notes and working files, such as which skills we chose.

## Rules

- **Write in plain English.** Use short sentences and everyday words, with no jargon.
- **Never send email to real people.** Practice leads use `@example.com` addresses only.
- **Ask me before deleting anything:** files, folders, commits or emails.
- Never put a real API key or password in any file.

## Tools

- Anthropic's marketing plugin is installed for this project only (see `.claude/settings.json`). It gives us `/marketing:campaign-plan`, `/marketing:email-sequence` and `/marketing:brand-review`.
- `.claude/settings.local.json` holds personal settings and is never committed.
