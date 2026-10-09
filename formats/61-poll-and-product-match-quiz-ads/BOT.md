# BOT.md · generate a "Poll-sticker & product-match quiz ads (interactive A/B polls → retarget by answer)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: Story ad with a poll sticker, or a quiz-funnel static), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@f3dericobartoli](https://x.com/f3dericobartoli/status/2039638255537201662) · Four statics a creative team made for a quiz funnel. One is an iMessage thread: "I finally looked into the hair thing. Took some quiz. Turns out it's not even about growth..." Another is an editorial 'New research' card. Each ad's job is to get people to start a quiz, which then matches them to a product.
- Example: [@frugalfreebies](https://x.com/frugalfreebies/status/1801654197462479132) · This or that? Which one would you pick for Father's Day? OneStopPlus Clearance Sale! - As low as $4.98! PLUS: Save 50% with code: KSESITEWIDE https://
- Example: [@ZeeNunewTikTok](https://x.com/ZeeNunewTikTok/status/1927734140985541103) · Tag Booster ‼️ Lats play This or that Jewelry edition. Tell us your choices in the comments. Please remember to use the hashtag and keyword. KazzMag19
- Example: [@codyschneider](https://x.com/codyschneider/status/2093098436069568758) · an AI agent is running facebook ads for a local business it just got the 2170 ebook downloads in august 16% of people who download the ebook turn into
- Example: [@zakburgers](https://x.com/zakburgers/status/2082826379863707993) · working with the biggest peptide players gave me huge experience in the segmentation game for emails creating 10 different angle flows for these brand
- Example: [@codyschneider](https://x.com/codyschneider/status/2093096255786234158) · an AI agent is running this local business facebook ads it got the 2170 ebook downloads 16% of people who download the ebook turn into a future patien
- Example: [@JamesEbringer](https://x.com/JamesEbringer/status/2081462841052151919) · Facebook CPCs in Africa are $0.05 right now Five cents a click Go inside TAP and look for the Africa Ads Method Set up a Facebook ad account Point a s

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Story frame 1 | Two necklaces side by side | Poll sticker: "Paperclip or snake chain?" |
| Story frame 2 | Result reveal next day | "62% said paperclip. Here's how to style it." |
| Quiz static | iMessage-style screenshot | "Took a 30-second quiz and it picked my stack." |
| Retarget | Ads by answer: paperclip voters see paperclip stacks | - |

### Prompts

**Meta**

```
Instagram Stories ad with the poll sticker (available in Ads Manager for Stories placements); build engaged audiences by answer.
```

**Quiz (Octane AI / Typeform)**

```
5 questions (style, metal tone, budget, occasion, sea or city), result = a 7-piece stack with an add-all button.
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
- [ ] Files named `F61-<concept>-<variant>`; tracking tag `utm_content=F61-<concept>-<variant>`.
- [ ] Avoid: Polls only work in Stories placements.
- [ ] Avoid: The quiz result must be a real, buyable stack.
- [ ] Avoid: Keep quizzes under 6 questions.

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
5. Name every asset `F61-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F61
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

Interactive creatives: a two-option poll sticker on a Story/Reel ad ("Herringbone or paperclip?") and/or a short product-match quiz ("Find your stack in 30s") as the destination. Answers create segments you retarget with matching creative.

### Why it works

- Low-friction participation lifts engagement and gives first-party preference data.
- Retargeting by answer = personalised follow-up creative.
- Quiz → personalised result page reduces choice paralysis for a 7-piece bundle.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Story ad | Two pieces side by side; poll sticker "Which would you wear daily?" | — |
| Retarget A | Ad featuring the chosen piece + "you picked herringbone" | — |
| Quiz | 5 questions (style, metal, occasion, budget, recipient) → "Your 7-piece stack" | Optional email for results |

### Hooks

- "Herringbone or paperclip? Vote."
- "Gold every day or only weekends?"
- "Find your 7-piece stack in 30 seconds"

### Production recipe

1. Polls: Stories ads with poll sticker (Meta supports polls on Reels/Stories ads).
2. Engagement custom audiences by answer where available; else retarget engagers with both variants.
3. Quiz: 5-7 questions on LC site (strategy 04), result = curated 7-piece cart.

### Existing bot prompt

```
Write 10 two-option poll prompts for LC (style/metal/occasion debates) and a 6-question product-match quiz mapping answers to {{SKUS}} → a 7-piece result + copy.
```

### Variants to test

- Poll vs quiz
- Story vs Reel placement

## Reference examples

See [examples/README.md](examples/README.md) (15 posts). Top 5:

- @f3dericobartoli (0L/0BM/0V):  — https://x.com/f3dericobartoli/status/2039638255537201662
- @IgorWoorts (110L/147BM/6kV): There is NO single landing page that works best for all your ads. It all depends on the awareness stage. Unaware → listicle / quiz funnel (educate around the pr — https://x.com/IgorWoorts/status/2084623022649188607
- @codyschneider (67L/92BM/7kV): an AI agent is running facebook ads for a local business it just got the 2170 ebook downloads in august 16% of people who download the ebook turn into a future  — https://x.com/codyschneider/status/2093098436069568758
- @lorenzo_pravata (28L/21BM/3kV): We scaled an app from $0 to $50M in 10 months on Meta. The peak month did $3M, counting first purchases only. Subscription LTV came on top of that. And here's t — https://x.com/lorenzo_pravata/status/2079684588620664861
- @JamesEbringer (8L/13BM/2kV): Facebook CPCs in Africa are $0.05 right now Five cents a click Go inside TAP and look for the Africa Ads Method Set up a Facebook ad account Point a simple ad a — https://x.com/JamesEbringer/status/2081462841052151919
