# BOT.md · generate a "Visual-diagnosis roll-call ('This is X. This is X. That's X.' symptom montage → hidden cause)"

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
5. Name every asset `F95-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F95
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

The ad opens on a rapid montage of everyday symptoms, each captioned with the same label ("This is clogged arteries"), so the viewer re-attributes many small annoyances to one hidden cause. Then it explains the cause (often with CGI) and presents the one product that "reaches" it. Resilia calls the move cause relocation: every complaint gets the same root.

### Why it works

- Repetition plus a visual makes the reframe stick in 5 seconds, even muted.
- The viewer self-diagnoses: "I have that one".
- One cause absorbs many symptoms, so one script reskins for dozens of avatars and pages.
- Works as hooks for statics, carousels and long VSLs alike.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0:00-0:06 | Quick cuts: green ring line on a finger, dull chain, flaking gold on a hoop, a rash under a pendant | On-screen + VO each time: "This is plating." |
| 0:06-0:25 | Macro or CGI: thin gold paint on brass, worn through by water and sweat | "Plating is a layer of gold paint thinner than a hair. Water gets under it." |
| 0:25-0:45 | Bonded PVD explainer + shower demo | "14K PVD is bonded to steel. Nothing to wear off." |
| 0:45-0:55 | Offer | "Any 7 for $85. Never take it off." |

### Hooks

- "This is plating. This is plating. This green line? Plating."
- "If your necklace does this, it was never gold."
- "Every one of these is the same problem."

### Production recipe

1. List 5-6 visible jewelry "symptoms" (green ring line, dull chain, flaking, itchy rash, broken clasp after the pool).
2. Shoot each as a 1-second macro shot; caption with the same label.
3. Reveal: plating vs bonded PVD in one sentence + demo.
4. Make a static carousel version (one symptom per card).

### Existing bot prompt

```
Write 3 visual-diagnosis roll-call hooks for LC: 5 one-second jewelry "symptoms" each captioned with the same label, then a 2-sentence cause explanation (plating wears through) and the LC fix (bonded 14K PVD). No health claims (do not imply allergies are cured).
```

### Variants to test

- Label wording
- Montage length 4 vs 8 s
- Real photos vs CGI

## Reference examples

See [examples/README.md](examples/README.md) (4 posts). Top 5:

- @lorenzo_pravata (0L/0BM/0V): Resilia 6,000 ads, parasite cause-relocation angle, "That's parasites" roll-call, carvacrol gate; 10+ subpages to avoid bans. — https://x.com/lorenzo_pravata/status/2065407167515984348
- @Network_UCG (70L/9BM/5kV): ☀️ Summer UGC Creator Roll Call! ☀️ Want more brands to discover your portfolio? Drop your link in the comments, follow other creators, and RT to help everyone  — https://x.com/Network_UCG/status/2079759701244338486
- @JenUGCGenX (39L/1BM/1kV): Am I the only one who feels like Gen X creators are still a small part of the UGC community? I see so many younger creators everywhere, but not as many Gen X cr — https://x.com/JenUGCGenX/status/2087962642568860039
- @rollcall (2L/0BM/2kV): The Democratic Congressional Campaign Committee is marking 100 days until the midterm elections with a new digital ad shared first with CQ Roll Call. https://t. — https://x.com/rollcall/status/2080621569739518408
