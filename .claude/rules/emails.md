---
paths:
  - "campaigns/**/emails/*.md"
---

# Rule for every email file

This rule applies to every email file in any campaign, and only to email files. Each email file must follow it exactly.

1. **The first line is the subject:** `Subject: ...`, 50 characters or fewer, counting everything after `Subject: `.
2. **The second line is the preview:** `Preview: ...`, 90 characters or fewer, counting everything after `Preview: `.
3. **Greet the reader with `{{first_name}}`**, for example `Hi {{first_name}},`.
4. **Exactly one main link,** written as a Markdown link to the FocusGuard Play Store page:
   `[Button text](https://play.google.com/store/apps/details?id=io.github.mumtazmaqsood.focusguard)`
   No other links anywhere in the email.
5. **End with our sign-off** from `brand/voice.md`:

   To more time for what matters,
   Mumtaz from FocusGuard

6. **Then this two-line footer, as plain text, not inside a code block:**

   You're getting this because you joined the FocusGuard waitlist.
   FocusGuard, {{company_address}} · Unsubscribe: {{unsubscribe_url}}

The file holds only the email itself: no subject options, no notes, no comments, and no code blocks.
