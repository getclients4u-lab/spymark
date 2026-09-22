# SpyMark Protection System™

### The Creator's Defense Against Invisible AI Tracking Marks

**By the SpyMark Defense Team · Edition 1.0 · 2026**

---

## Why you're reading this

In August 2026, Anthropic turned on **invisible watermarks** in Claude's text output. Google's SynthID already encoded **136-bit payloads** into a 512×512 image — enough room for a 64-bit database ID with error correction left over. Microsoft shipped watermarks in Paint and Photos that researchers linked back to **user IDs**. Then came the article that gave the problem its name: *Spymarks, not Watermarks* — which pointed out the uncomfortable truth:

> A **watermark** is a visible mark that verifies authenticity or asserts ownership.
> A **spymark** is a hidden signal that makes your work traceable **without your knowledge or consent**.

That distinction is the whole ballgame. Watermarks are benign. Spymarks track *you*.

If you publish anything online — text, images, audio, video — you are now the product of a quiet negotiation you were never invited to. This system is how you take the negotiation back.

---

## The SpyMark Model™ — four moves

Everything in this system hangs on one acronym. Learn it once; use it forever.

> **D — DETECT** → find out *what* is being written into your files
> **S — STRIP** → remove marks that don't belong to you
> **S — SEAL** → add *your own* verifiable mark instead
> **B — BROADCAST** → publish with a disclosure you control

That's the **DSSB Loop™**: Detect, Strip, Seal, Broadcast.

Most creators skip straight to Strip. That's why they get caught out — they remove a mark, but they never replace it with proof of *their own* authorship, and they never tell anyone what they did. The DSSB Loop closes all four gaps.

---

## Move 1 — DETECT

You cannot remove what you cannot see. Detection has three layers, and you should run all three on any file you're about to publish.

### Layer A — Metadata sweep
Every file carries a container. Before you ever worry about invisible signals, empty the container.

- **Images:** open the file's properties, or run `exiftool filename.jpg`. Look for `Make`, `Model`, `Software`, `UserComment`, `XMP`, `GPS`.
- **PDFs:** `exiftool` again — check `Creator`, `Producer`, `Author`.
- **Audio (MP3/M4A):** check ID3 tags with any tag editor.
- **Video (MP4/MOV):** check for `com.apple.quicktime` atoms and device strings.

Metadata is the *loudest* signal and the easiest to fix. Clear it first so your second read is clean.

### Layer B — Provenance sweep
Check whether the file was produced by a system that signs its output.

- **C2PA / Content Credentials:** upload to a C2PA verifier, or inspect the file for a `c2pa` manifest box. If your camera, editor, or AI tool is C2PA-enabled, it has *signed* the file and attached a provenance record.
- **SynthID (Google):** present on output from Gemini, Imagen, Veo, and increasingly Google-adjacent tools. There is no public detector — which is exactly the point.
- **Anthropic Claude text marks:** introduced August 2026 by steering word choices into a detectable statistical pattern. Invisible to readers.

Layer B tells you whether the origin of the file is already documented somewhere you don't control.

### Layer C — Statistical sweep
For AI-generated text, the mark is often a *statistical signature* — a skew in word choices, not a hidden character.

- Ask: did any part of this text pass through a generation model? If yes, assume it carries a statistical signature.
- Re-read the piece out loud. If it sounds like *you* — your cadence, your slang, your digressions — you're already diluting the pattern.
- Human editing is statistically noisy. Noise is your friend.

**The 90-second rule:** if a file takes more than 90 seconds to fully clear, it's not ready to publish. Use the Tracking Audit Sheet (deliverable 2) to log what you find.

---

## Move 2 — STRIP

Stripping is about removing marks that **do not belong to you** — not about hiding that you used a tool. This matters, ethically and legally. Read the "What stripping is not" section below.

### Text
There is no reliable way to *guarantee* removal of a statistical watermark, and anyone selling you a "100% watermark remover" is lying. What you *can* do is make your text honestly yours:

1. **Rewrite in your own voice.** Read the sentence, close the tab, write what you actually meant. Do this for every paragraph you plan to publish.
2. **Add specific, lived detail.** Names, numbers, places, opinions. Models can't invent your Tuesday.
3. **Break the rhythm.** Vary sentence length hard. The statistical pattern depends on consistency; you're going to destroy the consistency on purpose.
4. **Never publish raw model output.** Ever. Not once.

### Images
1. **Strip the container:** `exiftool -all= image.jpg` (this rewrites the file clean and drops XMP/IPTC).
2. **Re-render through your editor:** open → adjust one pixel → export at quality 92+. Re-encoding destroys many fragile marks.
3. **Recompose, don't just filter.** Crop 2–3%, add your own layer, your own color grade. A *new* photograph of a photograph leaves *your* fingerprint.
4. **Re-shoot where possible.** A photo taken on your phone is yours end to end; a render never is.

### Audio
1. Strip ID3 tags.
2. Re-export at a different bitrate (e.g. 320 → 256 → 320 kbps). Many waveform marks do not survive double re-encoding; robust ones do — accept that you can't win every battle and lean on *Seal* instead.
3. Layer your own room tone or instrument for one bar. Your additions are yours.

