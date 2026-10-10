# BOT.md · generate a "Breaking-news / news-report style ad"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-30s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@ladprofit](https://x.com/ladprofit/status/2089745258796261415) · An AI-generated breaking-news broadcast: a male anchor at a news desk with a red "BREAKING NEWS" lower-third, then a female reporter holding up the product as if it were a news story.
- Example: [@HenryCrochemore](https://x.com/HenryCrochemore/status/2034948938789171441) · an AI news broadcast opens the video “breaking news” a serious anchor at a desk city skyline behind him calm, authoritative voice it looks exactly lik
- Example: [@richardbrien](https://x.com/richardbrien/status/2103478126928138309) · "Breaking News" style ad creative crushes harder than any other format across long periods of time.
- Example: [@rogiergg](https://x.com/rogiergg/status/2086977376286585184) · (BREAKING NEWS - CAUSE OF DEATH REVEALED) tbh that's just a creative on a $29.99 CO detector not a product headline a news format! the ad does not fee
- Example: [@Bsschiller](https://x.com/Bsschiller/status/2048497164393791985) · We turned an @IShowSpeed stream into a “news report” ad for a South Florida experience brand — and it was an overnight hit. 106x reach vs followers Hu
- Example: [@inceptly](https://x.com/inceptly/status/2105302286490546274) · 🚨 What if your next ad looked like breaking news? This week's Modular Creative System ad breakdown covers a Find Legal ad that opens on an AI-generate
- Example: [@adamtaylorl](https://x.com/adamtaylorl/status/2090038023287152826) · 5. The Fake News static News framing = borrowed journalism trust. Their best static and it's basically a headline.

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Aurivita Cayenne: "WARNING: Fake websites!" brand notice static (Aurivita)** (197 days live): A red "WARNING Fake websites!" banner with screenshots stamped "FAKE": "We are the original brand, and we don't sell on Amazon… if you see ads offering Auri Cayenne Pepper in huge discounts, do not place an order."
- **Breaking News: Breaking-news TV lower-third static** (141 days live): Two news-anchor photos with a "BREAKING NEWS" bug and a lower-third headline about a family considering legal action against a news anchor.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | News-desk set, "BREAKING NEWS" red lower-third | Anchor: "Breaking: the necklace you can swim in is back in stock" |
| 3-15s | Reporter on location with the product | The genuinely new thing (launch, restock, milestone) |
| 15-25s | B-roll with news ticker | Facts |
| End | Logo card | Offer |

### Prompts

**Veo 3 / Kling**

```
television news studio, a male anchor at a news desk, red BREAKING NEWS lower third, professional lighting, says "[line]", 8s, 9:16
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
- [ ] Files named `F38-<concept>-<variant>`; tracking tag `utm_content=F38-<concept>-<variant>`.
- [ ] Avoid: Do not imitate a real network's branding.
- [ ] Avoid: The "news" must be true; use only for real launches/restocks/milestones.
- [ ] Avoid: Label AI.

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
5. Name every asset `F38-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F38
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

The ad borrows news grammar: "BREAKING" lower-third, anchor-style delivery or a news-article screenshot announcing something genuinely new (launch, milestone, restock, real press). Video = creator as reporter on green screen; static = headline card.

### Why it works

- News framing triggers "what happened?" curiosity.
- S-tier in a 2026 operator tier list.
- Natural fit for launches and milestones.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | Red "BREAKING" bar, creator as anchor | "Breaking: a jewelry brand just passed 300,000 customers and…" |
| 2-12s | B-roll of pieces in water | "…the reason is you can shower in it." |
| 12-20s | Offer card | "Any 7 for $85. Back to you." |

### Hooks

- "BREAKING: the necklace that survived 6 months of ocean"
- "News: 300,000 women stopped taking their jewelry off"
- "This just in: the herringbone is back"

### Production recipe

1. Only announce real news (launch, milestone, restock, real press).
2. News lower-third template; no real network logos.
3. Creator on green screen or AI presenter (labelled).

### Existing bot prompt

```
Write 5 news-style LC ad scripts (20s) around these real events {{EVENTS}}: anchor line, 2 supporting facts, CTA. Plus 5 headline statics. Do not mimic real news outlets.
```

### Variants to test

- Anchor video vs headline static
- Serious vs playful

## Reference examples

See [examples/README.md](examples/README.md) (13 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
- @EmerieOnoh (6L/6BM/498V): Static formats printing: us vs them, whiteboard, breaking news, doodle, low stock, iPhone notes, Google search, we're sorry, Reddit, tweet screenshot, text on p — https://x.com/EmerieOnoh/status/2098426706612683154
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
