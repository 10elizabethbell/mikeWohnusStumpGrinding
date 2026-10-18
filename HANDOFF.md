# Stump Grinding (Mike Wohnus) — handoff at ~60%

**Live:** https://10elizabethbell.github.io/mikeWohnusStumpGrinding/ · **Repo:** https://github.com/10elizabethbell/mikeWohnusStumpGrinding · **Built:** 2026-10-18 from Muse brief 2026-10-18 (Ocean County Home Helpers flyer post)

## What's built
- One page, phone first: header (stump mark + "STUMP GRINDING" lettering, 732-581-5311 top right), hero, how it works, quote form, close, footer.
- World: their own yard sign standing in a lawn. Forest green and cream come from the sign; cream sections are "sign boards" with the sign's rule lines; green is lawn.
- Signature element: a real stump, seen from above (bark flares, off-centre growth rings, drying cracks). Drag across it with a finger (or move the mouse over it) and a yellow grinder boom with a spinning carbide-tooth wheel grinds it down to fresh grindings, throwing wood chips into the grass. Until someone touches it, the grinder sweeps side to side and walks across the stump like the real machine. When less than 15% is left, the lawn grows back over the spot ("Lawn back."), holds for a moment, then a fresh stump fades in. A half-ground stump settles back after 4.5s of quiet. Constants at the top of the "stump in the lawn" script (`GRIND`, `REGROW`, `AUTO_AFTER`, `LAWN_AT`...). Scrolling past the stump doesn't grind it; only a finger pressed on it does.
- Grass edges: where a sign board meets the lawn, grass blades sway in two winds and part under the finger or mouse. One shared animation loop; paused off screen; reduced motion gets a still frame. `STILL = true` at the top of the script turns all motion off (older-audience mode).
- Contact: "Text us a photo" opens a text to 732-581-5311 with "Hi! Here's a picture of my stump for a free quote." The form (name, where, how many stumps, notes) writes a text and opens the messages app; the visitor attaches the photo. It falls back to a copy button and a call link. The number in the header is a tap-to-call link.
- Footer echoes the sign's bottom band: the stump mark, "Thank you for your business!" (from the sign), and a huge tap-to-call 732-581-5311 between rule lines.
- Favicon / home-screen icon: the stump mark redrawn from the sign. og.jpg (1200x630) is the hero, for the Facebook link preview.

## Assumptions I made
- **No business name on the site.** The brief says not to invent one; the sign only says "STUMP GRINDING", so that's the wordmark. Mike's name isn't on the page either (brief: only once outreach confirms it).
- Voice "we/us": the post says "Send us a picture".
- The step copy ("Stand back far enough to get the whole stump...", "We look at your stump ourselves and give you a straight price") is mine, written in their plain tone. No facts in it, but Mike should read it.
- Meta description says "Stump grinding in New Jersey". Inferred from the 732 area code and the NJTC number; no towns listed anywhere.
- Texting: unknown whether the number takes texts. The whole page leans on texting a photo because that's literally his ask; the header number and the form's call fallback cover calling.
- Not treated as a 40+ audience (brief doesn't say so), though Ocean County skews older. If Ellie wants the still version, set `STILL = true`.
- The yard sign image in the post looks like a mockup, not a photo of a job, so it isn't on the page. It was used for colors, lettering and the mark.

## Placeholders and gaps
- Business name: REQUIRED before handing over.
- Service area / towns: unknown. No area section on the page.
- NJTC# 939790: on the sign but not verifiable online (the NJ Board of Tree Experts has no public lookup that search could reach). Left off the page. Add it as a trust line once verified (or Mike confirms).
- No email (footer has none), no hours, no reviews, no prices, no work photos, no before/afters.
- Facebook: only Mike's personal profile exists, linked in the footer only. No "see more of our work" link under photos because there are no photos. Swap in a business page if he makes one.
- No proof section at all yet: the biggest hole once photos exist.

## Questions for the owner
- What should the business be called on the site (and is "Mike" OK to show)?
- Can customers text this number? (The site assumes yes.)
- Which towns do you cover?
- Can we use NJTC# 939790 on the site? Insured?
- A few job photos, ideally before/after pairs of the same stump.
- Anything you also do: root removal, chip haul-away, backfill, tree work?
- Email for the footer?

## Ideas not built (yours to pick)
- **Runner-up world:** the yard sign itself as the hero: a full cream sign on wire stakes in a lawn, the headline printed on it, grass swaying at the stakes.
- Before/after sliders (plain solid divider) the moment photos arrive, in a "Recent stumps" section with the Facebook link under it.
- Grinder sound on desktop when hovering (off by default).
- Self-hosted condensed face matching the sign lettering (e.g. Oswald or Barlow Condensed) instead of the system stack's Arial Narrow / Helvetica.
- Desktop: the form's left column has empty space under "Free quote" (it's sticky). A good spot for job photos once they exist.
- The sign's thin inset green frame on the desktop cream boards (finish reviewer's idea).
- A "how big is it?" size chip (under 12", 12–24", bigger) in the form if Mike quotes by diameter.

## Not verified
- Real-device touch (tested with simulated touch in Chromium; WebKit layout only).
- The real SMS handoff on iOS and Android, including whether iOS keeps the `body` text when the user attaches a photo.
- Frame rate on older phones (chips capped at 380 on phones).
- Impeccable sweep: finish reviewer + all modes except live/onboard ran; fixes applied. The critique pass ran its two assessments in one agent (degraded). The detector ran in full mode; its one remaining flag (flat type hierarchy) is a false positive because it skips the clamp() headline sizes, and is ignored for index.html in `.impeccable/config.json`.
- Facebook's in-app browser specifically.
