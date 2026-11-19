---
name: personalize
description: Write a version of each campaign email for every lead group in leads/leads.csv. Use when a campaign's emails are final and you want one copy per group.
argument-hint: "[campaign folder]"
context: fork
allowed-tools: Read, Glob, Grep, Write
---

# Personalize a campaign for each lead group

Write one version of every campaign email for every lead group, in the Epatchy brand voice.

## Step 1: Check the argument

The campaign folder is `$ARGUMENTS`.

If it is empty, or the folder does not exist, stop. Do not write anything. Use Glob on `campaigns/*/` and reply with only the list of campaign folders that exist, and ask which one to use.

## Step 2: Read what you need

1. Read `brand/voice.md`. Every line you write must follow it.
2. Read `.claude/rules/emails.md`. Every output file must follow it too.
3. Read `leads/leads.csv`. The groups are the distinct values in the `group` column (today: `sports-teams`, `first-responders`, `brands-local-business`). Read them from the file each time, never from memory. Do not invent groups.
4. Use Glob to find every `*.md` file in `<campaign folder>/emails/`. Read each one.

## Step 3: Write the versions

For each email, for each group, write a new file at:

`<campaign folder>/groups/<group>/emails/<same file name>`

Keep these exactly as in the original:

- The overall structure and paragraph order
- The `Subject:` and `Preview:` lines
- The `{{first_name}}` greeting
- The one `[Request a quote](https://epatchy.com)` link
- The closing tagline, the Jordan Hayes sign-off, and the two-line footer (address and `{{unsubscribe_url}}`)

Change only two things:

1. **The opening line** (the first sentence after the greeting). Rewrite it so it speaks to that group:
   - `sports-teams`: clubs and teams, uniforms, caps, players, coaches and volunteers
   - `first-responders`: fire, police, EMS and public-safety crews, department gear
   - `brands-local-business`: brands and local businesses, staff apparel, merch, a logo on the things you sell or wear
2. **One example** in the body. Swap a single example for one that fits the group. Do not touch the rest of the paragraph.

If an email is already written for one group (for example `03a-sports-teams.md`), still write all group versions, but keep the original's own group version close to the original.

## Voice rules (from `brand/voice.md`)

- Plain English, short clear sentences. Reliable, friendly, bold. Confident about the craft, never loud.
- Use our words: custom patches, custom embroidered patches, digitizing, request a quote, your team, your brand, your crew. Name patch types (chenille, woven label, PVC, dye-sublimation) and backings (hook-and-loop, iron-on).
- Never use: cheap, bargain, hype or superlatives ("amazing", "best in the world"), pressure language ("act now", "limited time", "hurry"), or spam trigger words ("free", "guarantee", "winner", "urgent", "no obligation", "risk-free", "click here", "buy now", "100%", "$$$"). No ALL CAPS words, no extra exclamation marks.
- Never state prices, minimum order quantities or turnaround times. Do not promise durability, speed, exact matches or services the client has not confirmed. Say "request a quote".
- "Over 8 years" is the only allowed form of the in-business claim.
- Do not use real people. Leads are made-up practice people only.

## Step 4: Check before you finish

Use Grep on the files you wrote to confirm: no banned words, no prices or turnaround claims, `{{first_name}}` and `{{unsubscribe_url}}` present, and the subject is 50 characters or fewer. Fix anything that fails.

## Step 5: Reply

Reply with a short summary only, nothing else:

- How many files you wrote
- One example opening line per group
