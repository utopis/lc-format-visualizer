# BOT.md · generate a "Persona pages: ads run from named narrator pages (catalog of the pattern + LC-safe version)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: System: 2-4 narrator Pages, each running 3-6 native story ads (image + 150-400 word post) to a matching advertorial), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Seanfrank](https://x.com/Seanfrank/status/2094988024211812654) · A creator talking to camera ("This is Meta's answer to TikTok Shop") with cutaways to persona-style pages: a woman holding a drink can, product screenshots, a "where you can deliver" card and a landing page. It explains how persona pages run ads natively.
- Example: [@vincenzo_micale](https://x.com/vincenzo_micale/status/2105349586717950002) · Menopause bracelet brand: 1,592 active Meta ads, 107 days, 59% US — saturation-level creative volume in wearable/jewelry.
- Example: [@benradack](https://x.com/benradack/status/2078473442714616149) · I consolidated our whitelisting ads into one ad set with our brand videos. My CBO performs better with fewer ad sets running. So instead of keeping wh
- Example: [@DTC_Quizbuilder](https://x.com/DTC_Quizbuilder/status/2107516274142285842) · Noverly's copy is built around one idea: ED isn't age or testosterone, it's a clogged pipe They sell it through a doctor-bylined listicle The buyer th

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Dr Ruth White: Persona-page "this woman found relief" static (Dr Ruth White)** (416 days live): An older woman with a red-glowing knee inset; black bar: "VIRAL: THIS WOMAN FOUND RELIEF FROM DAILY IBUPROFEN WITH JUST ONE TURMERIC SUPPLEMENT · CLICK TO LEARN". Run from the persona page "Dr Ruth White". DCO with 22 media.
- **Smooche · Cosmetic Times: “I thought foundation was over for me at 52”** (17 days live): "I thought foundation was over for me at 52": a Smooche first-person ad run from the "Cosmetic Times" page, styled as a beauty publication.
- **Smooche · Aging Queens Magazine: “I thought foundation was over for me at 52”** (6 days live): "I thought foundation was over for me at 52": the same copy run again from a second persona page, "Aging Queens Magazine".

**Do not copy (seen in these live ads):** Pages posing as independent publications and reviewers are deceptive. Do not copy.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Page setup (day 0) | A Facebook/IG Page with a narrator name ("Dana on Jewelry"), a real face (founder, staff or a consenting creator), a cover photo of her jewellery box, and a bio that says "Content by Louise Carter" | Bio: "Ex-stylist. I test jewellery in the sea so you don't have to. Partnered with Louise Carter." |
| Organic seed (week 1) | 6-10 ordinary posts so the Page looks lived in: outfit photos, a "what I packed" carousel, a reply to a follower | Plain first-person captions, no links |
| Ad 1: story post | Phone photo of her hand on a beach towel wearing the stack, slight grain, no logo | Opening line: "I've ruined 4 necklaces in the sea. This one's on month 9." 200-word story, link at the end |
| Ad 2: listicle post | Flat-lay of 5 pieces on a white bedsheet | "5 pieces I never take off (and the one I stopped wearing)" |
| Ad 3: reply post | Screenshot of a real comment she got, then her answer | "Someone asked if gold-plated really survives showers. Honest answer:" |
| Landing | Advertorial written in the same narrator voice, with a "This post is sponsored by Louise Carter" line at the top | Ends in the any-7 offer with a single CTA |

### Prompts

**Claude (narrator bible)**

```
Create a narrator for [brand]: name, age, job, why she wears the product, 3 phrases she always uses, 3 things she would never say. Then write 6 organic posts and 3 native story ads (150-300 words each) in her voice. Every claim must come from this product page: [paste]. Disclose the brand partnership in each ad.
```

**Meta setup**

```
Add the Page to Business Manager; run ads from the narrator Page with the brand as paid-partnership label where possible; same pixel and UTM pattern utm_campaign=F80-<narrator>.
```

**Image (real, not AI)**

```
Shoot on iPhone, natural light, slightly imperfect framing; no studio lighting, no logo overlays.
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
- [ ] Files named `F80-<concept>-<variant>`; tracking tag `utm_content=F80-<concept>-<variant>`.
- [ ] Avoid: Never invent a credentialed persona (doctor, dermatologist) or a fake real-person identity; Meta treats undisclosed persona pages as inauthentic behaviour.
- [ ] Avoid: The narrator must be a real person who agreed to it, or clearly a brand character.
- [ ] Avoid: One narrator per angle; do not run the same story from three narrators.
- [ ] Avoid: If the Page gets comments asking "is this an ad?", answer honestly and pin the answer.

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
5. Name every asset `F80-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F80
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

Big direct-response brands run hundreds of ads from pages named after a narrator ("Sarah Bennett", "Your Health Journal", "Dr. Lisa Downing") instead of the brand page. Each persona has an age, situation and voice and writes first-person natives. LC-safe version: real people (founder, CS lead, real customers with consent) as named narrators, clearly connected to LC, never invented people presented as independent.

### Why it works

- A first-person narrator page reads like a person, not a brand.
- Persona × angle multiplies ad diversity (more distinct "entities").
- Lets one product speak to many avatars (brides, mothers, swimmers).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Page | "Notes from Louise" (real founder) or "Jess from LC customer care" | first-person natives |
| Ad | Long-copy native about a real customer story (with consent) | "Here's what Maria told me…" |

### Hooks

- "Notes from our customer-care desk"
- "A bride wrote to us last week…"
- "I'm the founder, and this email made me cry"

### Production recipe

1. Map 6 real LC avatars (bride, swimmer, nurse, mother-of-the-bride, gift-giver, traveller).
2. Use real narrators with consent; ads clearly from LC.
3. Write 4 natives per avatar; rotate.

### Existing bot prompt

```
Using real stories {{CUSTOMER_STORIES}} (with consent), write 6 first-person natives, one per LC avatar, each ≤250 words, told by the real customer or a named LC staff member.
```

### Variants to test

- Avatar
- Founder vs customer narrator

## Reference examples

See [examples/README.md](examples/README.md) (20 posts). Top 5:

- @FedotOff90 (3L/8BM/1kV): Prime Prometics x-ray: 2,828 active ads, 24 avatars (6 life-event), ~28 narrator personas across 15 pages — persona-page scale pattern + MCP prompt. — https://x.com/FedotOff90/status/2108188222710862166
- @funneloftheweek (0L/0BM/0V): Resilia: 12 persona Pages → one 7-min advertorial (30-50% of traffic), 3-4 copy templates × hundreds of creatives, 544 new ads/30d, OTO flow $30→$83. — https://x.com/funneloftheweek/status/2044464896104857850
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @Seanfrank (140L/113BM/55kV): "Ill just whitelist" Whitelisting is fine. But meta is REWARDING accounts that commit to partnership ads. This is fully tin foil hat theory now... but I have se — https://x.com/Seanfrank/status/2094988024211812654
- @vincenzo_micale (50L/69BM/4kV): Menopause bracelet brand: 1,592 active Meta ads, 107 days, 59% US — saturation-level creative volume in wearable/jewelry. — https://x.com/vincenzo_micale/status/2105349586717950002
