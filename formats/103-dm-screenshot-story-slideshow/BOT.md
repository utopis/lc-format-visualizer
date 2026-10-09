# BOT.md · generate a "DM-screenshot story slideshow (a chat people binge, the app/product on the slide that changes what happens next)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 6-slide TikTok photo slideshow (1080x1920), chat screenshots), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@rsalimx](https://x.com/rsalimx/status/2103184083467837553) · The TikTok profile of "Rizz Commander" (@rizz.commander): 14.1K followers, 325.3K likes. The "Baddie Rizz" playlist is a grid of slideshow posts with NBA press-conference meme covers ("Shooting my shot on ig (mvp season)") at 2M, 1.1M, 279K, 230K and 222K views. Each slideshow is a DM screenshot story, and one middle slide shows the app writing the reply. The format is meme cover, then DMs, then t
- Example: [@leonclipping](https://x.com/leonclipping/status/2104660939069170110) · this girl might be a fucking genius she built a relationship page around the same couple photo on every post, posts simple "rules we made after a figh
- Example: [@jaxxdwyer](https://x.com/jaxxdwyer/status/2073376584564871455) · One of our creators hit 450k views less than 72hrs after creating her IG account Here's the UGC format that got immediate traction: Text hook + long t
- Example: [@marsdiiaryy](https://x.com/marsdiiaryy/status/2090988603451084990) · that wrong dm slideshow trend on tiktok… #TRANSCENDINGTHEGAME
- Example: [@laurgrowth](https://x.com/laurgrowth/status/2103981166118486250) · the most underused format in affiliate marketing right now is the text message thread and for GTA 6 content it is going to be one of the highest conve

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Slide 1 | Chat header (contact name "Sister-in-law 🙄") + first bubble | Hook text overlay: "my sister-in-law has never complimented me. until today:" |
| Slide 2 | Her message: "ok where is that necklace from" | — |
| Slide 3 | Typing bubble; overlay text | "do I tell her or gatekeep" |
| Slide 4 | The photo she sends: real LC necklace under shower water | Bubble: "14K PVD, I literally shower in it" |
| Slide 5 | SIL: "ordering rn. matching for the wedding??" | — |
| Slide 6 | Black slide | "part 2: she ordered the same one 😭" |

### Prompts

**Story bank (Claude)**

```
From these review themes {{REVIEW_THEMES}}, write 20 six-slide chat stories (5-7 bubbles total) where a Louise Carter piece changes the outcome on slide 4. First names only. End each with a "part 2" teaser.
```

**Chat mockups**

```
Use a mock-iMessage template in Figma: 9:41 status bar, real-looking carrier, blue/grey bubbles at 17pt SF Pro scaled to 1080 wide, no real phone numbers or photos of real people.
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
- [ ] Files named `F103-<concept>-<variant>`; tracking tag `utm_content=F103-<concept>-<variant>`.
- [ ] Avoid: Label it a dramatisation in the caption.
- [ ] Avoid: Product slide at the turning point, not the end; the end is the payoff.
- [ ] Avoid: Same characters every part, or the series loses followers.

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
