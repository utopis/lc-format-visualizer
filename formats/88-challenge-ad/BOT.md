# BOT.md · generate a "Challenge ad ('the 30-day never-take-it-off challenge')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

## Inputs you need

- `BRAND`: name, product, price, offer, audience, 3-5 proof points, claims you may NOT make
- `REVIEWS`: 20+ customer reviews or comments (voice of customer)
- `ASSETS`: real product photos / video, logo, fonts, colors
- `CHANNEL`: organic (TikTok/IG/Shorts) or paid (Meta/TikTok/YouTube)

## Steps

1. Read **Format DNA** below and 3-5 files in `examples/` (prefer `curated`). Note the hook, the beat structure and the length.
2. Mine `REVIEWS` for the 3 strongest angles (problem, desire, objection) in the customer's words.
3. Write 3 concepts. For each: title, angle, hook (first line / first 2 seconds), full script or slide-by-slide copy, shot list or layout, on-screen text, CTA, caption.
4. Follow the **Production recipe** below for tools and prompts. Use real product imagery for the product itself; never invent product features or results.
5. Name every asset `F88-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F88
concept: <short name>
angle: <problem | desire | objection>
hook: "<first line / first 2s>"
beats:
  - t: "0-2s"
    visual: "..."
    text: "..."
    audio: "..."
caption: "..."
cta: "..."
production: {tools: [...], prompts: [...], est_cost: "...", est_time: "..."}
test: {channel: "...", budget: "...", success_metric: "..."}
```

## Guardrails

- No fake reviews, fake customers, undisclosed AI people presented as real customers, or invented stats. Disclose AI where the platform requires it.
- Follow `../_COMPLIANCE.md` and the brand's claim rules.

## Format DNA (from the playbook)

### What it is

An ad that invites the viewer into a time-boxed challenge ("30 days, never take it off"), with a start date, rules and a reward (feature, gift card, entry). Participants post check-ins, which become new creative.

### Why it works

- Participation beats persuasion; the viewer becomes the demo.
- A dated challenge creates urgency without discounts.
- It generates UGC and streak content (F68).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Creator: "I'm not taking this off for 30 days." | — |
| 5-20s | Rules on screen: shower, swim, gym, sleep | "Join: post day 1 with #LCchallenge" |
| 20-30s | Prize / feature | "Best day-30 photo gets featured" |

### Hooks

- "30 days. Never take it off. Join me."
- "The LC shower challenge starts Monday"

### Production recipe

1. Write rules and prize terms (sweepstakes law if prizes).
2. Seed with 10-20 creators (F43).
3. Run the ad to customers and lookalikes; repost check-ins.

### Existing bot prompt

```
Design a 30-day LC challenge: name, rules, check-in prompts for days 1/7/14/30, prize mechanics (compliant), ad script (30s) and 3 recap post templates.
```

### Variants to test

- Prize vs feature-only
- Customer vs creator seeding

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @KimRaceRod (9L/0BM/107V): Day 15 of the Creator Quest 30 day challenge!!! I did a reach out with my comment banner and it does look more professional!!! #cqchallenge #ugc @UGCbyBrandon h — https://x.com/KimRaceRod/status/2094998935949427016
- @KimRaceRod (8L/0BM/139V): Day 9 of the Creator Quest UGC 30 day challenge. Working on sharpening and adding to my Fiverr, thumbnails to look more professional and mock videos to add to m — https://x.com/KimRaceRod/status/2093064218568233104
- @KimRaceRod (7L/0BM/79V): Day 30 of the Creator Quest UGC 30 day challenge 🙌🏼 We made and I learned so much!!! It's just the beginning 🙌🏼 #cqchallenge #ugc @UGCbyBrandon https://t.co/YxZ — https://x.com/KimRaceRod/status/2100366661324779651
- @KimRaceRod (6L/0BM/125V): Day 21 of Creator Quest UGC 30 day challenge!!! I can't count and did two 19s🤦🏻‍♀️ Heading it to the last week and learning a ton🙌🏼 #cqchallenge #ugc @UGCbyBran — https://x.com/KimRaceRod/status/2097084996548726860
- @KimRaceRod (5L/0BM/123V): Day 18 of the Creator Quest UGC 30 day challenge!! I can't wait to land some gigs☺️ #cqchallenge #ugc @UGCbyBrandon https://t.co/wgkLXo5eXM — https://x.com/KimRaceRod/status/2096026203589095690
