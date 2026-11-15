---
paths:
  - "campaigns/**/emails/*.md"
---

# Email file rules

These rules apply to every email file in any campaign. Each email file must follow all of them.

## Top of the file

- The first line is `Subject: ...` and it is 50 characters or fewer.
- The second line is `Preview: ...` and it is 90 characters or fewer.

## Body

- Greet the reader with `{{first_name}}`.
- Include exactly one main link, written as `[Request a quote](https://epatchy.com)`. Use the quote request page address once the client confirms it.
- Follow `brand/voice.md`: plain English, our words, and none of the words we avoid.
- Do not state prices, minimum order quantities or delivery times. Say "request a quote" instead.
- "Over 8 years" is the only form of the in-business claim allowed. Never use a bigger number.

## Ending

End every email with the sign-off from `brand/voice.md`:

Jordan Hayes
Account Manager, Epatchy

Then add this two-line footer as plain text, not inside a code block:

You're getting this because you are on the Epatchy practice list.
Epatchy, 10685-B Hazelhurst Dr. #42429, Houston, TX 77043 · Unsubscribe: {{unsubscribe_url}}
