# Skills I chose

Searched skills.sh on 2026-11-11 with `npx skills find` for "email marketing", "email sequence", "campaign plan" and "resend". Star counts come from each GitHub repository on the same day. Nothing is installed yet.

## Use these

**1. Anthropic's marketing plugin, for planning and writing campaigns**
`anthropics/knowledge-work-plugins`, 35,462 GitHub stars.
- Skills found: `campaign-plan` (3.4K installs), `email-sequence` (3.1K installs) and `campaign-planning` (221 installs).
- Why: the publisher is Anthropic, the company that makes Claude, and the repository is busy and well starred. It is built as a plugin for Claude Code, so it brings the planning, sequence and brand-review commands together in one install, at project scope.

**2. Resend's own skills, for sending email**
`resend/resend-skills` (211 stars) and `resend/email-best-practices` (147 stars).
- Skills found: `resend` (24.5K installs), `resend-cli` (14K), `agent-email-inbox` (14K) and `email-best-practices` (8.3K).
- Why: the publisher is Resend, the email service we will connect to. A company's own instructions for its own product are the most likely to be correct and kept up to date. The star counts are modest, but the publisher is the official organization, and that matters more here.

Worth knowing: `coreyhaines31/marketingskills` (59,752 stars) is a popular, well-known collection by one author. Its `emails` skill has 87K installs and `email-sequence` 55.1K. It's a good second opinion, but it isn't official, so the two above come first.

## Avoid these

**1. `caffeinelabs/skills@extension-email-marketing`, with 31.1K installs and 2 GitHub stars**
It's the top result for "email marketing", yet almost nobody has starred the repository. Thousands of installs with only a couple of stars is the classic sign of inflated download counts. Install numbers are easy to pump up with scripts and are not proof that people use or trust a skill.

**2. `samber/dev-event-organizer-skills@event-attendee-email-sequences`, with 6.6K installs and 4 GitHub stars**
It has the same mismatch between installs and stars, the repository is only two months old (created 2026-09-06), and it's about event attendees rather than product launches. So it's an untrusted source and the wrong fit.

Also skipped: `open.feishu.cn@lark-mail`, which shows 886.8K installs but is for Lark/Feishu mail, an unrelated product, and `claude-office-skills/skills`, which hasn't been updated since January 2026.

## How I decided

Before installing any skill, check these three things:

1. **Who publishes it.** Prefer the official organization: the tool's maker (anthropics) or the service's own team (resend). An unknown account needs a closer look.
2. **Do the GitHub stars match the install count?** Install counts can be faked. Stars, a long history and recent updates are harder to fake. High installs with very few stars is a warning sign.
3. **What's inside, and does it fit?** Open the SKILL.md and any scripts before installing. Check what it tells Claude to do, whether it runs commands or sends data anywhere, and whether it fits this studio's job: launch emails sent safely to test addresses.
