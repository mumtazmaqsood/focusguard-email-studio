# FocusGuard Email Studio

An email marketing studio run with **Claude Code**, built step by step for the **Email Studio Lab** assignment (Panaversity AI-102 / FDE-102). Claude plans a launch campaign, writes the emails, tailors them for each group of customers, and sends them, safely, to a practice email server only.

The full assignment is in [`ASSIGNMENT.md`](ASSIGNMENT.md). The course uses a sample brand (Kettlebird Tea and The Steep Club). This studio uses a real brand of my own instead: **FocusGuard**.

## The brand: FocusGuard

[FocusGuard](https://github.com/mumtazmaqsood/focusguard-releases) is an Android app (test version) that helps people spend less time on Facebook, X and other distracting sites and apps:

- **One daily limit** shared by everything on the block list (60 minutes by default)
- **Allowed hours**: blocked sites and apps only open in the hours you choose
- **A partner** (a parent, spouse or friend) is the only one who can give more time, with a one-time code
- **Private by design**: no internet permission, no ads, no analytics

The campaign launches FocusGuard to its waitlist, in three groups: **parents**, **professionals** and **students**.

## What's inside

```
├── CLAUDE.md                      the studio's rules (imports brand/voice.md)
├── ASSIGNMENT.md                  the course: 15 steps
├── brand/voice.md                 how FocusGuard sounds: voice, words, forbidden claims, sign-off
├── leads/
│   ├── leads.csv                  24 made-up practice leads (all @example.com)
│   └── CLAUDE.md                  rules for this folder only
├── campaigns/steep-club-launch/
│   ├── plan.md                    the 4-week launch plan (7 Dec 2026 to 3 Jan 2027)
│   ├── emails/                    4 launch emails
│   └── groups/<group>/emails/     a version of each email per lead group (12 files)
├── notes/skills-i-chose.md        which community skills to trust, and why
└── .claude/
    ├── settings.json              marketing plugin, enabled for this project only
    ├── rules/emails.md            format rule for every email file (paths: pattern)
    └── skills/personalize/        my own skill: one email copy per lead group (context: fork)
```

The campaign folder keeps the course's name (`steep-club-launch`) so the course's check prompts work unchanged. Its contents are all FocusGuard.

## Progress

| Step | Topic | Claude Code feature | Status |
|---|---|---|---|
| 1 | Look before you build | Finding and vetting skills | ✅ Done |
| 2 | Set up your studio | Project-scope plugin, CLAUDE.md, .gitignore | ✅ Done |
| 3 | Brand voice | Interview first, `@import` | ✅ Done |
| 4 | Plan the campaign | Plugin skill `/marketing:campaign-plan` | ✅ Done |
| 5 | Practice leads | Input/output examples, folder CLAUDE.md | ✅ Done |
| 6 | Email rule and sequence | `.claude/rules/` with `paths:` | ✅ Done |
| 7 | Fresh-eyes review | Review in a new session, fixes in one message | ✅ Done |
| 8 | Personalize skill | Own skill with `argument-hint`, `context: fork`, `allowed-tools` | ✅ Done |
| 9 | Connect Resend (practice mode) | `.mcp.json`, `${VAR:-default}` credentials | ⏳ Next |
| 10 | The safety guard | PreToolUse hook | ⬜ |
| 11 | Practice launch | Sending through MCP to test addresses | ⬜ |
| 12 | Resume and fork | `--resume`, `--fork-session` | ⬜ |
| 13 | Automatic review | Headless `claude -p` with a JSON schema | ⬜ |
| 14 | Package the studio kit | Plan mode, plugins | ⬜ |
| 15 | What customers love (stretch) | Subagents, scratchpad, `/compact` | ⬜ |

## How to use it

You need Node.js 22+, Git and [Claude Code](https://claude.com/claude-code).

```bash
git clone https://github.com/mumtazmaqsood/focusguard-email-studio.git
cd focusguard-email-studio
claude
```

Accept the prompts to trust the folder and the marketing plugin. Then try:

- `/marketing:brand-review campaigns/steep-club-launch/emails/`: review the emails against the brand voice
- `/personalize campaigns/steep-club-launch`: write one version of each email per lead group

## Safety

- **No real email is ever sent.** Every lead uses an `@example.com` address, a reserved domain that can't receive mail.
- Sending (from step 9 on) goes only to a practice server on your own computer, and only to Resend test addresses or your own email.
- No API keys are stored in this repo. Personal settings live in `.claude/settings.local.json`, which git ignores.
