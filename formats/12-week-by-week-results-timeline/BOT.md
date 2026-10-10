# BOT.md · generate a "What happens if you…" week-by-week timeline (30-second funnel)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 30-75s, 1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@tryatria_AI](https://x.com/tryatria_AI/status/2106069700950294836) · A Pixar-style girl character in a timeline story about 75 seconds long. A provocative opening, then week-by-week scenes (bloating, a swirling gut visual, ingredients on a table), ending on the product pouch (Ankhwa). Captions mark each week.
- Example: [@HenryCrochemore](https://x.com/HenryCrochemore/status/2014687698687062069) · $180k+ didn’t come from explaining beauty it came from warning most beauty ads soothe ingredients benefits “you’re fine, just glow more” this one didn
- Example: [@ZedNilm1](https://x.com/ZedNilm1/status/2076276174754316716) · female beauty scare ads convert stupidly fast because they don’t educate they show the future your customer is afraid of not “get glowing skin” more l
- Example: [@infovincentt](https://x.com/infovincentt/status/2094897333573918887) · yet another health and wellness brand pulling formats straight from organic health content except this one is using a few at once first it uses the cl
- Example: [@TopDealsHq](https://x.com/TopDealsHq/status/2025474734440292568) · Day 1 vs Day 30… This Is What Changed “ad” (https://linktr.ee/ecohealthdaily) #FootCareRoutine #HealthyNailHabits #SelfCareOver35 #ToenailCareTips #UG
- Example: [@skytookie](https://x.com/skytookie/status/2100679695973134683) · hey chat! as you may have seen, I've played in a few creator tournaments recently, and one thing I noticed is... there's ALWAYS a radiant or immortal 
- Example: [@Kolskithenerd](https://x.com/Kolskithenerd/status/2078167446196777289) · Most healthcare ads lead with fear. I wanted to see what happens if you don't. Spec project: a full ad copy system for @AskAwaDoc , a WhatsApp-based A

### Live paid ads in this format (8 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Feel Mighty: "Car chats" one-month update yapper (gifted, then hooked)** (341 days live): "Welcome to a new episode of car chats… I have been taking the mighty mushroom gummies for over a month now… initially these were sent to me as PR." 103 s.
- **Sports Illustrated: Your Body's Been Keeping Score.** (28 days live): "If a man who drinks alcohol regularly started taking one sachet of IM8 every morning for three weeks, this is what would happen. After the first few days, his gut starts to settle…" An X-ray body animation, then a day-by-day montage. Run from the **Sports Ill
- **Thrillist: You Drink More Than You Think.** (28 days live): "I counted every drink for 30 days, no judgement, just tallying, with one sachet each morning. The number did the persuading." Glass-count graphics over evening scenes, then an AI-UGC talking head. Run from the **Thrillist** page (#ad).
- **Resilia · Vascular Wellness Report: “A-Blood pressure took a lot of pressure on the blood pressure for two…”** (10 days live): Opens: “A-Blood pressure took a lot of pressure on the blood pressure for two months. Here's what happened, day one.”
- **Resilia · Ancient Remedy Co: “Here's what happens to your belly pooch if you it wild oregano oil…”** (1 days live): Opens: “Here's what happens to your belly pooch if you it wild oregano oil every single day for eight weeks week one you don't feel a thing and you figure you got scammed another supplement that does nothing…”
- **Resilia · Arterial Health Review: “What happens if you don if you don't clean out your arteries once they…”** (1 days live): Opens: “What happens if you don if you don't clean out your arteries once they start to clog? Day one, you feel completely normal, exactly like you have for years, but inside it has already begun.”

**Do not copy (seen in these live ads):** The health timelines include unsupported disease claims ("flushes calcium off artery walls"). Do not copy the claims.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | Provocative hook over a character close-up (real or Pixar-style) | "What happens if you never take your necklace off for 30 days?" |
| Week 1 | Small, believable change; caption "WEEK 1" | "Week 1: I forgot I was wearing it." |
| Week 2 | Real situation (shower, gym) | "Week 2: shower, gym, sea. Still gold." |
| Week 3 | Social proof moment | "Week 3: two people asked where it's from." |
| Week 4 | Result + product | "Week 4: it looks like day one." + offer |

### Prompts

**Pixar-style frames (Midjourney)**

```
3D animated style woman, warm Pixar lighting, standing in a steamy bathroom touching her gold necklace, week 2 of a story, consistent character --cref [ref] --ar 9:16
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
- [ ] Files named `F12-<concept>-<variant>`; tracking tag `utm_content=F12-<concept>-<variant>`.
- [ ] Avoid: Keep week 1 small; a huge week-1 result destroys believability.
- [ ] Avoid: Every week claim must match what the product really does; no invented testimonials.
- [ ] Avoid: Label AI visuals.

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
5. Name every asset `F12-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F12
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

### Production recipe

Real creator 30-day diary (best) or AI animated (F05). Metric hold to 75%, CPA, Omni.

## Reference examples

See [examples/README.md](examples/README.md) (7 posts). Top 5:

- @tryatria_AI (221L/410BM/18kV): 30-second funnel: provocative hook then week-1..week-4 storyline of results. — https://x.com/tryatria_AI/status/2106069700950294836
- @MaximilianMoj (0L/0BM/0V): Resilia "$36M/month" (unverified) top 5 ads via Playhead teardowns: candida, aged garlic 4-week arteries, GLP-1, urgency (8 at once), animated explainer. — https://x.com/MaximilianMoj/status/2101002307160731848
- @Salifsibane16 (0L/0BM/0V): 3 AI song-ad story frameworks: bumping into ex (start at end), week-by-week timeline, cheating → self-improvement. — https://x.com/Salifsibane16/status/2099891350015512903
- @skytookie (249L/69BM/16kV): hey chat! as you may have seen, I've played in a few creator tournaments recently, and one thing I noticed is... there's ALWAYS a radiant or immortal popping of — https://x.com/skytookie/status/2100679695973134683
- @ZedNilm1 (43L/62BM/4kV): female beauty scare ads convert stupidly fast because they don’t educate they show the future your customer is afraid of not “get glowing skin” more like “this  — https://x.com/ZedNilm1/status/2076276174754316716
