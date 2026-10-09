# BOT.md · generate a "AI song / singing story ad (Suno-style music-video ad)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 60-90s cut (test 30s and 3-4 min too), 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@lorenzo_pravata](https://x.com/lorenzo_pravata/status/2105684266457637009) · A Pixar-style 3D story about 70 seconds long. A lonely pink character sits by a door under the caption "2 YEARS AND NOBODY LOOKED AT THIS" and narrates ("I'm the one downstairs", "Then one winter", "And she decided I moved out") while a couple lives their life upstairs. It ends with the character wrapped in a blanket: "I'm COLD...". Every line has big centred captions; the product is the quiet ans
- Example: [@lifemaximised](https://x.com/lifemaximised/status/2100659903488819256) · RYZE ($25M+/mo) AI song ad library breakdown.
- Example: [@therahulissar](https://x.com/therahulissar/status/2102465180567543939) · 4-min AI song video, product not revealed until minute 3 - winner.
- Example: [@mkwizrd](https://x.com/mkwizrd/status/2088293230450512089) · Brand reports AI song ad driving big order.
- Example: [@manojbash](https://x.com/manojbash/status/2102083500052795710) · Suno Ai Song Ads are absolutely ripping for us Launched this ad few months back and it's still the top spender If you haven't tried it yet give this a
- Example: [@Diego_exits](https://x.com/Diego_exits/status/2100215847427944464) · 13k Active Meta ads and 17.000.000 MRR 🤯 AI SONG ADS for RYZE SUPERFOODS are cooking rn MILLION DOLLAR DAYS type potential on this format haha - doesn
- Example: [@qwertyu_alex](https://x.com/qwertyu_alex/status/2107923415650701515) · there's so many winning variations of song ads that prints! here are 4 products running their own style of song ad 1. coffee alternative 2. body butte
- Example: [@vladdubchak_x](https://x.com/vladdubchak_x/status/2107131198145204441) · You waste hours making one AI song ad because you did not do a timing map A timing map gets claude to listen to the song and map what word is said in 

### Live paid ads in this format (5 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Smooche · Cosmetic Times: “I lost the weight, I cut the body The body I had chased for ten long…”** (18 days live): Opens: “I lost the weight, I cut the body The body I had chased for ten long years The my best friend looked at my face And said, honey If you were famous people It's where you had been replaced by a local…”
- **Resilia · Active Longevity Review: “I matched with the baddest woman I've ever met Had her in my bed, her…”** (1 days live): Opens: “I matched with the baddest woman I've ever met Had her in my bed, her body pressed against mine Begging me with her eyes And my d*** is laid dead like a f***ing coward Let me tell you what happened…”
- **Resilia · Gut Health Insider: “The man who touched my chin and laughed It feels like touching a guy…”** (1 days live): Opens: “The man who touched my chin and laughed It feels like touching a guy Four months later, Brought him a night He looked once and twice Stood frozen by the door You look nothing like before And all I…”
- **Resilia · Gut Health Insider: “I'm feeling it all, hit their bodies the same Worked the same stress…”**: Opens: “I'm feeling it all, hit their bodies the same Worked the same stress but stayed lean it made no sense By year five, I gained 80 pounds doin' the same job Blow it, swollen, tired lookin' like the…”
- **Resilia · Blood Sugar Wellness: “He came with me, but left with my best friend I met him at a coffee…”**: Opens: “He came with me, but left with my best friend I met him at a coffee shop, on a Tuesday He came up to my table and asked if I wanted to grab a cup We satin' and now we're gonna walk down I was already…”

**Do not copy (seen in these live ads):** Some of the lyrics are explicit or body-shaming. Keep ours brand-safe.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Emotional close-up of the heroine (AI image-to-video, slow push-in) | Sung cold-open lyric that is a confession: "I took it off for the wedding photos..." Lyric caption centred, 2 lines max |
| 3-30s | Verse 1: 4-6 problem scenes, 4-6s each, cut on the beat | Lyrics name concrete moments (the green ring mark, the drawer of broken chains) |
| 30-45s | Chorus: the turning point, a friend/sister hands her the gift | The hook line of the song repeats here; this is the line people remember |
| 45-70s | Verse 2: life after, compliments, swimming, the daughter's graduation | Lyrics show proof through other people noticing |
| 70-90s | Outro: REAL product footage (not AI) on skin, then end card | Product name sung once; on-screen offer + "AI-generated visuals" label |

### Prompts

**Suno (v4.5+, paid plan with commercial rights)**

```
Style: emotional female pop ballad, piano and strings, 82 bpm, intimate close-mic vocal, builds at chorus. Lyrics: [paste verse/chorus/verse/outro, 120-180 words, product named once in the outro].
```

**Midjourney (keyframes)**

```
cinematic still of a 38-year-old woman sitting on the edge of a bathtub holding a tarnished necklace, soft window light, shallow depth of field, Pixar-adjacent 3D or photoreal (pick one and keep it), consistent character --cref [heroine image] --ar 9:16
```

**Kling 2.x / Seedance / Veo (image-to-video)**

```
5s, slow dolly-in, subtle hand movement, no camera shake, keep face consistent, no text
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
- [ ] Files named `F04-<concept>-<variant>`; tracking tag `utm_content=F04-<concept>-<variant>`.
- [ ] Avoid: Generate 6-10 song takes and pick one; the first take is almost never the one.
- [ ] Avoid: AI-rendered jewelry misrepresents the product. Use real product footage for every shot where the piece is visible up close.
- [ ] Avoid: Lyrics that insult the viewer (insecurity angles) can win on supplements but damage a gifting brand; aim at aspiration.
- [ ] Avoid: Only use music you have commercial rights to; do not imitate a real artist's melody or voice.

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
