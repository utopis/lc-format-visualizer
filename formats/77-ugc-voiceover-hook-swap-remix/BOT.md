# BOT.md · generate a "UGC voiceover remix (one creator clip, 10 swapped VO hooks)"

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
5. Name every asset `F77-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F77
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

Take one winning UGC or B-roll clip and lay a professional or AI voiceover on top, swapping only the first 3-5 seconds to test many hooks. The VO controls the claims (compliance-friendly), and footage costs nothing extra.

### Why it works

- The hook is the biggest lever, so testing 10 hooks on proven footage is cheap and fast.
- No new usage rights or reshoots needed (when the license covers edits).
- VO keeps claims consistent and PDP-exact.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | Same winning footage | VO hook variant 1-10 |
| 3-30s | Unchanged body | Shared VO body |
| End | Offer card | "Any 7 for $85" |

### Hooks

- 10 hooks from the F34/F54/F71 banks

### Production recipe

1. Confirm the creator license covers edits and VO.
2. Write 10 hooks; record VO (human, or AI with disclosure where needed).
3. Export 10 cuts and name them F77-<clip>-<hook>.

### Existing bot prompt

```
For LC clip {{CLIP_DESC}} (transcript {{TRANSCRIPT}}), write 10 alternative 3-second VO hooks across these types: callout, contrarian, regret-discovery, side effect, number. Keep the body VO unchanged.
```

### Variants to test

- Hook type
- Human vs AI VO

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @HenryCrochemore (44L/55BM/4kV): ai podcast ads might be one of the easiest ways to make ugc feel native again instead of generating another creator holding a product put them behind a micropho — https://x.com/HenryCrochemore/status/2089291503919087933
- @blvckledge (30L/57BM/4kV): for anyone looking to crack cold traffic on demand gen many of our brands are spending $10k-$20k/day rn we use a strategy framework to iterate and ship new crea — https://x.com/blvckledge/status/2089880028440133945
- @sleepclip (41L/46BM/2kV): no F*CKING way this app scaled from $1k to $500k off ai videos all it took was ai videos of different animals and characters that crossed millions of views. the — https://x.com/sleepclip/status/2102703772354875719
- @OriSilver (34L/44BM/2kV): 📂 THE AI AD FACTORY ┃ ┣ 📂 Research ┃ ┣ 📂 Audience & Pain Points ┃ ┣ 📂 Failed Solutions ┃ ┣ 📂 Objections & Misconceptions ┃ ┣ 📂 Voice of Customer ┃ ┣ 📂 Competito — https://x.com/OriSilver/status/2094742070468730903
- @adamtaylorl (17L/9BM/3kV): Fully agree. Most brands have a winning ad they haven't made yet and the footage is already sitting on a hard drive. But there's a reason this works that most p — https://x.com/adamtaylorl/status/2103439375787003983
