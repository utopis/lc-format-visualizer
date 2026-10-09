# BOT.md · generate a "Fiction serial native (an episodic short story told across a run of ads)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 6-episode serial: 6 image ads with 300-600 words each, sequenced 2-3 days apart), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@adriamatz](https://x.com/adriamatz/status/2108190619449372721) · An Arcads demo of a short-drama ad: office scenes with actors, split with a script panel, styled like DramaBox micro-dramas but built around a product.
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2101445743412138341) · Pocket FM storytelling drama ads — 199 longest-running; serial episode logic.

### Live paid ads in this format (6 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Cosmetic Times: “At 58, I went to my school reunion and barely recognized myself in the…”** (21 days live): Opens: “At 58, I went to my school reunion and barely recognized myself in the mirror that night. I'd been the pretty one back in school, homecoming queen and everyone spotlight.” The same script appears in 2 ads across 1 pages (Cosmetic Times).
- **Smooche · Cosmetic Times: “When your eyelids start hooding, right here, foundation transfers onto…”** (9 days live): Opens: “When your eyelids start hooding, right here, foundation transfers onto the crease all day. And when Jaws drop at your Jaws line, foundationsations for mature skin, they just took the regular formula,…” The same script appears in 2 ads across 1 pages (C
- **Smooche · Korean Beauty Tips: “My husband started turning off the light while we had sex We've been…”** (7 days live): Opens: “My husband started turning off the light while we had sex We've been married for 22 years And I still saw him the way I did when I was 30 But somewhere in the last few years he started flinching when…” The same script appears in 2 ads across 1 pages (K
- **Resilia · Gut Health Insider: “My husband slept with my sister I was four months pregnant I found the…”** (1 days live): Opens: “My husband slept with my sister I was four months pregnant I found the messages on a Saturday morning while he was at the gym The name on his phone with a heart emoji next to it, my own sister The…” The same script appears in 2 ads across 1 pages (Gut 
- **Resilia · Active Longevity Review: “Dad! Look at you. You made it…”** (1 days live): Opens: “Dad! Look at you.” The same script appears in 2 ads across 1 pages (Active Longevity Review).
- **Resilia · Blood Sugar Wellness: “Come on, Dad. Climb with me. Like before…”**: Opens: “Come on, Dad. Climb with me.”

**Do not copy (seen in these live ads):** The characters are presented as real people. Label it as a series or fiction.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Episode 1 image | Illustration or moody phone photo: a woman at an airport gate touching her necklace. Same style every episode | Header text on image: "The Necklace · Episode 1" |
| Ep 1 copy | Labelled "(A short story. Fiction.)" on line 1 | Sets up the character and her problem: her late grandmother's chain turned green the night before her sister's wedding. Ends on a cliffhanger. |
| Ep 2-3 | Same character, new setting each time (sister's house, the beach) | The new necklace is just part of her routine: she showers, swims, forgets it's on. Never a pitch. |
| Ep 4-5 | Tension: someone notices, asks where it's from | Dialogue between characters carries the product facts naturally |
| Ep 6 (finale) | Wedding photo moment | Resolution + a soft line at the end: "The stack in this story is Louise Carter's. Any 7 for $85." |

### Prompts

**Claude (serial)**

```
Write a 6-episode fiction serial, 350-450 words per episode, about [character]. Episode 1 opens with a concrete problem; each ends on a cliffhanger; the product appears as a quiet constant (never pitched) until a 1-line note at the end of episode 6. Label each as fiction.
```

**Midjourney / illustration**

```
editorial illustration, woman in her 30s at an airport gate touching a thin gold necklace, warm muted palette, gouache texture, consistent character --ar 4:5 --cref [ep1 image] --sref [ep1 image]
```

**Meta sequencing**

```
Ep1 to a broad audience; Ep2 to people who engaged with Ep1 (post engagement 7d); and so on. Cap frequency at 2 per episode.
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
- [ ] Files named `F81-<concept>-<variant>`; tracking tag `utm_content=F81-<concept>-<variant>`.
- [ ] Avoid: Label fiction clearly in every ad; never present it as a true story.
- [ ] Avoid: Sequencing needs engagement audiences; without them, people see episode 4 first and the story makes no sense.
- [ ] Avoid: Keep the character consistent (same face and style) or the serial breaks.

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
5. Name every asset `F81-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F81
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

Long-copy image ads that each carry one episode of a story (clearly labelled fiction) with a recurring character. Each ends on a cliffhanger; the product is a quiet constant in every episode. Retarget each episode's readers with the next one.

### Why it works

- Serial cliffhangers bring readers back.
- Fiction is honest when labelled, and it builds affinity.
- Retargeting by episode creates a natural sequence.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Ep1 static | Illustration or photo, "Episode 1: The summer she stopped taking it off" | 1,200-char story, cliffhanger |
| Ep2 | Retarget Ep1 engagers | continues; product appears |
| Ep3 | Retarget Ep2 | resolution + offer |

### Hooks

- "Episode 1: The necklace that went everywhere"
- "A short story in 3 parts"

### Production recipe

1. Write a 3-episode arc; label it "a short story".
2. Ep1 cold; Ep2/Ep3 to engagers.
3. Keep the product a quiet constant, never a pitch, until Ep3.

### Existing bot prompt

```
Write a 3-episode fiction serial for LC (each ≤1,200 characters, ending on a cliffhanger) about a recurring character; the necklace appears in each; Ep3 ends with the offer. Label it as fiction.
```

### Variants to test

- Illustration vs photo
- Weekly vs daily cadence

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @FedotOff90 (210L/592BM/83kV): Pocket FM storytelling drama ads — 199 longest-running; serial episode logic. — https://x.com/FedotOff90/status/2101445743412138341
- @adriamatz (0L/0BM/0V):  — https://x.com/adriamatz/status/2108190619449372721
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
