# BOT.md · generate a "DM-screenshot story slideshow (a chat people binge, the app/product on the slide that changes what happens next)"

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
5. Name every asset `F103-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F103
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

A TikTok photo slideshow made of **chat screenshots** that tell a story people want to finish (a flirt, a fight, a group chat meltdown). Somewhere in the middle, one slide shows the app/product **changing what happens next** (the AI writes the reply; the necklace is the thing she sends a photo of). Even the posts where the story goes badly do numbers, because the story is the content.

### Why it works

- Chat screenshots are native and instantly readable; people read every bubble.
- Story tension (will she reply?) drives swipes to the end, which TikTok rewards.
- The product slide sits at the turning point, so it is remembered as the cause of the outcome.
- Recurring hook ("part 7 of texting my ex with…") turns it into a series people follow.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Slide 1 | Hook slide: chat header + first message | "my sister-in-law has never once complimented me. until today:" |
| Slide 2 | iMessage: SIL: "ok where is that necklace from" | — |
| Slide 3 | Her reply draft; she hesitates | "do I tell her or gatekeep" |
| Slide 4 | Product slide: photo of the necklace in the shower (the photo she sends) | "14K PVD, I literally shower in it" |
| Slide 5 | SIL: "ordering rn. matching for the wedding??" | — |
| Slide 6 | Cliff/CTA | "part 2: she ordered the same one 😭" |

### Hooks

- "my sister-in-law has never complimented me. until today:"
- "group chat when I said my jewelry is waterproof"
- "texting my mom pics of my necklace after 6 months in the ocean"
- "part 3 of the bridesmaid chat"

### Production recipe

1. **Story bank:** 20 short chat plots from real customer DMs/reviews (with permission, names changed): compliments, gifting, bridesmaids, mother-daughter, "you're swimming in that??".
2. **Make the screens:** build chats in a mock-iMessage generator or Figma template; real-looking timestamps, battery, carrier.
3. **Product slide** at slide 4 of 6 (the turning point), using a real LC photo.
4. **Series:** post as "part N", same account, same characters.
5. **Disclosure:** label as a dramatisation in the caption ("based on DMs we get").

### Existing bot prompt

```
Write 12 six-slide chat-screenshot stories for Louise Carter. Each: the chat participants (first names only), 5-7 bubbles total, the turning-point slide where an LC piece (from {{CATALOG}}) changes the outcome, and a 'part 2' teaser. Stories must be plausible and based on these real review themes: {{REVIEW_THEMES}}. Caption must say it is a dramatisation.
```

### Variants to test

- Product slide position (3 vs 4 vs last)
- Series vs one-off
- iMessage vs WhatsApp vs IG DM look
- Happy vs savage ending

## Reference examples

See [examples/README.md](examples/README.md) (2 posts). Top 5:

- @leonclipping (449L/765BM/37kV): Faceless relationship page: same couple photo every post, 'rules we made after a fight' slides, app plug as bonus tip; 1.7M top post. — https://x.com/leonclipping/status/2104660939069170110
- @rsalimx (40L/52BM/3kV): Nah bro, this is genuinely crazy 😭 this ai rizz app is doing $100k/mo off tiktoks that look like memes every post is just his dms with girls, and one slide in t — https://x.com/rsalimx/status/2103184083467837553
