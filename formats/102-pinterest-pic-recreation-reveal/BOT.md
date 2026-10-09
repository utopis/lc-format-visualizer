# BOT.md · generate a "Pinterest-pic recreation reveal (\"I recreated this Pinterest photo with me in it\")"

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
5. Name every asset `F102-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F102
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

Slide/clip 1 is a **saved Pinterest photo** (the aspirational image everyone has on a board), slide 2 is **the creator recreating it**: same pose, light, outfit and, for LC, the same jewelry stack. The reveal is the side-by-side. For the app version (Retake) the app generates the recreation; for a brand it is a styling challenge: *"I recreated my most-saved Pinterest jewelry pics with pieces under $85."*

### Why it works

- Pinterest boards are where the purchase intent already lives; the viewer recognises the aesthetic.
- Side-by-side = before/after without a 'before' that insults anyone.
- Comments ask "do this one next" with their own pins, which writes the next 20 videos.
- For women the desire is identity ("that girl, but me"); the product becomes the bridge.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Slide 1 | Screenshot-style Pinterest pin of a gold-stacked neck/wrist look (own licensed or creator-shot reference; never a stolen photo) | Text: "my most-saved pin for 3 years" |
| Slide 2 | Creator recreating the pose, light and stack with LC pieces | "recreated it with pieces I can shower in" |
| Slide 3 | Close-up of the stack, piece names | "Chelsea Herringbone + 2 paperclip chains + mini hoops" |
| Slide 4 | Split screen: pin vs recreation | "total: any 7 for $85" |
| Slide 5 | CTA | "send me your pin, I'll recreate it next" |

### Hooks

- "Recreating my most-saved Pinterest jewelry looks (under $85)"
- "Pinterest vs me: the gold stack edition"
- "I recreated the 'clean girl' jewelry pin with waterproof pieces"
- "Send me your pin and I'll recreate it"

### Production recipe

1. **Pin sourcing:** use LC's own Pinterest pins, customer UGC (with permission) or creator-shot reference images. Do not repost other people's photos without a licence.
2. **Recreate:** match angle (phone at chest height), light (window, golden hour), outfit colours; jewelry stack from LC.
3. **Format:** 5-slide TikTok photo carousel or 9 s video with a swipe transition; trending sound.
4. **Comment loop:** reply to "do mine" with F18 green-screen recreations.
5. **AI variant (internal test only):** generate lookbook recreations with F20 rules (QC every piece against the real product).

### Existing bot prompt

```
Write 15 'Pinterest vs me' carousel concepts for Louise Carter. Each: (1) describe a typical high-save Pinterest jewelry aesthetic (e.g. 'clean girl gold', 'beach stack', 'bridal minimal'), (2) the exact LC pieces from {{CATALOG}} that recreate it, (3) 5 slide captions (max 9 words each), (4) a comment-bait last slide. No celebrity names or copyrighted images.
```

### Variants to test

- Carousel vs video
- Own pin vs follower-submitted pin
- Price callout on vs off
- Aesthetic category

## Reference examples

See [examples/README.md](examples/README.md) (3 posts). Top 5:

- @ErnestoSOFTWARE (380L/706BM/60kV): This is literally a $1M app idea...😭 This post has over 2 million views and 12k+ comments asking for the app its literally just an app that helps you replicate  — https://x.com/ErnestoSOFTWARE/status/2061578473370501423
- @simonecanciello (56L/65BM/18kV): who’s building this $1M app? take a pic of yourself + pick any pic you want to recreate from pinterest. the app recreates the exact same pic, but replaces the g — https://x.com/simonecanciello/status/2102046332970013078
- @onlinedopamine (34L/39BM/3kV): these are the types of outsized organic views you get on new accounts when you nail &gt; understanding of your target audience (= pinterest aesthetic girlies) & — https://x.com/onlinedopamine/status/2082813772373098530
