# Rules for the leads folder

These rules apply only to files in `leads/`.

- **These are made-up practice people.** Nobody in `leads.csv` is real. They exist only to practise the FocusGuard launch.
- **Never add real people or real email addresses.** If someone asks to add a real person (a friend, a customer, a Gmail or company address), refuse and quote this rule. Practice leads only.
- **Every row needs a consent value.** The `consent` column must never be empty. It says how the person joined, for example `waitlist form`.
- **Never change the `@example.com` addresses.** Every email address ends in `@example.com`, a reserved domain that can never receive mail. Don't edit, replace or "fix" them.

## Format

Keep exactly these columns, in this order:

```
first_name,last_name,email,group,joined_on,consent
```

- `group` is one of: `parents`, `professionals`, `students`.
- `joined_on` is a date written as YYYY-MM-DD.
- The email is `first.last@example.com`, in lowercase.
