# BOT.md · generate a "'Ugly ad': an unusual or weird visual + long copy (native image)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 1 odd image (1080x1350) + 250-500 word primary text), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@alexgoughcooper](https://x.com/alexgoughcooper/status/2092657905002529270) · A man in a lab-like room holding a big water bottle with a goofy caption ("Revealing my greatest invention"), swinging it around, a cheap and odd look that stops the scroll, 32M views.
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2049572960143347768) · Ugly ads scale brands to $100k a day. They are great at getting customers' attention. Yes, they don't win design awards, but who gives a fuck. Bank ac
- Example: [@TaherZariwala](https://x.com/TaherZariwala/status/1973431067702075421) · Ugly ads are crushing right now But the ad isn’t the goal, it’s the funnel 👉 Ugly Ad (pattern interrupt) → Primary Copy (hook) → Advertorial (warm-up)
- Example: [@TaherZariwala](https://x.com/TaherZariwala/status/1978326652183589040) · Ugly statics we did recently
- Example: [@TatsukiThomas](https://x.com/TatsukiThomas/status/2037548415429816608) · When you launch a new ad format and it immediately starts RIPPING. This ones a super a ugly static of mostly copy. Let's see if it can scale...
- Example: [@TatsukiThomas](https://x.com/TatsukiThomas/status/2049168032485064768) · Swipe this ad library for ugly static inspo. Great for clean pattern-interrupting formats and clever before/afters.
- Example: [@zackcreates](https://x.com/zackcreates/status/2023515671502659784) · Don't sleep on ugly ads!! Got feedback over the weekend that this video is doing NUMBERS for my SaaS client. Currently a top performer getting the mos
- Example: [@iKaustubhChavan](https://x.com/iKaustubhChavan/status/2102363416803561551) · Dr. Squatch's static ads strategy FU*K design FU*K brand Make them ugly Give a killer offer Make tonnes of them DM if you want ugly statics that conve
- Example: [@FedotOff90](https://x.com/FedotOff90/status/2046591654354735155) · UGLY ads print. For health/ wellness/ beauty/ supplement niches. They are so WEIRD that people can't stop themselves from checking them out. Want a sw

### Live paid ads in this format (7 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Alicia Darling: Gym-clock POV with sticky caption ("Black leggings so I hope no one notices")** (319 days live): A POV of sneakers on a gym floor, a flip-clock "10:45" overlay, a white caption bubble: "Black leggings so I hope no one notices 😅". 4 variants ("At least no one else will smell me now"). Alicia Darling has 710 ads.
- **Skincare Tips: Mundane car-door POV (Skincare Tips)** (290 days live): A POV of legs in denim shorts getting into a car, holding keys. Nothing explained; the copy does the selling.
- **Raising Toddlers with Bec: Vintage anatomy diagram static ("2 years in diapers vs 4 years")** (278 days live): A vintage medical-illustration-style diagram comparing two toddlers' brain-bladder connection ("active connection" versus "signal suppression"). Raising Toddlers with Bec.
- **WebMD: Editorial flat-lay food static (WebMD 'Polyphenols')** (253 days live): Overhead flat-lay of polyphenol foods (berries, olives, nuts, dark chocolate, cinnamon) with a handwritten 'POLYPHENOLS' label in a star bowl.
- **Pet PA: Horse-nose-in-lens static (Pet PA)** (176 days live): A horse's nose fills the camera, with a "Save an extra 5% with auto delivery" bar and products below.
- **Resilia · Vascular Wellness Report: A skeleton among wine barrels holding the garlic pouch** (1 days live): A skeleton among wine barrels holding the garlic pouch, with a "3 for $20" badge.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| Image | A deliberately strange but relevant photo: the necklace in a fish tank, on a lemon, coiled in a cereal bowl. Phone-shot, slightly off-centre, no text on image | - |
| Copy line 1 | - | Explains the weirdness: "Yes, that's our necklace in my son's fish tank. It's been in there 3 weeks." |
| Copy body | - | The story: why it's there (a dare / a test), what happened, what it proves (waterproof) |
| Copy close | - | Offer + a P.S. that callbacks the image: "P.S. The fish are fine." |

### Prompts

**Idea bank (Claude)**

```
List 20 weird-but-true places to photograph [product] that each prove one benefit (water, sweat, durability, giftability). For each, a first line that explains the photo in under 15 words.
```

**Shoot**

```
iPhone, daylight, no styling; the image should look like a friend sent it.
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
- [ ] Files named `F84-<concept>-<variant>`; tracking tag `utm_content=F84-<concept>-<variant>`.
- [ ] Avoid: Weird, not misleading: the photo must show something that really happened.
- [ ] Avoid: If the image needs explaining, line 1 of the copy must explain it.
- [ ] Avoid: Don't test more than one weird image per ad set; you won't know which one worked.

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
5. Name every asset `F84-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F84
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

A deliberately odd, low-polish photo (product in a weird place, strange crop, unexpected object) paired with long, story-driven primary text. Steal the visual idea and keep your own copy.

### Why it works

- Weirdness beats beauty for stopping the scroll.
- A low-polish look reads as organic.
- Long copy does the selling once the visual earns the pause.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Static | Necklace frozen inside an ice cube / in a glass of seawater / on a lemon | Primary: 300-word first-person story |

### Hooks

- "I left my necklace in a glass of seawater for 30 days"
- "Why is there a necklace in my ice tray?"

### Production recipe

1. Brainstorm 10 weird but true scenes (real tests: ice, saltwater, lemon juice).
2. Shoot on phone, flash on.
3. Pair with F09 long-copy natives.

### Existing bot prompt

```
List 10 weird-but-true visual scenes for LC that also prove durability, then write a 250-word native primary text for the top 3.
```

### Variants to test

- Weird level
- Proof vs pure oddity

## Reference examples

See [examples/README.md](examples/README.md) (8 posts). Top 5:

- @FedotOff90 (68L/98BM/6kV): 777 native images + long-form copy swipe board. — https://x.com/FedotOff90/status/2104253649346068682
- @FedotOff90 (41L/53BM/5kV): "The ugly ads print" — weird visuals stop the scroll, long copy sells; 122-ad Native Unusual Visuals board. — https://x.com/FedotOff90/status/2107184145541853536
- @alexgoughcooper (61L/60BM/9kV): This video did 32M views and is a masterclass in ugly ads. Why? Because it’s authentic. You keep trying to make ‘UGC’ or ‘ugly ads’ that are fully scripted. But — https://x.com/alexgoughcooper/status/2092657905002529270
- @Simon__Rob (51L/79BM/5kV): this is how your Meta ad account should be built if you're a brand: - ugly static ads and yapping videos stop cold traffic - testimonials and stats convince war — https://x.com/Simon__Rob/status/2089448804676239424
- @dileshumale (10L/3BM/775V): Animate those ugly static ads. Thank me later. — https://x.com/dileshumale/status/2105897021328757090
