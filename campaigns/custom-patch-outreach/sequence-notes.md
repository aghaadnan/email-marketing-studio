# Sequence notes: Custom Patch Outreach

Companion to `plan.md`. Covers subject line options, the send flow, branching rules and tests. Practice mode only: no email goes to real people.

## 1. Subject line options

Option A is the subject already in the email file. Option B and C are alternates for testing. All are 50 characters or fewer and follow `brand/voice.md`.

| Email | A (in file) | B | C |
|---|---|---|---|
| 1 | Custom patches for your team or brand | Meet Epatchy, a Houston patch maker | What custom patches can do for your crew |
| 2 | Four patch types, in plain words | Chenille, woven, PVC: which one fits? | What is a chenille patch? And the other three |
| 3a | Patches for your team's uniforms and caps | Give your whole team a matching look | Team patches on jackets, hoodies and caps |
| 3b | Department patches, clear and built to last | A patch your department can be proud of | Clear, durable patches for your crew |
| 3c | Your brand, stitched onto caps and apparel | Put your logo on a patch | Branded caps and jackets, made with care |
| 4 | Hook-and-loop, iron-on, or sewn on for you | How should your patch attach? | We can sew your patches on for you |
| 5 | How a quote request works, step by step | From artwork to patch: how it works | What happens after you request a quote |
| 6 | Planning patches for the new year? | New season, new gear, new patches? | A quiet note before the new year |

Preview text stays as written in each email file.

## 2. Send flow

```
[Practice list, tagged by group]
        |
        v
Email 1  Mon 2026-12-07  (all groups)
        |
Email 2  Thu 2026-12-10  (all groups)
        |
        +-- Sports teams and clubs ------> Email 3a  Tue 2026-12-15
        +-- First responders ------------> Email 3b  Tue 2026-12-15
        +-- Brands and local businesses -> Email 3c  Tue 2026-12-15
        |
        v   (groups rejoin)
Email 4  Thu 2026-12-17  (all groups)
        |
Email 5  Tue 2026-12-22  (all groups)
        |
   (no sends 12-24, 12-25)
        |
Email 6  Wed 2026-12-30  (all groups)
        |
        v
[END: sequence complete. No send on 2027-01-01]

Exit at any point (no more emails):
  - Requests a quote   -> [EXIT: converted]
  - Unsubscribes       -> [EXIT: suppressed]
  - Replies with a question -> pause, answer by hand, then resume or exit
```

## 3. Branching and exit rules

- **Exit on quote request.** Anyone who submits a quote request leaves the sequence. They get a personal follow-up instead.
- **Exit on unsubscribe or spam complaint.** Remove right away and never re-add.
- **Pause on reply.** If someone replies, stop their emails until a person has answered.
- **Group split at email 3.** Each contact gets only the version for their group. A contact in no group, or in more than one, is held back until tagged. This is a dependency from `plan.md`.
- **No engagement branches.** The list is small and the calendar is short, so every remaining contact gets every email. The open slot in the calendar (about 20 percent) can hold one follow-up for people who clicked but did not request a quote, if early results suggest it.
- **Re-entry.** None during this campaign.
- **Suppression.** Skip anyone who unsubscribed from any earlier Epatchy list.

## 4. A/B test suggestions

1. **Subject lines (emails 1, 2 and 6).** Split the list in half, send option A to one half and B or C to the other. Judge by open rate. With a small list, treat the result as a hint, not proof.
2. **Link wording in email 1.** "Request a quote" against "Tell us what you need". The email file rules require the link text "Request a quote", so run this only after the client agrees to change the rule.
3. **Group comparison (email 3).** The three versions already show which group responds most. Compare click rate and quote requests by group. This answers the secondary goal in `plan.md`.

Change one thing per test.

## 5. Metrics to track

- **Primary:** quote requests, against the planning target of 40 by 2027-01-03 (to be confirmed by the client).
- **Per email:** open rate, click rate to the quote page, replies, unsubscribes.
- **By group:** the same numbers for sports teams, first responders and brands.
- **Sequence level:** quote requests per email, and the email after which most unsubscribes happen.
- **Targets:** set after the practice send, as in `plan.md`.
- **Review:** a short summary each week, and a full review in the week of 2027-01-04.

## 6. Setup checklist

1. Tag each contact with one group.
2. Confirm the quote request page works and swap it in for `https://epatchy.com` in every email.
3. Confirm `{{first_name}}` and `{{unsubscribe_url}}` fill in correctly.
4. Schedule each email for its date. Skip 12-24, 12-25 and 01-01.
5. Add the exit rules above in the sending tool.
6. Do a practice send to made-up addresses only.
