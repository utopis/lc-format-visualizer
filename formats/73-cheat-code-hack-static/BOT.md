# BOT.md · generate a "'The Cheat Code' / life-hack static (the product as the shortcut)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 (plus 1080x1920)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@bluestone_com](https://x.com/bluestone_com/status/1748311425330622859) · A 12-second jewellery 'hack' from Indian jeweller BlueStone: on-screen title "Pro tip: Wear your ring as a necklace". Hands thread a ring onto a fine chain and fasten it around the neck, ending on the BlueStone logo. The product is the trick.
- Example: [@TheLittStore](https://x.com/TheLittStore/status/1759496322753741209) · Our favourite jewellery hack for rings that we swear by and you’ll never regret is ✨Adjustable Rings✨ The most important thing about adjustable rings 
- Example: [@vincent_alonzi](https://x.com/vincent_alonzi/status/2088876642840277159) · Trendtrack is a cheat code guys Meta, TikTok, Google, Emails Ads rank, EU ad spend, LPs... In one click, you have the entire e-com funnel of any shop 
- Example: [@SEOKeval](https://x.com/SEOKeval/status/2080403580260110750) · Investing in Google Ads is the ultimate SEO cheat code. It literally gives you data on what keywords convert into sales. All you have to do is rank fo
- Example: [@PerezHatesAI](https://x.com/PerezHatesAI/status/2106779894785188006) · This is wild 😭 4.3M views. 250K saves. On a "weird habits" slideshow. No product demo. No feature dump. Just aesthetic slides of habits that "actually
- Example: [@doublenickk](https://x.com/doublenickk/status/2093709535231840277) · This is a f**king cheat code Someone just published a skill pack with the skills used at Anthropic, Google, OpenAI and others ComposioHQ/awesome-claud
- Example: [@natiakourdadze](https://x.com/natiakourdadze/status/2105285236091228373) · AI singing ads are killing it on Tiktok right now. And Arcads lets you turn any script into a singing ad in 1 click 👇 Singing ads cheat code: → Pick a

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Headline | Big bold sans, game-style or "life hack" framing | "The cheat code for birthday gifts:" |
| Visual | The product as the shortcut: a gift box already wrapped, or the necklace in the shower | - |
| Body | 1-2 short lines | "Any 7 for $85. Pre-wrapped. She'll never take it off." |
| Corner | Small logo + "unlocked" icon | - |

### Prompts

**Claude**

```
Give me 20 headlines that frame [product] as a cheat code, hack or shortcut for a known annoyance (gifting, packing, getting ready, travelling). Max 8 words each, no exaggerated claims.
```

**Figma**

```
1080x1350, headline 96px heavy sans, a "🔓 unlocked" chip in gold, product photo 60% of the canvas.
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
- [ ] Files named `F73-<concept>-<variant>`; tracking tag `utm_content=F73-<concept>-<variant>`.
- [ ] Avoid: The "hack" must really save time or effort; otherwise it reads as clickbait.
- [ ] Avoid: No clean public example was found; the visual is an illustrative mock.

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
5. Name every asset `F73-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F73
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

A static that frames the product as a hack or cheat code for a known annoyance: gifting, packing, getting ready fast. The language is "cheat code", "hack" or "the one thing that actually gets used", backed by short review quotes.

### Why it works

- "Cheat code" promises effort saved; people love shortcuts.
- Gift framing ("actually gets used") answers the gift-giver's fear.
- Review snippets supply the proof inside the copy.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Gift box open, 7 pieces fanned; headline "The gift cheat code" | Body: 3 short real review quotes + "any 7 for $85" |

### Hooks

- "The gift that actually gets worn"
- "Cheat code for getting ready in 30 seconds"
- "Travel hack: one stack, zero jewelry pouch"

### Production recipe

1. Pick 3 jobs: gifting, getting ready, travel.
2. Pull 3 short real review quotes for each.
3. Design as a plain static or a Notes screenshot.

### Existing bot prompt

```
Write 6 "cheat code" statics for LC (headline ≤7 words, 3 real review snippets from {{REVIEWS}}, offer line).
```

### Variants to test

- Gift vs routine vs travel
- With vs without quotes

## Reference examples

See [examples/README.md](examples/README.md) (14 posts). Top 5:

- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @bluestone_com (0L/0BM/0V):  — https://x.com/bluestone_com/status/1748311425330622859
- @mkwizrd (136L/186BM/66kV): AquaVoice is a fucking cheat code. Watched the Evolve podcast with @elfilosofooooo today, and bro shared so much sauce. Spoke the shit out of the Claude code to — https://x.com/mkwizrd/status/2089013712959189120
- @SEOKeval (132L/188BM/13kV): Investing in Google Ads is the ultimate SEO cheat code. It literally gives you data on what keywords convert into sales. All you have to do is rank for them, an — https://x.com/SEOKeval/status/2080403580260110750
- @doublenickk (86L/75BM/6kV): This is a f**king cheat code Someone just published a skill pack with the skills used at Anthropic, Google, OpenAI and others ComposioHQ/awesome-claude-skills.  — https://x.com/doublenickk/status/2093709535231840277
