# SpyMark Defense™ — 5-Minute VSL Script + Storyboard

**Target:** the uptrending "Spymarks, Not Watermarks" conversation + Claude/Anthropic invisible-watermark wave (HN front page 442 pts; Gizmodo, WIRED, TechCrunch, IEEE Spectrum coverage Sept 2026)
**Runtime:** ~5:00
**Format:** Talking head with uppercase text slides (bold captions, teal-on-dark)
**VOICE:** ElevenLabs voiceId `PeMXWXe7DDCb8HldBr2s`

---

## COLD OPEN — 0:00–0:30

**[SLIDE 1]** `YOUR FILES ARE TELLING PEOPLE WHO YOU ARE`

*VO:*
In August 2026, Anthropic switched on invisible watermarks in Claude's text. Google's SynthID started hiding a hundred-and-thirty-six-bit payload inside a single image. Microsoft's Paint and Photos watermarks were traced back to user IDs by researchers.

None of it is visible. All of it travels with your work.

**[SLIDE 2]** `THAT IS NOT A WATERMARK. IT'S A SPYMARK.`

---

## THE PROBLEM — 0:30–1:15

**[SLIDE 3]** `A WATERMARK PROVES AUTHENTICITY` / `A SPYMARK TRACKS YOU`

*VO:*
There's a difference and it's the whole ballgame. A watermark is a visible mark of authenticity or ownership. A spymark is a hidden signal that makes your work traceable — without your knowledge or consent.

**[SLIDE 4]** `AND BUYERS CAN NO LONGER TELL HUMAN FROM MACHINE`

*VO:*
Here's what that costs you. When buyers can't tell human work from machine work, they don't pay a premium. They discount *everyone*. Your honesty doesn't matter. Your skill doesn't matter. Because you can't *prove* a human made the work, you get priced like a machine.

That's not a talent problem. It's a **proof** problem.

---

## THE MECHANISM — 1:15–2:45

**[SLIDE 5]** `THE SPYMARK MODEL™` / `DETECT · STRIP · SEAL · BROADCAST`

*VO:*
The SpyMark Defense System runs on four moves. Learn them once and you never publish exposed again.

**[SLIDE 6]** `MOVE 01 — DETECT`

*VO:*
Detect. Find every mark in the file — the metadata container, the provenance signatures, the statistical fingerprints. You can't fix what you can't see.

**[SLIDE 7]** `MOVE 02 — STRIP`

*VO:*
Strip. Remove the tracking identifiers that don't belong to you. Cleanly. Ethically. And here's the line nobody else gets right — stripping does not mean hiding that you used a tool. Disclosing your tools is a separate act, and the system tells you to do it. Strip tracking. Disclose tools. Opposite things.

**[SLIDE 8]** `MOVE 03 — SEAL`

*VO:*
Seal. This is the move almost everyone misses. Once you've removed someone else's mark, you have a gap — and a gap reads as *suspect*. So you fill it. A dated origin record. Your badge. Your disclosure. Proof that a person made the decisions.

**[SLIDE 9]** `MOVE 04 — BROADCAST`

*VO:*
Broadcast. A seal nobody sees protects nobody. You put it on the work, in your bio, and in your pricing. And that's where it stops being a chore and starts being revenue.

**[SLIDE 10]** `DETECT. STRIP. SEAL. BROADCAST.` / `UNDER 60 SECONDS PER FILE`

---

## THE OFFER — 2:45–4:00

**[SLIDE 11]** `THE 8-PART SPYMARK DEFENSE™ SYSTEM`

*VO:*
I've packaged the entire thing into eight working deliverables.

The core guide with the four-move model and the 7-day defense sprint. The Tracking Audit Sheet and the Origin Log — your fill-in proof of authorship. The Strip and Seal Toolkit with paste-in disclosure blocks and the exact cleanup commands. The Trust Premium Pricing Sheet with the script to defend a twenty-five-percent premium without ever discounting.

Then the Pre-Publish Checklist — the eight-minute gate. The SpyMark Tracker — your weekly risk score and 30-day trust score. The Provenance Scripts — word-for-word answers to the twelve hardest questions, including the one you're thinking right now: *isn't this just hiding AI use?* And the Playbook — the 30-day roadmap.

**[SLIDE 12]** `VALUE: $196` / `TODAY: $19`

*VO:*
Individually that's a hundred-and-ninety-six dollars of value. Today it's nineteen.

Because here's the math that matters: a freelancer who raises one four-thousand-dollar project by fifteen percent banks six hundred dollars — from one sentence. "This comes with an origin record."

---

## CLOSE — 4:00–5:00

**[SLIDE 13]** `60-DAY GUARANTEE` / `KEEP EVERYTHING EITHER WAY`

*VO:*
You're covered by a sixty-day guarantee. Run the system. If your work isn't provably yours and you don't feel the difference, email me and I'll refund every cent — and you keep everything.

**[SLIDE 14]** `THE MARKS ARE BEING WRITTEN NOW` / `GET THE SYSTEM — $19`

*VO:*
The marks are being written into your files right now, whether you act or not. Later just means more unprotected work.

Prove your work is human-made. Then charge for it.

Click below. Get the SpyMark Defense System for nineteen dollars.

Detect. Strip. Seal. Broadcast.

**[END CARD]** `SPYMARK DEFENSE™` / `https://spymark.vercel.app`

---

## STORYBOARD NOTES

| Slide | Visual | Duration |
|-------|--------|----------|
| 1–2 | Dark gradient bg, teal text, slow zoom | 30s |
| 3–4 | Split-screen: "watermark" vs "spymark" | 45s |
| 5 | Four-move loop animation | 15s |
| 6–9 | One slide per move, icon top-left, teal accent | 90s |
| 10 | Loop closes into a circle | 15s |
| 11 | 8 PDF cards fanning out | 45s |
| 12 | Price reveal, gold accent | 30s |
| 13–14 | Guarantee seal, then CTA button pulse | 60s |

**Production:** Slides in uppercase, Inter/Archivo Bold, 60fps. VO via ElevenLabs (`PeMXWXe7DDCb8HldBr2s`). Background: subtle dark gradient with a faint scanning-line motif.

---

## GENERATION COMMAND (if ElevenLabs key available)

```bash
# Requires ELEVENLABS_API_KEY — not present at build time; script ships as fallback
curl -X POST "https://api.elevenlabs.io/v1/text-to-speech/PeMXWXe7DDCb8HldBr2s" \
  -H "xi-api-key: $ELEVENLABS_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"text":"<VSL_SCRIPT>","model_id":"eleven_multilingual_v2","voice_settings":{"stability":0.45,"similarity_boost":0.8}}' \
  --output vsl.mp3
```

**Status:** `ELEVENLABS_API_KEY` not present in credentials.env at build time → **full script + storyboard shipped as the deliverable** (per job instructions).
