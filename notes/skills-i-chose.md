# Skills I chose (Epatchy.com B2B embroidery outreach)

Searches run on skills.sh: "campaign plan", "resend", "email marketing" and "email sequence".

"email sequence" results (2026-11-15): `coreyhaines31/marketingskills@email-sequence` has 55.1K installs and its repo has about 60.5K stars (active, individual author, SaaS focus). Anthropic's `email-sequence` has 3.1K installs. I still pick Anthropic's because it is official and sits in the same plugin as `campaign-plan`. `coreyhaines31` is a real second option. Compare both SKILL.md files before choosing. `onewave-ai@cold-email-sequence-generator` (522 installs) looks like a fit by name, but its repo is unchecked.

Checked again on 2026-11-15: all recommended skills still exist and the install and star numbers below are roughly right. Still to do before installing: read each SKILL.md for extra network calls or secret handling.

Note: the "email marketing" search puts high-install skills at the top that don't fit Epatchy, for example `caffeinelabs@extension-email-marketing` (31.8K installs) and `open.feishu.cn@lark-mail` (901.9K installs, a Lark/Feishu mail tool). Install counts alone don't show fit.

## Use these

1. **anthropics/knowledge-work-plugins (marketing plugin: campaign-plan, email-sequence, brand-review)**
   Published by Anthropic. The repo has about 36K GitHub stars. The `campaign-plan` skill shows 3.4K installs. It covers planning and writing campaigns, which is what Epatchy needs.
2. **resend/resend-skills (resend)**
   Published by Resend, the email service. The skill shows 24.7K installs, but the repo has only about 212 stars. The publisher is official, so I trust it for sending. The low star count is normal for a vendor's own skills repo.
   `resend/email-best-practices` (about 146 stars) is a good companion for deliverability advice. B2B cold outreach to US businesses depends on it.

## Avoid these

1. **gocallum/nextjs16-agent-skills@resend-integration-skills**
   About 413 installs but only 23 stars, from an individual author. It is a Next.js code integration, not a campaign tool.
2. **"campaign-planner" clones**, for example `genspark-ai/genoffice` (78 installs, though its repo has about 12.4K stars) and `w95/awesome-claude-corporate-skills` (43 installs, about 321 stars).
   They duplicate Anthropic's `campaign-plan` and have little adoption for this skill. `genoffice` is not a small publisher, so I avoid it because it duplicates `campaign-plan`, not because of who publishes it. A different name does not make a skill better.

## How I decided

1. **Who publishes it?** Prefer official publishers (anthropics, resend) over anonymous accounts.
2. **GitHub stars versus installs.** Install counts can be inflated. Check that the repository has stars and activity that match.
3. **What does the skill do and ask for?** Read the SKILL.md first. Make sure it still exists under the same name, and that it does nothing beyond its purpose, such as extra network calls or secrets.
