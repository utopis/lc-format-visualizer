# BOT.md · generate a "Screenshot-native static pack (iPhone Notes, text thread, Reddit, email, Google, IG story/DM, Trustpilot)"

Plug-in brief for any agent (Claude, GPT, Grok, Codex) to produce this format for ANY brand. Self-contained: read this file, then skim `examples/` for real references.

<!-- QUICKSTART:START -->
## Quick start (bot-ready)

Machine-readable version of this brief: [`bot.json`](bot.json) (spec, shots, prompts, references, paid-ad examples, QA checklist).

**Do this in order:**

1. Open the real references below and write down the hook, the beat order and the length of each.
2. Fill the inputs (brand, reviews, assets, channel). Pick the 3 strongest angles from the reviews.
3. Write 3 concepts on the reference structure (target: 5-10 statics, 1080x1350/1080x1920), then produce them with the prompts below.
4. Run every concept through the QA checklist. Fix, then hand off.

### Real references (study before writing)

- **Main example**: [@liv_unltd](https://x.com/liv_unltd/status/1774923299136716885) · A real Gopuff ad shown in the Instagram feed, built to look like an iPhone Notes page: a 'Notes' header, a bold line "40% off alcohol?!?" and a few casual sentences about getting drinks delivered in minutes with a promo code. Under it sits the normal app-install card (logo, stars, Install). It reads like a note someone typed, not like an ad.
- Example: [@growthquesthq](https://x.com/growthquesthq/status/1922749862262489528) · 1⃣ Notes App Ad This one has cut client CPLs by 75%+
- Example: [@pearmill_agency](https://x.com/pearmill_agency/status/1674091921508007944) · 2/7 The Notes App Static 📒 - Open the Notes app on an iPhone - Create copy that reads like a note to self - think natural and human - Screenshot and p
- Example: [@daniel_eckler](https://x.com/daniel_eckler/status/1678803289243041793) · Literal iMessage Ad 👀
- Example: [@gregmfitz](https://x.com/gregmfitz/status/1621504769079517184) · Whatever agency or consultant is recommending this notes app ad creative style must be stopped

### Live paid ads in this format (3 in [adlibrary/](adlibrary/README.md), longest-running first)

- **Amy: Verified-buyer review card over car selfie (Amy, beef liver)** (382 days live): "GREAT ENERGY BOOSTER!" headline; a 5-star "Verified Buyer" review card floats over a man's car selfie holding the bottle; an arrow links the two.
- **British Supplements: Google-search UI static ('Which UK brand has no fillers?')** (331 days live): A Google search bar with an autocomplete question 'Which UK brand has no fillers?', a cursor clicking it, then a featured-snippet style answer box with ticks and product photos.
- **Japanese Taste: iPhone Notes checklist static (Japanese Taste)** (238 days live): An iPhone Notes screen: "Weekly Japanese Taste Checklist: Snacks for Friday night ✓, Matcha for Monday mornings ✓, J-Beauty for your nightly reset ✓" with product photos.

### Shot list (fill the [brackets])

| Slot | Visual + camera | Audio / on-screen text |
|---|---|---|
| iPhone Notes | Notes app screenshot | "things I stopped doing at 35: 1. taking my jewelry off to shower..." |
| iMessage thread | Two friends texting | "where is your necklace from?? you wore it in the pool" |
| Reddit post | Reddit-style post in a relevant community | A question + top answer mentioning the product |
| Google results | Search bar "jewelry you can shower in" | Top result is the product |
| Trustpilot / review card | Review layout | A real review verbatim |

### Prompts

**Build**

```
Recreate UIs in Figma with community UI kits (iOS 17 Notes/Messages, Reddit). Use generic names, no real usernames. Export at 1080 wide.
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
- [ ] Files named `F32-<concept>-<variant>`; tracking tag `utm_content=F32-<concept>-<variant>`.
- [ ] Avoid: Do not fabricate reviews or present a fake conversation as real; reviews must be real and attributed.
- [ ] Avoid: Do not use other platforms' logos in a way that implies endorsement.
- [ ] Avoid: No clean public example was found in this research pass; the visual is a mock.

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
5. Name every asset `F32-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F32
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

Statics that mimic native phone UI: an iPhone Notes list, an iMessage thread, a Reddit post, an email, a Google search results page, an IG story/DM, a Trustpilot review card, a tweet. The UI is the hook; the copy carries the angle; usually paired with long primary text.

### Why it works

- Cheapest reach in two accounts: screenshot/fake-text/Reddit $7-12 CPM vs $20 for educational talking heads (@PhilKiel).
- Reads as content from a person, not a brand — the brain files it as "someone I follow".
- Each UI = a different Entity ID for the same message; dozens per hour with AI image tools.
- Pairs with long primary text (S-tier "long primary text with organic image", @nicktheriot_).

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Notes | iPhone Notes titled "jewelry I never take off" with 5 bullets, last = "LC herringbone (14K PVD, showers fine)" | Primary text: personal story |
| iMessage | Thread: friend "wait is that the necklace you swam in??" / "yes 6 months, still gold" / "SEND LINK" | Primary text: "my sister made me post this" |
| Reddit | r/jewelry-style post (LC-authored, labeled): "Finally found gold jewelry I can shower in — 6 month update" | Primary text: update copy |
| Google | Search bar "jewelry you can shower in" → LC as result with stars | Headline: "Stop googling" |
| Trustpilot | 5-star card with a real review quote + name initial | Primary text: 3 more reviews |
| Email | Inbox screenshot "Your necklace is still gold? (6-month check-in)" | — |

### Hooks

- Notes: "things I stopped doing at 30" (#4: taking my necklace off)
- iMessage: "WAIT is that the necklace you wore in Cabo"
- Google: "why does my necklace turn green"
- Reddit-style: "6 months of showering in the same necklace — update"
- IG DM: "where is your necklace from?? I need it"
- Trustpilot: real review "I swim, shower, sleep in it"

### Production recipe

1. Make 7 UI templates in Figma (Notes, iMessage, Reddit-style, Google SERP, IG DM/story, Trustpilot card, email) at 1080×1350 and 1080×1920.
2. Fill from the angle bank: each angle × 3 UIs.
3. Use real customer quotes (with permission) for review/DM/text content; LC-authored posts must not impersonate a real Reddit user.
4. Long primary text (150-400 words) telling the story behind the screenshot.
5. Batch 20 per week; let Meta pick.

### Existing bot prompt

```
For each LC angle in {{ANGLES}}, write copy for 3 native UI statics chosen from: iPhone Notes list, iMessage thread (2 friends), Reddit-style post (clearly LC's own account), Google search page, IG DM, Trustpilot card (REAL review text from {{REVIEWS}} only), email subject+preview. Output UI type, exact on-image text (fits a phone screen), and 200-word primary text in first person. No invented testimonials; flag where a real quote is required.
```

### Variants to test

- UI type (7)
- Long vs short primary text
- Real review vs founder Notes
- Feed 4:5 vs story 9:16

## Reference examples

See [examples/README.md](examples/README.md) (9 posts). Top 5:

- @ads4apps (412L/930BM/27kV): 39 Meta formats that convert (930 bookmarks): X reasons, IG story, us vs them, Venn, don't buy this, iPhone notes, text message, low stock, we're sorry, breakin — https://x.com/ads4apps/status/2081785032679518490
- @FedotOff90 (110L/208BM/9kV): 37 formats printing (with days active): AI podcast 280d, report card, iPhone Notes, text on skin, Reddit, cross-out, fake PDP, tier list, myth vs fact, zero sta — https://x.com/FedotOff90/status/2104949773539442831
- @PhilKiel (35L/37BM/6kV): Format-level CPMs over 90 days: screenshot/fake-text/Reddit formats $7-12 vs educational talking heads $20; partnership creator $11-17 vs brand $18-31. — https://x.com/PhilKiel/status/2096549796408619413
- @DtcMamun (59L/14BM/3kV): Jewelry brand running AI statics + videos on TikTok/Meta: $14k sales on $7k ads (2.04 ROAS) day screenshot. — https://x.com/DtcMamun/status/2087270100617646477
- @raph_guilhem (9L/6BM/377V): 35 static/native formats tree: Trustpilot, text msg, email screenshot, Reddit, text on skin, crossed-out, tier list, Venn, breaking news. — https://x.com/raph_guilhem/status/2090725512976970065
