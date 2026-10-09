# BOT.md · generate a "'Fake PDP': a product-page screenshot as the ad (+ app-settings / Trustpilot / comment screenshots)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 static 1080x1350 (phone-screenshot look)), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2106046297434374289) · A native-looking warehouse photo: a hand holding the product (a grey neck pillow) in front of stacked shipping boxes with a pink "SUMMER SALE IS LIVE! 55% OFF + Free shipping + Free gift" banner. It looks like a store update, not a designed ad.
- Example: [@callmenirmal](https://x.com/callmenirmal/status/1905160356810625284) · 4. Turn into ADS/Creatives. This part blew my mind 🤯 I literally just took a screenshot of the product page (PDP) and told GPT-4o: “Make an ad out of 
- Example: [@reemaabajaj](https://x.com/reemaabajaj/status/1869425787805262293) · I love this ad by @TeaboxTea Typical Ugly Ad 2.0 Here's why👇 💚 Headline hook with a freebie offer They don’t just mention a freebie; they boost its pe

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Main image | A phone screenshot of the real product page: product photo, title, price, star rating with review count, 3 bullets, a gold "Add to bag" button | - |
| Overlay | One handwritten-style circle or arrow around the reviews count | "4,812 reviews" |
| Variant A | iOS Settings-style toggles | "Take off before shower: OFF · Turns green: OFF · Compliments: ON" |
| Variant B | Trustpilot-style review card screenshot | One real 5-star review |
| Primary text | - | "Screenshot this for later." |

### Prompts

**Figma**

```
Recreate the PDP at 1170x2532 (iPhone), then crop to 1080x1350 keeping price + stars + button; use the real numbers.
```

**Settings variant**

```
iOS Settings UI kit (Figma community), 4 toggles, SF Pro, a product photo as the profile image.
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
- [ ] Files named `F90-<concept>-<variant>`; tracking tag `utm_content=F90-<concept>-<variant>`.
- [ ] Avoid: Price, rating and review count must be real and current.
- [ ] Avoid: Don't imitate Amazon, Apple or Trustpilot logos; use their look, not their trademarks.
- [ ] Avoid: Update the ad when the price changes.

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
5. Name every asset `F90-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F90
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

A static that looks like a phone screenshot of a product page (price, stars, "add to cart", bullets) or other UI (iOS Settings toggles "Take off before shower: OFF", a Trustpilot card, a TikTok comment, a Google search). It extends F32 with the UI types Fedotoff found running.

### Why it works

- Familiar UI looks like content, not an ad, so people stop for screenshots.
- The PDP mock pre-sells the offer before the click.
- The settings-toggle joke communicates benefits instantly.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static A | PDP screenshot: Chelsea Herringbone, real ★ rating, "Any 7 for $85", "Waterproof ✓" | — |
| Static B | iOS Settings: "Take jewelry off to shower: OFF", "Green neck: OFF", "Compliments: ON" | — |
| Static C | TikTok comment: "where is your necklace from??" + reply | — |

### Hooks

- Settings: "Take jewelry off before shower: OFF"
- "where is your necklace from??" (comment screenshot)

### Production recipe

1. Use only real ratings and real comments (with consent).
2. Design 3 UI types; keep native fonts and spacing.
3. Avoid mimicking a platform so closely that it implies an endorsement.

### Existing bot prompt

```
Create copy for 6 UI-screenshot statics for LC: PDP mock, Settings toggles, TikTok comment + reply, Trustpilot card (real review), Google search "waterproof gold necklace that doesn't turn green", an email from the founder. Real data only.
```

### Variants to test

- UI type

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @FedotOff90 (151L/268BM/11kV): Statics that do not look like ads: Notes, iMessage, Reddit, tweet, email, app settings, breaking news, fake product page; 200 on one board + Native Statics Mach — https://x.com/FedotOff90/status/2106046297434374289
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
