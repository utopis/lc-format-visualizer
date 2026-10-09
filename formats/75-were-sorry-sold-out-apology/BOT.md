# BOT.md · generate a "'We're sorry, we keep selling out' apology notice"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static notice 1080x1350 (or a 10s founder video)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@OmologatoUK](https://x.com/OmologatoUK/status/2099497006158725545) · A back-in-stock / nearly-sold-out post: a watch on an orange strap laid on an old racing newspaper (TIFOSI x CAN-AM), with copy saying it came back and "has already nearly sold out again — ONE LEFT".
- Example: [@Djigida_Central](https://x.com/Djigida_Central/status/1639635729130176512) · Our stock gets sold-out so fast! We are sorry to have to tell you “sold out” that’s just the price we have to pay for being the best womens fashion st
- Example: [@bikeshopwhse](https://x.com/bikeshopwhse/status/1582101101343830016) · The Motobecane Fantom 29 Advent is now back in stock! We are sorry they keep selling out... https://bikeshopwarehouse.com/cgi-bin/BSW_STOR20.cgi... #b
- Example: [@ChichiChachaha](https://x.com/ChichiChachaha/status/2076303701426471059) · #Overdo sets a new pre-release advertising record. ~RMB 120M secured from ads &amp; sponsorships bef. its premiere date is even announced. 20+ brand p
- Example: [@notdailyavatar](https://x.com/notdailyavatar/status/2080320968178692301) · Getting ads for the same brand as Johannes' boots... Are you mocking me? 😭😭 They're too expensive and also sold out https://t.co/6ZwGz09Zcq
- Example: [@mikasafavx](https://x.com/mikasafavx/status/2077807501211267281) · SKIMS after lisa’s ad: 22% revenue growth in APAC skims x nike set sold out $1B net sales projected at the end of the year GAP after trasheye: 7% reve

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Smooche: “We f*cked up”** (100 days live): "We f*cked up." A letter-style apology for over-ordering, with a warehouse photo of pink boxes and a "60% off" button. Served through a catalog-template slot.
- **Resilia · Resilia: “We're so sorry!”** (1 days live): "We're so sorry!": a "we've been so busy packing 6,000kg of oregano oil…" apology with a "$39.99 with free gifts" button.
- **Resilia · Midlife Wellness Journal: “OFFICIAL APOLOGY STATEMENT”**: "OFFICIAL APOLOGY STATEMENT": a black text-heavy notice about selling out.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Header | Plain notice layout, small logo, date | "We're sorry." |
| Body | 3-4 short lines from the founder | "We didn't expect 3,000 of you to want the same paperclip chain. It sold out in 9 days. Again." |
| Close | Restock date or waitlist | "Back on [date]. Join the waitlist so you don't miss it." |
| Sign-off | Founder name | - |

### Prompts

**Copy (Claude)**

```
Write a genuine apology from the founder about [product] selling out, under 60 words, with the real reason it sold out and the real restock date.
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
- [ ] Files named `F75-<concept>-<variant>`; tracking tag `utm_content=F75-<concept>-<variant>`.
- [ ] Avoid: Only run it when the item really sold out; fake scarcity breaks consumer-protection rules.
- [ ] Avoid: Give a real date; vague "soon" kills the urgency.

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
5. Name every asset `F75-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F75
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

A notice-style static written as an apology: "We're sorry. We didn't expect to keep selling out of ___." The body explains why demand spiked (the mechanism) and that it is back in stock now. Scarcity and social proof wrapped in humility.

### Why it works

- An apology reads as an announcement, not an ad.
- "Keeps selling out" is evergreen demand-based urgency (7 Trends #6).
- The story explains why others buy it.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Plain cream notice card, signature at the bottom: "We're sorry. Chelsea Herringbone sold out [N] times this summer." | Body: why (waterproof), it's back, any 7 for $85 |

### Hooks

- "We're sorry, it sold out again"
- "An apology from Louise Carter"
- "To everyone on the waitlist: we're sorry"

### Production recipe

1. Run it only for SKUs that really sold out (log the dates).
2. Signed by the founder or team.
3. Retarget waitlist and visitors first, then go cold.

### Existing bot prompt

```
Write 3 "we're sorry, we keep selling out" notices for LC SKUs with real sell-out history {{SELLOUTS}}: ≤70-word card text + 120-word primary text.
```

### Variants to test

- Founder signature vs team
- Cold vs retargeting

## Reference examples

See [examples/README.md](examples/README.md) (10 posts). Top 5:

- @briannjho (138L/338BM/10kV): Ad picks: Smooche AI song ad, Ryze AI skit, UndrDog big-enemy, Everyday Dose skit, Serene Herbs AI identity, Nuora apology mash-up, Mama Bear "this is what happ — https://x.com/briannjho/status/2094662259746480410
- @FedotOff90 (17L/18BM/3kV): Rebuilt the formats list with proof: 30-day survival column = "this works" bar; copy the structure, not the words. — https://x.com/FedotOff90/status/2100948331136782532
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @OmologatoUK (0L/0BM/0V):  — https://x.com/OmologatoUK/status/2099497006158725545
- @ChichiChachaha (251L/24BM/10kV): #Overdo sets a new pre-release advertising record. ~RMB 120M secured from ads &amp; sponsorships bef. its premiere date is even announced. 20+ brand partnership — https://x.com/ChichiChachaha/status/2076303701426471059
