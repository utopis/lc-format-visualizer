# BOT.md · generate a "Live shopping ads (TikTok LIVE / IG Live sessions amplified with paid)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-60 min live session + paid amplification), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@HobiCasa](https://x.com/HobiCasa/status/2084825639866277902) · A TikTok LIVE selling stream: a host holding up Colgate Optic White tubes in front of a red branded backdrop, with on-screen live comments and a product pin.
- Example: [@onlysweatequity](https://x.com/onlysweatequity/status/2099276927697551652) · TikTok live shopping is making QVC look like a rounding error:⁣ ⁣ "Pop Mart got 105,000,000 people to tune into their live streams. These people put u
- Example: [@JVCocoDeals](https://x.com/JVCocoDeals/status/2100085900692607088) · $600 in TikTok LIVE sales packed inside those boxes. Crazy, I know! Here’s how the night started vs. how it ended. The more I do LIVE selling, the les
- Example: [@ShannonJean](https://x.com/ShannonJean/status/2096268871288131727) · JV @JVCocoDeals started reselling about six months ago after discovering me and The Koerner Office podcast. He started with books, moved into pallets,
- Example: [@gotchabellph](https://x.com/gotchabellph/status/2097602786036949382) · 𝐓𝐢𝐤𝐓𝐨𝐤 𝐋𝐢𝐯𝐞 𝐒𝐞𝐥𝐥𝐢𝐧𝐠 𝐰𝐢𝐭𝐡 𝐆𝐨𝐭𝐜𝐡𝐚𝐛𝐞𝐥𝐥 🛒🛍️ A huge thank you to everyone who joined and supported the live selling last Sept. 8! 💕 📈 182.4K total views 👥 
- Example: [@BraydenFlack](https://x.com/BraydenFlack/status/2087037515274547291) · Just had my best night live selling This puts us at $20K in sales 10 days into the month. Pretty close to hitting our first $200K in revenue on TikTok

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Pre-live | Teaser posts and a reminder ad 24h before | "Live tomorrow 7pm: we test 7 pieces in a fish tank." |
| Opening (0-5 min) | Host welcomes viewers, shows the offer | "Any 7 for $85, live-only gift with purchase." |
| Demo blocks | Each piece tested: water, sweat, scratch | Pinned product card for each |
| Q&A | Answer comments by name | - |
| Close | Countdown on the live gift | - |

### Prompts

**TikTok LIVE / IG Live**

```
Run LIVE Shopping ads to the session; pin products; set a 2-person team (host + comment moderator).
```

**Run of show (Claude)**

```
Write a 45-minute run of show with 6 demo blocks, 3 offer reminders and a Q&A.
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
- [ ] Files named `F63-<concept>-<variant>`; tracking tag `utm_content=F63-<concept>-<variant>`.
- [ ] Avoid: Have a moderator for comments.
- [ ] Avoid: Live-only offers must be honoured.
- [ ] Avoid: Rehearse the demos; a failed test live hurts.

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
5. Name every asset `F63-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F63
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

Scheduled live sessions (founder/host trying on stacks, water tests, Q&A, live-only bundle) promoted with Live Shopping Ads that drop viewers straight into the stream with a product bag.

### Why it works

- Real-time Q&A answers objections instantly.
- Live-only offers create genuine urgency.
- Amplify only sessions that already convert organically (MySmile pattern).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5 min | Host intro + today's live-only bundle | — |
| 5-30 min | Try-ons, water test in a bowl, viewer requests | — |
| 30-45 min | Gift guide by recipient | — |
| 45-60 min | Last call; pin product | — |

### Hooks

- "LIVE: we're dunking jewelry in water for an hour"
- "Build-your-stack live — you pick, I style"

### Production recipe

1. Only after TikTok Shop is live (F19).
2. Weekly slot; organic first; boost sessions with above-average GMV/viewer.

### Existing bot prompt

```
Write a 60-minute live run-of-show for LC with segments, live-only bundle (real), objection answers from {{FAQ}}, and 5 hook lines for the Live Shopping Ad.
```

### Variants to test

- Founder vs creator host
- Day/time

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @HobiCasa (293L/18BM/7kV): Colgate PH TikTok live is now showing j-hope’s face for Optic White in their live selling. 😍 🧡 The campaign started this August announcing him as the newest Bra — https://x.com/HobiCasa/status/2084825639866277902
- @ShannonJean (27L/10BM/6kV): JV @JVCocoDeals started reselling about six months ago after discovering me and The Koerner Office podcast. He started with books, moved into pallets, and then  — https://x.com/ShannonJean/status/2096268871288131727
- @BraydenFlack (31L/8BM/2kV): Just had my best night live selling This puts us at $20K in sales 10 days into the month. Pretty close to hitting our first $200K in revenue on TikTok Live sell — https://x.com/BraydenFlack/status/2087037515274547291
- @JVCocoDeals (30L/4BM/2kV): $600 in TikTok LIVE sales packed inside those boxes. Crazy, I know! Here’s how the night started vs. how it ended. The more I do LIVE selling, the less foreign  — https://x.com/JVCocoDeals/status/2100085900692607088
- @Brandeal_ai (14L/1BM/1kV): 🎬 BFCM UGC Roster — Now Open (North America) Beauty/Skincare • Lifestyle • Tech We’re recruiting NA-based creators for Black Friday / Cyber Monday UGC, with pri — https://x.com/Brandeal_ai/status/2101920189705330803
