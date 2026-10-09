# BOT.md · generate a "Fiction serial native (an episodic short story told across a run of ads)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

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

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @FedotOff90 (210L/592BM/83kV): Pocket FM storytelling drama ads — 199 longest-running; serial episode logic. — https://x.com/FedotOff90/status/2101445743412138341
- @zackpaid (9L/20BM/2kV): 11 AI formats (agency pitch): native UGC, founder, claymation, Pixar 3D, jingle, screen recording, before/after, testimonial compilation, cinematic demo, mini-d — https://x.com/zackpaid/status/2085621175292670183
