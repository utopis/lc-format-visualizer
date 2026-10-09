# BOT.md · generate a "Challenge ad ('the 30-day never-take-it-off challenge')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Launch ad (20-30s, 1080x1920) + participant posts + a wrap-up ad), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@0xShahzaib_](https://x.com/0xShahzaib_/status/2104901293190119594) · A real-world stress test: a creator unboxes a smart ring, then wears it through a gym workout (push-ups, dumbbells, machines) to see whether it holds up.
- Example: [@TheModernElder](https://x.com/TheModernElder/status/2093143918355357888) · DAY 10 OF UGC 30 DAY CHALLENGE Today video creation is officially running on repeat in my head. Reaching Day 10 has shifted my focus from making conte
- Example: [@KimRaceRod](https://x.com/KimRaceRod/status/2097084996548726860) · Day 21 of Creator Quest UGC 30 day challenge!!! I can't count and did two 19s🤦🏻‍♀️ Heading it to the last week and learning a ton🙌🏼 #cqchallenge #ugc 
- Example: [@KimRaceRod](https://x.com/KimRaceRod/status/2096026203589095690) · Day 18 of the Creator Quest UGC 30 day challenge!! I can't wait to land some gigs☺️ #cqchallenge #ugc @UGCbyBrandon https://t.co/wgkLXo5eXM
- Example: [@KimRaceRod](https://x.com/KimRaceRod/status/2094998935949427016) · Day 15 of the Creator Quest 30 day challenge!!! I did a reach out with my comment banner and it does look more professional!!! #cqchallenge #ugc @UGCb
- Example: [@KimRaceRod](https://x.com/KimRaceRod/status/2100366661324779651) · Day 30 of the Creator Quest UGC 30 day challenge 🙌🏼 We made and I learned so much!!! It's just the beginning 🙌🏼 #cqchallenge #ugc @UGCbyBrandon https:
- Example: [@KimRaceRod](https://x.com/KimRaceRod/status/2093064218568233104) · Day 9 of the Creator Quest UGC 30 day challenge. Working on sharpening and adding to my Fiverr, thumbnails to look more professional and mock videos t

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Founder or creator to camera, holding up the necklace | "30 days. Never take it off. Not in the shower, not in the sea." |
| 3-10s | The rules on screen while she talks | "Start Monday. Post day 1 and day 30 with #30DayLC. Best results win $500 of jewellery." |
| 10-20s | Fast montage of her own first days: shower, gym, pool | "I'll go first." |
| Updates (week 2-3) | Repost participant clips (with permission) as Stories and a weekly ad | "Day 14: still gold." |
| Wrap-up ad | Grid of day-30 photos + winners announced | "312 of you did it. Here's what 30 days looks like." |

### Prompts

**Official rules (Claude)**

```
Write official rules for a 30-day wear challenge: dates, eligibility by country, how to enter, judging criteria, prize, how winners are notified, no purchase necessary wording where required.
```

**Content plan**

```
Post day 1, 7, 14, 21 and 30 updates; collect clips via a form with a rights checkbox.
```

### QA checklist (all must pass before hand-off)

- [ ] Hook lands in the first 1.5 s (video) or is readable at thumbnail size (static / slide 1).
- [ ] Removal test: delete the product from the script. If it still makes sense, rewrite so the product is the payoff.
- [ ] Matches the reference structure (same beat order and length band) before any creative twist.
- [ ] Uses only real product imagery for the product; AI is for backgrounds, characters or b-roll, and is disclosed where required.
- [ ] Every claim is on the brand's approved-claims list (PDP); no invented stats, reviews, doctors or customers.
- [ ] Captions burned in and inside the safe zone; sound-off still understandable.
- [ ] One clear CTA that matches the landing page offer.
- [ ] Three hook variants delivered for the same body (test hooks, not whole new ads).
- [ ] Files named `F88-<concept>-<variant>`; tracking tag `utm_content=F88-<concept>-<variant>`.
- [ ] Avoid: Prize promotions have legal rules per country (no-purchase-necessary, registration); check before launch.
- [ ] Avoid: Don't promise results; show what participants actually posted.
- [ ] Avoid: Plan for the quiet middle (days 8-20) with your own content.

<!-- QUICKSTART:END -->

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

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @0xShahzaib_ (0L/0BM/0V):  — https://x.com/0xShahzaib_/status/2104901293190119594
- @KimRaceRod (9L/0BM/107V): Day 15 of the Creator Quest 30 day challenge!!! I did a reach out with my comment banner and it does look more professional!!! #cqchallenge #ugc @UGCbyBrandon h — https://x.com/KimRaceRod/status/2094998935949427016
- @KimRaceRod (8L/0BM/139V): Day 9 of the Creator Quest UGC 30 day challenge. Working on sharpening and adding to my Fiverr, thumbnails to look more professional and mock videos to add to m — https://x.com/KimRaceRod/status/2093064218568233104
- @KimRaceRod (7L/0BM/79V): Day 30 of the Creator Quest UGC 30 day challenge 🙌🏼 We made and I learned so much!!! It's just the beginning 🙌🏼 #cqchallenge #ugc @UGCbyBrandon https://t.co/YxZ — https://x.com/KimRaceRod/status/2100366661324779651
- @KimRaceRod (6L/0BM/125V): Day 21 of Creator Quest UGC 30 day challenge!!! I can't count and did two 19s🤦🏻‍♀️ Heading it to the last week and learning a ton🙌🏼 #cqchallenge #ugc @UGCbyBran — https://x.com/KimRaceRod/status/2097084996548726860