### Video
1. Strip QuickTime metadata atoms.
2. Re-encode through your NLE with your own export preset.
3. Overlay your own bug/logo/credits card.

> **What stripping is NOT:** Stripping does not mean denying you used a tool. It does not mean deceiving a client, an employer, a regulator, or a platform that requires disclosure. It means removing *non-consensual tracking identifiers* from **your** creative output. Disclose tool usage when asked. Strip covert identity tracking always. Those are different acts; never confuse them.

---

## Move 3 — SEAL

Here is the move almost everyone misses. Once you've stripped someone else's mark, you have a **gap** — and a gap is dangerous, because "no provenance" reads as "suspect." So you fill it with a mark of *your own*.

Your seal has three parts:

1. **A signed record** — a dated note in your origin log (deliverable 2) recording what you made, when, with what tools, at what version.
2. **A visible badge** — a small, consistent mark on your work (the ◍-style human mark or your own monogram) that says *this came from a person you can name*.
3. **A public claim** — a short disclosure block you paste anywhere you publish (templates in deliverable 3).

Sealing turns "please trust me" into "here is my evidence." That shift is the entire difference between competing on price and competing on trust.

**Seal in 3 minutes:** date log entry → add your badge → paste your disclosure block. Done. Move on.

---

## Move 4 — BROADCAST

A seal nobody sees protects nobody. Broadcasting is the discipline of *saying out loud* what you did.

Three channels, always:

- **On the work itself** — badge + disclosure block.
- **In your bio / About page** — one sentence: *"Everything I publish is human-made and origin-logged. Verify at [link]."*
- **In your pricing conversation** — "My work comes with an origin record" is a *premium justification*, not a caveat. (See deliverable 4 for the exact script.)

Broadcasting is also a marketing engine. In a feed full of unmarked, unverifiable output, the creator who *shows their work* is the one who gets remembered.

---

## The 7-Day Spymark Defense Sprint

You do not need a month. You need one week of focused reps.

| Day | Focus | Outcome |
|-----|-------|---------|
| **Day 1** | DETECT — audit your last 10 published files | A filled Tracking Audit Sheet (deliverable 2) |
| **Day 2** | STRIP — clean metadata on every one of them | 10 files with empty containers |
| **Day 3** | STRIP — rewrite/re-render the 3 that were AI-assisted | 3 pieces that read/sound/look like you |
| **Day 4** | SEAL — build your origin log + badge + disclosure block | A named, dated record you can show anyone |
| **Day 5** | SEAL — apply the seal to your 3 best pieces | 3 pieces carrying YOUR proof |
| **Day 6** | BROADCAST — update bio, About page, and publish the disclosure | A public, verifiable claim |
| **Day 7** | BROADCAST — use the pricing script on one real quote | A premium, justified in one sentence |

By day 7 your work carries a **defensible story**. That story is what buyers pay for.

---

## The economics: why this is worth real money

Three forces are converging, and all three push money toward creators who can prove origin.

1. **The trust premium.** When buyers can't tell human from machine, they *discount everyone*. The only way to escape the discount is to prove origin. Provenance is the one feature a competitor's output can't copy.
2. **The regulatory tailwind.** EU AI Act transparency rules are forcing disclosure. Businesses that must disclose are also being asked by *their* clients to prove human input. You are selling into a compliance-shaped demand curve.
3. **The scam backlash.** Watermark-removal apps turned out to be full of lies and malware. The market is desperate for *credible*, *ethical*, *non-sneaky* provenance help. That's your lane — and you get to own the honest half of it.

Do the math on one client: a freelancer who raises rates by even **15%** on a single $4,000 project banks $600 from one well-timed sentence — *"this comes with an origin record."* That's the entire system paying for itself hundreds of times over.

---

## Ten rules to keep

1. Metadata first, always.
2. Never publish raw model output.
3. Human editing is a defense, not a chore.
4. Replace what you remove — the gap is the danger.
5. Date everything. Memory is not evidence.
6. Disclose tools; strip tracking. Different acts.
7. Your badge must be consistent, or it means nothing.
8. Say your claim out loud — on the work, in the bio, in the quote.
9. Charge for trust; don't apologize for it.
10. Re-audit monthly. The marks evolve. So do you.

---

## What's in the rest of this system

| File | What it gives you |
|------|-------------------|
| `02-tracking-audit-sheet.md` | The fill-in audit + origin log |
| `03-strip-seal-toolkit.md` | Word-for-word disclosure templates + badge spec |
| `04-trust-premium-pricing.md` | Tiers, three levers, the premium script |
| `05-publish-checklist.md` | The 8-minute pre-publish gate |
| `06-spymark-tracker.md` | Weekly risk scorecard + 30-day trust score |
| `07-provenance-scripts.md` | Answers to the 12 hardest questions |
| `08-spymark-playbook.md` | The 30-day client roadmap + starter block |

You now have the model. Everything after this is the toolkit that makes it real.

**Detect. Strip. Seal. Broadcast.** Then publish like you mean it.

— The SpyMark Defense Team
