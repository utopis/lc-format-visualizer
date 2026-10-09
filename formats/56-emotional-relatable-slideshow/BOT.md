# BOT.md · generate a "Emotional + relatable TikTok slideshow (share-bait story slides)"

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
5. Name every asset `F56-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F56
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

A 4-8 slide photo-mode story built around a relatable emotional moment (a mother, a breakup, a friend's birthday at 5am), told in short first-person lines over candid photos; the product appears naturally in one slide as part of the moment. Optimised for shares and saves rather than clicks.

### Why it works

- Emotion + relatability drives shares (802 shares on 13.3K views ≈ 6% share rate).
- "Put them in the moment" POV openers are among the most-saved hook types.
- Cheap; tests emotional angles before paying for video.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Slide 1 | Candid photo: mom's hands; text "my mom never bought herself jewelry" | — |
| Slide 2 | "she always said 'it'll just turn green anyway'" | — |
| Slide 3 | "so for her 60th I got her one she can wear in the garden, the shower, everywhere" | — |
| Slide 4 | Close-up LC necklace on her | — |
| Slide 5 | "she hasn't taken it off in 4 months" | — |
| Slide 6 | "call your mom" (no hard CTA; product tag/comment pin) | — |

### Hooks

- "It's 5am on her birthday…"
- "my mom never bought herself jewelry"
- "POV: your best friend remembers the necklace you pointed at 8 months ago"
- "things my grandma told me about jewelry"

### Production recipe

1. Write stories from real customer reviews/notes (with permission) or as the brand's/founder's own story.
2. Candid, warm photos (not studio); 6-8 words per slide.
3. Post 1/day on an owned page; pin a comment with the product.

### Existing bot prompt

```
From these real customer stories {{REVIEWS}}, write 8 emotional 6-slide slideshow scripts (≤12 words per slide, first person, the LC piece appears once naturally). Never invent a story and present it as a real customer's.
```

### Variants to test

- Opener type (POV / name the viewer / moment)
- Slide count

## Reference examples

See [examples/README.md](examples/README.md) (12 posts). Top 5:

- @consumerxai (12L/18BM/1kV): 30 most-SAVED app TikTok hooks in 6 types (POV moment, name the viewer, disbelief, signs/lists, result first, pattern interrupt); save rate > views as signal. — https://x.com/consumerxai/status/2107471216126906682
- @g_buildz_apps (7L/5BM/390V): "Post emotional slideshows on TikTok" — one slideshow: 13.3K views, 2,881 likes, 802 shares, 313 saves (TikTok Studio screenshot). — https://x.com/g_buildz_apps/status/2108234459241935255
- @g_buildz_apps (0L/1BM/172V): Emotional slideshows do better every time and convert better (claim). — https://x.com/g_buildz_apps/status/2094812455847309758
- @brainextends (265L/497BM/16kV): 2-slide slideshow, AI visuals + phone-notification copy -> 1M views, app $1k->$5k/mo. — https://x.com/brainextends/status/2099496707209994736
- @rsalimx (76L/122BM/8kV): Claim slideshows convert harder than videos; it's about finding the right format. — https://x.com/rsalimx/status/2090094780864713021
