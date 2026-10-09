# 66 · Interactive gesture add-on ads (TikTok tap-to-reveal, shake-to-reveal, Super Like): see it, then make it

[![The example: storyboard of @_deepakss_'s post](example/storyboard.jpg)](https://x.com/_deepakss_/status/2087895969157246985)

**The example:** [@_deepakss_ on X](https://x.com/_deepakss_/status/2087895969157246985) · 0:15 video · 10 likes, 201 views

**Watch it:** [open the post on X](https://x.com/_deepakss_/status/2087895969157246985) · [play the video file](https://video.twimg.com/amplify_video/2087894468787675137/vid/avc1/320x568/OJey6kH1QrZRe7CY.mp4?tag=29)

> Building "Tiktok for games" Arcadeo for this year's Shipaton. My main aim is to have a non frustrating experience when viewing an ad. This means user can skip the ad in 5 seconds, it appears naturally when scrolling for games, and they aren't those stupid interactive ads but entertaining video ones. Biggest lesson: AdMob doesn't always have an ad for you and you need to manage all of this yourselfs. #buildinpublic

## What you are seeing

An interactive game ad: phone screens showing a puzzle you tap to play, then a story scene, so the viewer plays a few seconds inside the ad before the app is shown.

## Beat by beat

The storyboard above samples the video every 0:01. Lines are the transcript for that stretch; on-screen text comes from OCR, so treat it as rough.

| Frame | Time | On screen | Said / sung |
|---|---|---|---|
| 1 | 0:00–0:01 | 14:09 cw so wes as ae mes me a | · |
| 2 | 0:01–0:03 | · | · |
| 3 | 0:03–0:05 | a, oo SS io Bi a in mm Test mode: The Wisdom App a | · |
| 4 | 0:05–0:07 | Ee Sr Oy ra! a My Ob Rj Test mode: The Wisdom App | from ancient minds |
| 5 | 0:07–0:09 | · | to modern times |
| 6 | 0:09–0:11 | · | · |
| 7 | 0:11–0:13 | · | · |
| 8 | 0:13–0:15 | · | · |

<details><summary>Full transcript (timestamped)</summary>

- `0:05` from ancient minds
- `0:08` to modern times

</details>

## How to make one like it

**The format in one line:** TikTok interactive add-ons layered on an existing video ad: a Display Card that reveals an offer on tap, a shake-to-reveal surprise, or branded Super Like icons on double-tap.

**Why it works:** - Turns a gesture viewers already make into the ad interaction. - Good for offers/drops.

**Contents:** [1. Structure](#1-copy-the-structure) · [2. Shot by shot](#2-shot-by-shot-remake) · [3. Script and hooks](#3-write-the-script) · [4. Prompts](#4-prompts) · [5. Tools and settings](#5-tools-and-settings) · [6. Louise Carter remake](#6-louise-carter-remake) · [7. Variants and test](#7-variants-and-test-plan) · [8. Pitfalls](#8-pitfalls)

### 1. Copy the structure

Use the example's timing as your beat sheet. Keep the beat, change the words and the product.

| Beat | Time | In the example | Your version |
|---|---|---|---|
| 1 | 0:01 | on screen: 14:09 cw so wes as ae mes me a | … |
| 2 | 0:02 | (visual beat, see frame 2) | … |
| 3 | 0:04 | from ancient minds | … |
| 4 | 0:06 | from ancient minds to modern times | … |
| 5 | 0:08 | from ancient minds to modern times | … |
| 6 | 0:10 | to modern times | … |
| 7 | 0:12 | (visual beat, see frame 7) | … |
| 8 | 0:14 | (visual beat, see frame 8) | … |

### 2. Shot-by-shot remake

**Target length / size:** Existing video ad + interactive add-on

| # | Time / slot | What we see (visual + camera) | Dialogue / on-screen text |
|---|---|---|---|
| 1 | Base | A proven 15-30s video | - |
| 2 | Add-on | Display card / shake-to-reveal / gift code | Reveals an offer |
| 3 | Measure | Engagement on the add-on | - |

<details><summary>Playbook shot list (Louise Carter version from the README)</summary>

| Time / slot | Visual | Audio / copy |
|---|---|---|
| 0-5s | Gift box unboxing video | — |
| 5s | Display Card: "Tap to reveal today's stack" | — |
| Reveal | Card with any 7 for $85 | — |

</details>

### 3. Write the script

Open with one of these hooks (first 1–3 seconds, or the headline on a static):

- "Tap to open the box"
- "Shake to reveal your stack"

Then fill the beats from the table above. Pull the wording from real customer reviews, not from ad copy: a review line beats a copywriter line almost every time. Read every line out loud and cut anything you would not say to a friend. Ready-made Louise Carter scripts are in section 6; hand [BOT.md](BOT.md) to any AI agent to write versions for another brand.

### 4. Prompts

**TikTok Ads Manager**

```text
Ad > Interactive add-ons > Display Card (or Gift Code), set the reveal at 3-5s, card text max 30 characters.
```

**Full creative-agent prompt (from the playbook):**

```
Write 5 Display Card / gesture concepts for LC TikTok ads with on-card copy ≤8 words.
```

### 5. Tools and settings

1. Add Display Card to winning TikTok video ads; test vs no card.

| Setting | Value |
|---|---|
| What you are building | A repeatable system (account, page, offer or pipeline), not one ad |
| Cadence | Decide the posting or launch rhythm up front (e.g. daily, or 3 new ads a week) and keep it for 30 days |
| Template | Lock one caption, layout and naming template so output is consistent |
| Tracking | One UTM pattern per system (`utm_campaign=F<NN>`) and a weekly sheet: spend, CTR, hook rate, CPA |
| Tools | Meta Ads Manager / TikTok Ads Manager, a shared Drive folder per format, the agent brief in BOT.md |

### 6. Louise Carter remake

- A · Tap-to-reveal offer.
- B · Shake-to-reveal gift.
- C · Super Like gold sparkles.

Brand rules, claims you can and cannot make, and more scripts: [brands/louise-carter.md](brands/louise-carter.md). Step-by-step from idea to scale: [STAGES.md](STAGES.md).

### 7. Variants and test plan

- Card vs no card

**Test plan:** - **Budget/structure:** A/B on an existing winner, $30/day - **Primary KPIs:** CTR, CPC; Omni (F66-*) - **Kill rule:** No CTR lift - **Scale rule:** Holiday drops - **Naming:** `utm_content=F66-<concept>-<variant>`; weekly Omni roll-up of new-customer revenue by format.

**Naming:** `F66-<variant>-<hook##>-<date>` so results map back to this folder. Change one thing per test (hook, narrator, length or offer), never two.

### 8. Pitfalls

- Add-ons sit on top of a good video; they do not fix a weak one.
- No clean public example; visual is a mock.
- Changing the template every week: the system only learns if it stays consistent for at least 30 days.
- No tracking: without one naming and UTM pattern you cannot tell which piece of the system works.

**Compliance:** Baseline: [_COMPLIANCE.md](../_COMPLIANCE.md) (no fake testimonials, AI disclosure, no bulk/spoofed accounts, copy structure not assets, PDP-only claims). - Offer must be real.

## More examples

Every post we found for this format, with transcripts: [examples/](examples/README.md). Playbook: [README.md](README.md). Agent brief: [BOT.md](BOT.md).
