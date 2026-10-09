# BOT.md · generate a "AI song / singing story ad (Suno-style music-video ad)"

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
5. Name every asset `F04-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F04
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

A full original song (30s to **4 minutes**) whose lyrics tell a relatable story — usually a woman's emotional problem → turning point → product as the quiet hero. Visuals are AI-generated scenes (realistic, Pixar-3D, or animated) cut to the lyrics, captions on screen like a lyric video. Product often **not revealed until late** (minute 3 in @therahulissar's winner). Variants:
- **Ballad/drama** (Smooche): "Lisa poured the wine and I started crying… he left, and I'm the one who looks like she lost… Lisa has been a dermatologist for 15 years… Sit down, I brought something" (transcript from @EcomSapo's example).
- **Comedic/rap** (Ecombos example): "3 a.m. wide awake… got home and saw my wife laughing with the neighbor".
- **Long-form Pixar 3D skit + song** (RYZE, @lifemaximised).
- **Male-angle cold open** (@qwertyu_alex's 5x ROAS ad, transcript): "I caught my wife in bed with a trainer. He was 26. I was 45" — a sung confession as the hook.
- Targeting women 45+ by naming insecurities (7 Suno links, @LachezarVoynov) — LC should use aspiration, not insecurity.

Shot-by-shot (60-90s cut):
0-3s cold open lyric line that is a hook statement ("I took it off for the wedding photos…") over an emotional close-up · 3-30s verse: the problem scenes · 30-45s chorus: turning point (friend/sister gives the gift) · 45-70s verse 2: life after (compliments, confidence) · 70-90s outro: product name sung once + on-screen offer.

### Why it works

Songs are watched to the end (retention), emotionally sticky, feel like content not ads; novelty in feed; music lets you say a lot without a talking head. Long run-time works because Meta optimises on purchase, not view length.

### Hooks

First lyric = story conflict; sung confession; "I didn't know…"; question sung over silence; very specific scene (wine, wedding photos, airport).

### Production recipe

1. Claude: write story brief from real review mining (top 20 LC 5-star reviews) → lyrics (verse/chorus/verse/outro, 120-180 words) with product named once.
2. Suno (paid plan with commercial rights) → generate 6-10 takes, pick 1. Optional: ElevenLabs for spoken bridge.
3. Visuals: Midjourney/Nano Banana keyframes with one consistent heroine → Kling/Seedance/Veo image-to-video 5-8s shots; or Pixar-style per F05.
4. Edit in CapCut: lyric captions, beat cuts, 9:16 + 4:5, real product shots for the reveal (use LC product footage, not AI-rendered jewelry, to avoid misrepresenting the product).
Cost ~$10-60 + 2-4h. Make 3 songs per concept (different genres), not 30 hook variants.

## Reference examples

See [examples/README.md](examples/README.md) (31 posts). Top 5:

- @LachezarVoynov (396L/1453BM/88kV): 29 TOF video ad formats to test on Meta (transformation, Suno song, skit, beginner-intermediate-expert...). — https://x.com/LachezarVoynov/status/2086842038457098499
- @adamtaylorl (357L/463BM/29kV): Smooche creative to study. — https://x.com/adamtaylorl/status/2107425650478829611
- @LachezarVoynov (119L/340BM/10kV): 7 Suno song ad examples selling to women 45+ (links). — https://x.com/LachezarVoynov/status/2100612763487740236
- @EcomSapo (157L/220BM/24kV): Smooche ($22M/mo skincare) uses singing ads as acquisition weapon. — https://x.com/EcomSapo/status/2105288429873528875
- @rayjbjang (155L/207BM/21kV): 9-fig founder group chats sharing singing animation ads - format printing. — https://x.com/rayjbjang/status/2085447071990251986
