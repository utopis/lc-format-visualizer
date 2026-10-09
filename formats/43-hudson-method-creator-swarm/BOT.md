# BOT.md · generate a "Hudson Method creator swarm (hundreds of small creators → every ad channel)"

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
5. Name every asset `F43-<concept>-<variant>` so results can be read per format.
6. Write the output to `brands/<brand-slug>.md` in this folder and set `STAGES.md` stage 3 to `drafted`.

## Output schema (per concept)

```yaml
format: F43
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

Instead of a few polished influencers, recruit hundreds of small creators (1k-50k followers) who each post many videos/month for a base fee + commission + volume bonuses; contests drive output; every creator video is whitelisted and loaded into Meta Partnership ads, Snap and YouTube — the creator swarm becomes the ad-creative engine.

### Why it works

- Volume of real creators = volume of Entity IDs and hooks; winners emerge statistically.
- Partnership/creator ads stay live longer (50.5 of 90 days) and get cheaper CPMs than brand assets.
- Commission on ad-driven sales keeps creators motivated to keep producing.
- Cal AI (15M downloads, $50M run rate) ran a creator roster + affiliate + daily creative team.

### Shot-by-shot (written for Louise Carter; swap in your brand)

| Time / slot | Visual | Audio / copy |
|---|---|---|
| Recruit | TikTok Shop affiliate center + IG search; samples to 50-200 creators/month | DM template (brand-run, opt-in) |
| Brief | 1-page brief: minimum every video must hit, 5 hook ideas, do/don't | Day-one rules |
| Produce | Creator posts 10-30 videos/mo on own account | Base pay per video + commission |
| Contest | Monthly video-count contest: $100-250 for 10 approved videos | VA review, net-30 |
| Amplify | Whitelist top 5% → Meta Partnership ads + Spark Ads | Omni attribution |
| Iterate | Winning hooks fed back to all creators | Weekly hook memo |

### Hooks

- Creator brief hooks: "I wore this necklace in the ocean for 30 days"
- "Unboxing the stack my husband got me"
- "Things I never take off"
- "Gift idea under $100 she'll actually wear"

### Production recipe

1. Phase 1 (month 1): 50 creators seeded via TikTok Shop affiliate + IG; 10% commission + $10-20/video base for first 10 videos.
2. Brief with minimum standards (product visible in 2s, says "14K PVD/waterproof" exactly as PDP, #ad/Paid partnership on).
3. VA reviews every video in a sheet (approved/not) → pay net-30.
4. Monthly video-count contest; top 10 creators get retainer ($300-500/mo for 20+ videos).
5. Weekly: pull top 5% by views/CTR → whitelist → Meta Partnership ads (utm_content=F43-<creator>-<hook>).
6. Feed winning hooks back to the swarm.

### Existing bot prompt

```
You manage LC's creator swarm. Given this week's creator video sheet {{SHEET}} (views, likes, link clicks, approvals), 1) list top 5% for Partnership ads with suggested ad copy, 2) extract the 5 best hooks verbatim, 3) write the weekly hook memo to creators (≤200 words), 4) flag any non-compliant videos (missing disclosure, off-PDP claims).
```

### Variants to test

- Pay model: per-video vs retainer vs commission-only
- Contest type: count vs GMV
- Organic only vs whitelisted

## Reference examples

See [examples/README.md](examples/README.md) (18 posts). Top 5:

- @Seanfrank (2027L/3902BM/376kV): The "Hudson Method" (Comfrt): seed hundreds of small TikTok creators, pay per video + commission, bonuses for 100+ videos/mo, load all into every ad channel. (M — https://x.com/Seanfrank/status/2051036381359849697
- @jakecastilloooo (984L/3090BM/290kV): Ex-Cal AI UGC lead's full AI UGC workflow (article): customer context → outlier videos vs creator baseline → reverse-engineer → believable first frame → test ta — https://x.com/jakecastilloooo/status/2107873317369581751
- @SeoulJosephK (720L/2243BM/98kV): App marketing reading list: paid (athcanft), organic UGC (Superwall pod), Sideshift/Posted/Noise view-based campaigns, Jake Castillo for influencers. — https://x.com/SeoulJosephK/status/2072291737536803119
- @pixclipper (134L/339BM/26kV): Mise $300K/mo: 18 UGC accounts running the SAME 43s wordless video (ALDI/LIDL/German versions); store name does the targeting; 702 videos in 8 weeks, 3 carry 60 — https://x.com/pixclipper/status/2084739019187847201
- @jesseabed_ (148L/324BM/18kV): Sideshift creator pay: hook-and-demo creators ~$400 base + view milestones for 40-60 videos; talking head/skit ~$400 for 20-30; 25% upfront. — https://x.com/jesseabed_/status/2102818749384421524
