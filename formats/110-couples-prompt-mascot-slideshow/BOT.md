# BOT.md · generate a "Couples prompt slideshow with a mascot duo (\"5 slightly uncomfortable questions to ask your boyfriend\", \"this or that\", \"pick who's guilty, comment 1A 2B\")"

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
5. Name every asset `F110-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F110
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

A TikTok or Instagram photo-mode slideshow from a faceless brand account. Every cover uses the **same two cartoon characters**, a "him" and a "her" (the example uses a pig and a cat with a pink bow), on a flat colour background. A short lowercase-feeling headline in bold white sits at the top. Inside are 5-8 slides of **prompts couples answer together**:
- "5 slightly uncomfortable questions to ask your boyfriend (no lying allowed)"
- "this or that: cute but spicy edition (it's safe, we promise)"
- "couples, pick who's guilty (comment like 1A 2B)"

The product (here a couples app) appears on the last slide or in the caption as the place to keep playing. The engine: people **send it to their partner** or **answer in the comments with a code**, and both signals feed distribution.

### Why it works

- **Shareable to exactly one person.** "Questions to ask your boyfriend" begs to be DM'd to the boyfriend, and sends are the strongest TikTok and Instagram signal.
- **Comment codes ("1A 2B")** make commenting effortless, and every comment is a vote, so comments stack.
- **"Slightly uncomfortable" is the dose** (reply under the post): fully uncomfortable gets scrolled past, mildly uncomfortable gets answered.
- **Mascots make it brand-ownable and safe.** The same characters on every cover build recognition (F21), and nobody's face is needed.
- **Cheap to run at volume.** @jackfriks says Claude wrote a day's posts from his reference sheet and taste notes and scheduled and posted them through the Post Bridge MCP.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Slide 1 (cover) | LC mascot duo (e.g. a little gold bear "him" and a bunny "her" with a pearl necklace) on blush pink; headline "this or that: jewelry edition" + "(he has to answer honestly)" | Trending sound, auto-added |
| Slide 2 | Two mascot panels: "gold 🅰️ or silver 🅱️" | — |
| Slide 3 | "dainty 🅰️ or chunky 🅱️" | — |
| Slide 4 | "matching couple rings 🅰️ or never 🅱️" | — |
| Slide 5 | "surprise gift 🅰️ or send-me-the-link 🅱️" | — |
| Slide 6 | "necklace 🅰️ or bracelet 🅱️" | "comment your answers like 1A 2B 3A" |
| Slide 7 | Mascot holding an LC box: "send this to him 👀 (any 7 for $85, link in bio)" | — |

### Hooks

- "5 slightly uncomfortable questions to ask your boyfriend"
- "this or that: [category] edition"
- "couples, pick who's guilty (comment like 1A 2B)"
- "send this to him if you want [X] for your birthday"
- "rate your boyfriend's gift history 1-10"

### Production recipe

1. **Mascot sheet:** generate the duo once (GPT Image / Nano Banana: "two cute chibi characters, thick dark outline, flat pastel shading, a bear and a bunny with a pearl necklace, front-facing, transparent background") and make 8 poses (shy, guilty, pointing, holding a box).
2. **Reference sheet** (Google Doc): 30 example headlines that worked, tone rules (lowercase-feeling, playful, never explicit), banned salesy phrases, a CTA list.
3. **Prompt bank:** Claude writes 20 prompt sets a week from the sheet. Swap the hook families so it doesn't converge on two hooks.
4. **Template:** Canva or Figma 1080×1920, flat colour background per series, white bold headline, mascots at the bottom third.
5. **Post:** schedule via Post Bridge (MCP or UI) or post natively; let TikTok auto-add trending audio; 1-3 a day per account.
6. **Pin a comment** with the answer code legend ("comment like 1A 2B 3A").

### Existing bot prompt

```
Using the LC reference sheet (tone: playful, lowercase-feeling, never explicit, never salesy), write 10 couples-prompt slideshows for the LC mascot duo. Mix 4 families: 'questions to ask your boyfriend', 'this or that: <x> edition', 'pick who's guilty (comment 1A 2B)', 'send this to him'. Each: cover headline (≤8 words) + sub-line, 5-6 slides with one prompt each and A/B options where relevant, final slide CTA (any 7 for $85, link in bio), pinned comment, 3 hashtags. Keep it slightly uncomfortable, never mean.
```

### Variants to test

- Mascot duo versus real couple photo covers
- Comment-code versus "send this to him" CTA
- Pastel background per series versus one brand colour
- AI-written versus human-written hooks (Matt Gittleson: never let AI write hooks; run both)

## Reference examples

See [examples/README.md](examples/README.md) (1 posts). Top 5:

- @jackfriks (0L/0BM/0V):  — https://x.com/jackfriks/status/2108536144896163993
