# BOT.md · generate a "Notification / lock-screen 2-slide slideshow"

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
5. Name every asset `F03-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F03
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

2 slides. Slide 1: aesthetic AI/lifestyle visual with an iPhone lock screen overlay showing 2-4 push notifications written in a witty/brutal brand voice ("Right now is another chance to become who you want to be"). Slide 2: the "app comes in naturally" — product/app screenshot or a single line. ([@brainextends](https://x.com/brainextends/status/2099496707209994736), [@enzoxmotion](https://x.com/enzoxmotion/status/2099622190970712321)).

### Why it works

Feels like a meme/screenshot, instantly readable, relatable voice; 2 slides = high completion.

### Hooks

Lock-screen time + 3 notifications from the brand: affirmation, call-out, joke. "your necklace texted you", "notifications from your jewelry box".

### Production recipe

Figma/Canva lock-screen template (generic iOS-style, no Apple logos), AI background (consistent palette), copy generated in batches of 50 by Claude in LC voice, human-edited. 
Prompt: *"Write 30 sets of 3 lock-screen notifications from 'Louise Carter' (jewelry) to its owner. Voice: warm, teasing best friend. Themes: showering with jewelry on, beach days, compliments, stacking, Monday. Max 70 chars each. No false claims; jewelry is 14K PVD waterproof."*

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @brainextends (265L/497BM/16kV): 2-slide slideshow, AI visuals + phone-notification copy -> 1M views, app $1k->$5k/mo. — https://x.com/brainextends/status/2099496707209994736
- @enzoxmotion (208L/378BM/13kV): Same 2-slide notification-style slideshow case ($1k->$10k MRR claim). — https://x.com/enzoxmotion/status/2099622190970712321
- @Just_sharon7 (339L/8BM/38kV): This is the slideshow system people keep skipping. Don’t start from “give me 20 viral ideas.” Start from a format that’s already winning, then let ChatGPT Astra — https://x.com/Just_sharon7/status/2098089273123848524
- @defileo (27L/34BM/6kV): I CAN'T F*CKN BELIEVE SOMEONE LEAKED FULL TIK-TOK AUTOMATION STACK 20M views across six videos, one of them did 7.5M and pulled 3.3K followers, and the whole th — https://x.com/defileo/status/2103190977678877006
- @Voxyz_ai (15L/34BM/4kV): > someone built an AI marketing team for their app with 𝟱 𝗚𝗿𝗼𝗸 𝗕𝗼𝘁𝘀. the content playbook behind it had already pulled 𝟮𝟬𝗠+ 𝘃𝗶𝗲𝘄𝘀 across six videos. now the who — https://x.com/Voxyz_ai/status/2103144930655051824
