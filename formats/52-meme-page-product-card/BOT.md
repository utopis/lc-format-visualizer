# BOT.md · generate a "Owned meme / niche page with product card ('bro vs me')"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Static memes or 5-10s clips, daily, from an owned meme page), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@leonclipping](https://x.com/leonclipping/status/2107564115275501944) · A meme page format: a supercar "bro vs me" meme (two cars in a garage), then the app's speed card pasted in as the punchline. The page posts memes; the product rides inside them.
- Example: [@iamjasonlevin](https://x.com/iamjasonlevin/status/2079193650450649327) · Nobody wants to follow your brand page. Your brand needs a "Finsta". A secondary account that lets you take risk you wouldn't normally on the main acc
- Example: [@iamjasonlevin](https://x.com/iamjasonlevin/status/2075207111307563424) · Every brand should have a meme page If you are: - scared to post memes on main - run a SaaS or e-com - want to pull the funny marketing lever You shou
- Example: [@iamjasonlevin](https://x.com/iamjasonlevin/status/2064716198843957258) · MEMECEPTION (n.) putting your product into memes In a sentence: “yo bro, memeception on big meme pages is the future of product placement”
- Example: [@DimitriNakis](https://x.com/DimitriNakis/status/2034046029155258542) · Testing the Stake ad method for DoorList on frat meme pages. Might need to dial in the copy lol. Every app is a dating app
- Example: [@jakewilliammo](https://x.com/jakewilliammo/status/1998076247331438778) · I found the “meme page arbitrage” opportunity of 2025 These videos AVERAGE millions of views And brands are completely sleeping on it It’s branded sor
- Example: [@gauravsbuilding](https://x.com/gauravsbuilding/status/2086540833717895480) · Attention all founders who don't know how to market your app, it's fr this easy. Create IG + TikTok pages for: 1. Your Brand 2. AI Influencer 3. Theme
- Example: [@shadcnblocks](https://x.com/shadcnblocks/status/2103741617194578191) · Copy DESIGN.md from any theme Open Alpine, Vercel, or any theme page → Brand guidelines → Copy DESIGN.md. Then install tokens with the shadcn CLI. Age

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Meme | Two-panel "bro vs me" or "them vs me" meme | "Them: takes jewellery off to shower. Me:" |
| Product card | Small product card in the second panel | - |
| Caption | - | "if you know you know" |
| Cadence | Daily posting from the page; product in 1 of 4 posts | - |

### Prompts

**Meme bank (Claude)**

```
Write 30 two-panel meme captions for [niche] where panel two shows the product as the obvious answer; no punching down.
```

**Tools**

```
Canva meme templates or Imgflip; keep the page's look consistent.
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
- [ ] Files named `F52-<concept>-<variant>`; tracking tag `utm_content=F52-<concept>-<variant>`.
- [ ] Avoid: Use meme formats you have rights to; avoid copyrighted stills for paid ads.
- [ ] Avoid: Product in at most one in four posts.
- [ ] Avoid: Label the page as brand-owned in the bio.

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
5. Name every asset `F52-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F52
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

A brand-owned (disclosed) niche meme page posting relatable memes where the product appears as a small card/sticker in the image — distribution via shares, not ads.

### Why it works

- Memes travel; product card rides along.
- Separate from brand feed; tests humour angles cheaply.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Post | Meme image (gift-giving humour) with small LC card in corner | Caption |
| Bio | "by Louise Carter" | Disclosure |

### Hooks

- "Him: what do you want for your birthday / Me:"
- "POV: you can shower in your jewelry now"

### Production recipe

1. Own the page openly ("by LC"); original memes only (no stolen images).

### Existing bot prompt

```
Write 20 gift/jewelry memes (top text/bottom text) with placement for a small LC card; original concepts only.
```

### Variants to test

- Meme style

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @leonclipping (23L/25BM/1kV): Supercar "bro vs me" meme page with the app's speed card pasted on the photo: 2.2k followers, 736k likes, top post 1.4M views. — https://x.com/leonclipping/status/2107564115275501944
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @gauravsbuilding (62L/76BM/5kV): Attention all founders who don't know how to market your app, it's fr this easy. Create IG + TikTok pages for: 1. Your Brand 2. AI Influencer 3. Theme page Then — https://x.com/gauravsbuilding/status/2086540833717895480
- @cattybk (17L/15BM/886V): The most interesting companies being built right now aren't tech companies. They're ad agencies. If, like me, you want to be creative but you're not talented en — https://x.com/cattybk/status/2102397506843725858
