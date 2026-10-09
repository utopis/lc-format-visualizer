# BOT.md · generate a "Backhanded / 'bad review' ad (complaint that is secretly a benefit)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 or a 10-15s video), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@Smdigitalsys](https://x.com/Smdigitalsys/status/2099549775892783266) · An agency's animated ad built from a real 1-star review ("They left us a 1-star review. We turned it into an ad"): a review card pops up, a hand on a laptop, an "ADS" dashboard, then a logo end card.
- Example: [@thedennis](https://x.com/thedennis/status/2036981673259393507) · The best ad I ever wrote came from a 1-star review. No brainstorming session. No creative brief. No agency deck. One angry customer who wrote exactly 
- Example: [@Peter_Quadrel](https://x.com/Peter_Quadrel/status/2050482614696640734) · 1 Star Reviews Make Your BEST Ads... Nevermind UGC, founder explainers, or polished product shots, negative review ads are what get your market's atte
- Example: [@cortex_adbrain](https://x.com/cortex_adbrain/status/2103883993603031429) · if you're a creative strategist, a 1-star review just outworked your entire creative brief the brand quoted their own worst complaint, bolded it, gave
- Example: [@stephenfung_dev](https://x.com/stephenfung_dev/status/2089528727445062001) · Results of buying this ad spot: 358 downloads (+29% week over week) $121.67 in revenue (+114% week over week) $62 in MMR (+75% week over week) 1 - 1 s

### Live paid ads in this format (2 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Smooche: “I just got the smooth reverse tight serum in an absolutely shook it…”** (4 days live): Opens: “I just got the smooth reverse tight serum in an absolutely shook it. Literally target Literally target my fine lines and wrinkles helps target those hyperpigmentation pigmentation in dark spots and…”
- **Resilia · Arterial Health Review: “not because it stopped working for the 4th of july right now. my chest…”** (1 days live): Opens: “not because it stopped working for the 4th of july right now. my chest at night.”

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Main | A 1-star review card, real-looking, with the "complaint" | "1/5: My husband keeps asking where my necklace is from and I'm tired of answering." |
| Product | The necklace on the reviewer's neck, or on its own | - |
| Video version | Creator reads the "complaint" deadpan | "Worst purchase. I can't take it off. Literally, I don't need to." |
| End | Offer | "Any 7 for $85." |

### Prompts

**Claude**

```
Write 15 backhanded "complaints" about [product] where the complaint is really a benefit (too many compliments, never wears out). Keep them short and dry.
```

**Figma**

```
Review card with stars, name, "Verified buyer" tag; make it obviously a playful creative.
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
- [ ] Files named `F36-<concept>-<variant>`; tracking tag `utm_content=F36-<concept>-<variant>`.
- [ ] Avoid: If you present it as a real review, it must be a real review.
- [ ] Avoid: Otherwise make the joke obvious so nobody is misled.
- [ ] Avoid: Keep the benefit inside the joke concrete.

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
5. Name every asset `F36-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F36
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

A review-card or creator reading a "1-star review" whose complaint is actually a benefit ("1 star: I can't find a reason to take it off"), or a brand "we're sorry" apology for a positive problem ("we're sorry the herringbone sold out again"). Must use real reviews or be clearly the brand's own joke.

### Why it works

- Negative stars stop the scroll (loss-aversion).
- The twist makes it shareable; humour lowers ad resistance.
- Real backhanded reviews are common in LC's review base (compliments, "addicted").

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-2s | 1-star review card on screen, creator reacting | "We got a 1-star review…" |
| 2-8s | Zoom on text: "Ruined my life. Everyone asks where it's from and I have to keep sending the link." | Creator deadpan |
| 8-15s | Product shots | "We're so sorry. Any 7 for $85." |

### Hooks

- "Our worst review ever:"
- "We're sorry. (Not really.)"
- "1 star: now my sister wants one too"
- "Complaint received: I forgot I was wearing it in the ocean"

### Production recipe

1. Search LC reviews for backhanded phrases ("addicted", "everyone asks", "husband", "can't stop").
2. Use real review text (with reviewer first name/initial per review-platform rules); if invented for comedy, frame as brand's own joke, never as a customer review.
3. Static review card + 10-15s creator/Qirra read version.

### Existing bot prompt

```
From these real LC reviews {{REVIEWS}}, find 10 that read like complaints but are benefits. For each: on-image quote (verbatim), 1-line brand "apology", 80-word primary text. Do NOT edit review wording.
```

### Variants to test

- Review card vs founder read
- Apology vs 1-star frame

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @KanishDigital (13L/13BM/824V): Negative hooks ("this product should be banned", "don't buy this…") — for one baby brand the best ad is a fully negative ad. — https://x.com/KanishDigital/status/2101549415467213023
- @Yannlce (3L/2BM/1kV): Same 40-format list (adds claymation, AI podcast). — https://x.com/Yannlce/status/2085017654364958737
- @nicktheriot_ (219L/348BM/12kV): 2026 FB creative styles tier list: S = long primary text + organic image, LTO, UGC, VSL, reaction, news; A = demo, us vs them, testimonial, close-up, founder st — https://x.com/nicktheriot_/status/2108173638033871013
