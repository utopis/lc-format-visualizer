# BOT.md · generate a "AI doctor avatar explainer (white-coat presenter breaks a problem into 'layers', product is the fix for the layer nobody treats)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 60-120s (plus a 3-min long cut), 1080x1920, avatar head-and-shoulders + 1 PiP insert per layer), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@FedotOff90](https://x.com/FedotOff90/status/2106401392374186396) · A 3:28 vertical explainer. A woman in a white coat with a stethoscope sits in a warm home-office set under a fixed top headline: "Chronic bad breath has 3 layers‼️". Word-by-word captions sit mid-frame, and small picture-in-picture inserts pop up for each layer (a tongue close-up, a gloved hand with a scraper, a dropper bottle). Script: "If you want your tongue to look like this, you are only seei

### Live paid ads in this format (6 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Khazanay Pakistan: Clinic presenter in scrubs (orthopedic shoes)** (338 days live): A woman in navy scrubs in a clinic corridor: "Let me tell you that you don't need a new body. You just need better support… it's not always an injury… unsupported shoes… plantar fasciitis". 70 s, run as 2 near-identical ads.
- **Dr. Lisa Downing: "Men's health researcher" podcast (prostate DHT)** (267 days live): "As a men's health researcher, I study why the prostate swells… This is what most men over 40 get wrong about nighttime urination… Block DHT at the source… 3,000 mg cold-pressed pumpkin seed oil with saw palmetto." 54 s. Dr. Lisa Downing page, 1,357 ads.
- **Male Health Tips: Elder "ancient remedy" doctor (men's health, gut-blood-flow claim)** (222 days live): A grey-bearded man in a suit vest holds a dropper bottle; captions read "Dr. Sebi exposed how to increase size QUICKLY". Script: "Most men don't realize… It all comes down to blood flow and what's happening in your gut… berberine and sodium alginate…". 41 s, 2
- **Dr. Amina Siddiq, MD: "Dr. Amina Siddiq, MD" long explainer (skin)** (214 days live): A hijab-wearing presenter in a lab-coat look with before/after skin inserts: "It all comes back to one thing. Your skin is missing… The part most women never realize. Almost all modern moisturizers make this worse." 289 s.
- **Astrid Zeegen: 60-year-old founder quiz talking head (collagen)** (208 days live): A woman of 60 to camera: "Quick quiz. Do you know the difference between marine collagen and bovine collagen? …Does that help your skin, your joints or your gut?" 357 s (with a 392 s sibling).
- **Resilia · Blood Sugar Wellness: AI lab-coat “scientist” pitches cinnamon 1000 mg + berberine** (1 days live): Opens: “to-do-of to be on cinnamon.extract at 1000mg The same daily amount used in clinical studies Paired with 500mg of Burberry HCL I always recommend both pathways together”

**Do not copy (seen in these live ads):** An AI-generated "nutritionist PhD" persona making health claims is deceptive and likely violates platform policy. Do not copy.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| 0-3s | AI specialist (lab coat, 40s, warm studio). Fixed top headline in a white pill: "Why your necklace turns your neck green: 3 layers‼️" | "If your jewelry turns your skin green, it's not your skin." |
| 3-15s | PiP top-right: real green-neck close-up (UGC, with permission). Word-by-word captions mid-frame | "Layer one is what everyone blames: sweat, perfume, sensitive skin." |
| 15-35s | PiP: macro of worn plating flaking off a brass base (stock or own lab shot) | "Layer two is the real cause: a copper or brass base under plating so thin it wears through in weeks." |
| 35-60s | PiP: water beading on a PVD-coated piece (REAL LC footage) | "Layer three is the one nobody fixes: the bond. PVD fuses gold to steel. It doesn't rub off." |
| 60-75s | Full-screen real LC b-roll: shower, pool, sleep | "That's why ours are waterproof. Shower, swim, sleep in them." |
| 75-90s | Avatar returns, offer card lower third | "Any 7 for $85. Link below." End card 2s |

### Prompts

**Script (Claude)**

```
Write a 90-second explainer for Louise Carter in the "[problem] has 3 layers" structure: layer 1 = what people blame, layer 2 = real cause, layer 3 = what nothing fixes → PVD bond. ≤15 words per sentence, 140 wpm, calm specialist voice. Mark one PiP insert per layer. No medical claims, no credentials.
```

**Avatar (HeyGen / Arcads / Captions)**

```
Pick 4 "specialist" avatars: woman 35 lab coat, man 55 smart casual, woman 60 cardigan, woman 28 scrubs-free studio. 9:16 head-and-shoulders, neutral warm background, eye-line to lens. Upload the same script to each; export 1080x1920.
```

**Voice (ElevenLabs)**

```
Stability 50, similarity 75, style 15; "calm, reassuring, slightly slow"; add 0.3s pauses after each "Layer N".
```

**Edit (CapCut)**

```
Fixed headline pill top 12%; captions word-by-word mid-frame (white, black stroke, 58px); punch-in zoom 105% every 5s; PiP 35% width top-right with 0.2s pop; end card 2s.
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
- [ ] Files named `F108-<concept>-<variant>`; tracking tag `utm_content=F108-<concept>-<variant>`.
- [ ] Avoid: Never call the avatar "Dr." or give credentials it does not have: deceptive endorsement.
- [ ] Avoid: Disclose AI-generated people (Meta AI info label / TikTok AIGC).
- [ ] Avoid: Keep layer 3 = product; if the product appears before layer 3 the curiosity loop breaks.
- [ ] Avoid: Use real product macros for every LC shot; AI-rendered jewelry looks wrong and breaks trust.
- [ ] Avoid: Health brands: run claims through a banned-words list; structure-function wording only.

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
5. Name every asset `F108-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F108
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

A single presenter in a white coat (or scrubs) talks straight to camera in a calm clinic or home-office set. The top of the screen has a fixed headline that names the problem and promises structure, for example **"Chronic bad breath has 3 layers‼️"**. Word-by-word captions sit mid-frame. Small picture-in-picture inserts (a mouth close-up, a gloved hand, a dropper bottle) pop up for each "layer". The script **reframes the problem**: what most people think it is (layer 1, "food"), what it really is (layer 2, "hydrogen sulfide / biofilm"), and the layer nothing they have tried touches (layer 3). The product is introduced as the only thing that reaches layer 3. The presenter is fully AI-generated (HeyGen / Arcads / Captions avatar) or an AI-cloned real expert. It runs 60 s to 3.5 min.

It differs from F06 (AI UGC talking head: a "customer" sharing an experience) and F15 (retro infomercial expert: a staged TV set). Here the authority is the **lab coat plus the layered mechanism**. Nobody is giving a testimonial.

### Why it works

- **Authority without a real doctor's calendar:** the white coat, stethoscope and calm delivery borrow trust, and AI makes it about $5-40 per video instead of $3-5K for an expert shoot (Fedotoff: AI formats are $3-6 per ad in credits versus a studio).
- **"It has 3 layers" is a curiosity loop.** The viewer waits for layer 3, and the product sits in layer 3.
- **The reframe gives a graceful exit.** "Most people think it's food" tells buyers their past purchases failed because they were aimed at the wrong layer, not because they were stupid (Fedotoff: "sell the reframe, not the relief").
- **Long holds are fine:** a 3:28 explainer keeps watch time because each layer is a mini-payoff.
- **Scales by persona:** the same script can run on 10 different doctor faces (age, ethnicity, gender) to open new Andromeda pockets (see F97).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-3s | AI "jewelry chemist" in a lab coat, a soft-lit studio, fixed headline "Why your necklace turns your neck green: 3 layers‼️" | "If your jewelry turns your skin green, it's not your skin." |
| 3-15s | PiP: green neck close-up | "Layer one is what everyone blames: sweat, perfume, 'sensitive skin'." |
| 15-35s | PiP: macro of worn plating flaking off brass | "Layer two is the real cause: a copper or brass base under plating so thin it wears through in weeks." |
| 35-60s | PiP: water drop beading on a PVD-coated piece | "Layer three is the one nobody fixes: the bond. PVD fuses gold to steel at the molecular level. It doesn't rub off." |
| 60-75s | Real LC product macro on skin, in water, in the shower | "That's why ours are waterproof. Shower, swim, sleep in them." |
| 75-90s | Avatar + LC offer card | "Any 7 for $85. Link below." |

### Hooks

- "[Problem] has 3 layers, and you've only been treating the first one."
- "Doctors don't tell you this about [problem]."
- "If you've tried [3 things], here's why they didn't work."
- "I'm going to explain [problem] in 60 seconds."
- "Stop blaming [common scapegoat]."

### Production recipe

1. **Script (Claude):** problem → "it has N layers" → layer 1 (what they blame) → layer 2 (the real cause) → layer 3 (what nothing touches) → product = layer 3 → proof → offer. 150-450 words.
2. **Avatar:** HeyGen / Arcads / Captions "doctor" or "specialist" avatar in a white coat, 9:16 head-and-shoulders, neutral clinic background. Make 4-10 faces of different ages and ethnicities.
3. **Voice:** ElevenLabs, a calm and slightly slow delivery; 140-150 wpm.
4. **Inserts:** 1 PiP per layer (stock macro, a real product macro); keep the fixed headline at the top the whole time.
5. **Captions:** word-by-word, white with a black stroke, mid-frame.
6. **Edit:** cuts every 4-6 s (zoom punch-ins), an end card with the offer. Export 60 s, 90 s and a long version.

### Existing bot prompt

```
Write 4 AI-doctor-avatar explainer scripts (60-120 s) for Louise Carter waterproof PVD jewelry. Structure: fixed headline '[problem] has 3 layers'; layer 1 = what people blame; layer 2 = the real cause; layer 3 = what nothing they tried fixes → LC's PVD bond. One PiP insert per layer (describe it). Calm specialist voice, 140 wpm, ≤15 words per sentence. The presenter is a 'jewelry materials specialist', never a medical doctor, never claims credentials. End with any 7 for $85. Give 3 headline variants and 5 avatar casting notes (age/ethnicity/setting).
```

### Variants to test

- Avatar age (30s vs 50s vs 60s) and gender
- White coat vs smart casual "specialist"
- 60 s vs 3 min
- Headline "3 layers" vs "3 mistakes" vs "the real reason"

## Reference examples

See [examples/README.md](examples/README.md) (1 posts). Top 5:

- @FedotOff90 (103L/205BM/8kV): 5 AI formats scaling: AI podcast (280 days live), AI UGC, AI doctor avatar, AI listicle, AI animation (claymation/CGI). — https://x.com/FedotOff90/status/2106401392374186396
