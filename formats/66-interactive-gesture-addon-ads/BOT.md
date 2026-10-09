# BOT.md · generate a "Interactive gesture add-on ads (TikTok tap-to-reveal, shake-to-reveal, Super Like)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 15-30s TikTok in-feed ad with an interactive add-on), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@ChrisHarihar](https://x.com/ChrisHarihar/status/1703108334218297531) · A TikTok in-feed ad using the 'shake to learn more' interactive add-on (from the Barbie movie campaign): a creator talks to camera, a prompt asks viewers to shake their phone, the screen bursts into a full-screen pink Barbie pattern, then a 'watch it' card with ticket links. The poster says the format works well and has mostly been used for films.
- Example: [@crowizard_stef](https://x.com/crowizard_stef/status/1735569746349670808) · Stores are using TikTok’s new interactive cards already! Don’t fall behind: ​1. Create a new campaign where you select Reach & Frequency as the Ad Buy
- Example: [@coltonjetlee](https://x.com/coltonjetlee/status/1790930807764435387) · For those running TikTok Shop ads... Do you guys turn on a "Interactive Add-on" like a Product Card? We've been using them as TikTok claims it boosts 
- Example: [@_deepakss_](https://x.com/_deepakss_/status/2087895969157246985) · Building "Tiktok for games" Arcadeo for this year's Shipaton. My main aim is to have a non frustrating experience when viewing an ad. This means user 
- Example: [@SOCIALFUELio](https://x.com/SOCIALFUELio/status/2092930152133243178) · ana luisa are running 22 ads. this one has held for 47 days. Using an iOS crop-menu overlay visually programs the exact user behavior needed to claim 

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Creator holds up a closed gift box | "Shake your phone to open it." |
| Shake moment | Gesture add-on triggers a gold burst animation | - |
| 3-10s | Box opens: 7-piece stack | "Any 7 for $85." |
| 10-20s | Demo in the shower | "Waterproof." |
| Card | Product card add-on with price | - |

### Prompts

**TikTok Ads Manager**

```
Add the Gesture / Super Like / Countdown sticker interactive add-on when building the ad (check current availability in your region).
```

**Animation**

```
After Effects or CapCut: 1s gold particle burst, brand colours.
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
- [ ] Files named `F66-<concept>-<variant>`; tracking tag `utm_content=F66-<concept>-<variant>`.
- [ ] Avoid: Add-on availability varies by region and objective; check before you produce.
- [ ] Avoid: The video must work without the interaction too.
- [ ] Avoid: Don't make the gesture the only content.

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
5. Name every asset `F66-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F66
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

TikTok interactive add-ons layered on an existing video ad: a Display Card that reveals an offer on tap, a shake-to-reveal surprise, or branded Super Like icons on double-tap.

### Why it works

- Turns a gesture viewers already make into the ad interaction.
- Good for offers/drops.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Gift box unboxing video | — |
| 5s | Display Card: "Tap to reveal today's stack" | — |
| Reveal | Card with any 7 for $85 | — |

### Hooks

- "Tap to open the box"
- "Shake to reveal your stack"

### Production recipe

1. Add Display Card to winning TikTok video ads; test vs no card.

### Existing bot prompt

```
Write 5 Display Card / gesture concepts for LC TikTok ads with on-card copy ≤8 words.
```

### Variants to test

- Card vs no card

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @SOCIALFUELio (1L/0BM/12V): ana luisa are running 22 ads. this one has held for 47 days. Using an iOS crop-menu overlay visually programs the exact user behavior needed to claim the in-sto — https://x.com/SOCIALFUELio/status/2092930152133243178
- @ChrisHarihar (0L/0BM/0V):  — https://x.com/ChrisHarihar/status/1703108334218297531
- @_deepakss_ (10L/0BM/201V): Building "Tiktok for games" Arcadeo for this year's Shipaton. My main aim is to have a non frustrating experience when viewing an ad. This means user can skip t — https://x.com/_deepakss_/status/2087895969157246985
