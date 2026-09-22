# The Pre-Publish Checklist™

**Deliverable 5 · SpyMark Protection System™**

The 8-minute gate between you and every file you publish. If a file doesn't pass all four gates, it doesn't go live.

---

## Gate 1 — DETECT (≈2 min)

- [ ] Ran `exiftool -a -G1 -s` on every file
- [ ] Read `Make` / `Model` / `Software` / `Author` fields
- [ ] Checked for GPS coordinates
- [ ] Checked for a C2PA / Content Credentials manifest
- [ ] Asked: "Did any part of this pass through a model?" — answered honestly
- [ ] If text: re-read aloud for uniform rhythm / generic phrasing

**Fail condition:** any identity-linking ID, GPS, or provenance signature you can't explain. → Fix with Gate 2.

---

## Gate 2 — STRIP (≈3 min)

- [ ] `exiftool -all=` run on images, PDFs
- [ ] ID3 tags stripped from audio
- [ ] QuickTime/metadata atoms cleared from video
- [ ] Re-exported / re-rendered through **your own** tool
- [ ] If AI-assisted text: **every paragraph rewritten** in your own voice
- [ ] Added at least one piece of lived detail (name, number, place, opinion)
- [ ] Broke sentence rhythm deliberately (vary length hard)

**Fail condition:** any raw, unedited model output remains. → Rewrite it. There is no shortcut here.

---

## Gate 3 — SEAL (≈2 min)

- [ ] Origin Record entry written (title, date, tools, human work)
- [ ] HumanBadge applied (image corner / doc footer / end card / audio intro)
- [ ] Disclosure block (A–E) pasted next to the work
- [ ] File hash recorded (optional but powerful)

**Fail condition:** stripped a mark and added nothing back. → The gap is the danger. Seal it.

---

## Gate 4 — BROADCAST (≈1 min)

- [ ] Bio / About page carries the origin-logged sentence
- [ ] Footer / signature includes the verify link
- [ ] If it's a client deliverable: certification line item included in the quote

**Fail condition:** nobody can find your claim. → A seal nobody sees protects nobody.

---

## The one-screen version (pin this)

```
□ DETECT   exiftool read · provenance check · "was AI in the chain?"
□ STRIP    metadata emptied · re-rendered · text fully rewritten
□ SEAL     origin log · badge · disclosure block
□ BROADCAST bio · footer · quote line item
```

Four gates. Eight minutes. **No file ships until it's four-for-four.**

---

## File-type quick paths

### Before you post an IMAGE
1. `exiftool -all= photo.jpg`
2. Open in editor → tiny crop or color tweak → export q92+
3. Add badge bottom-right (2–3% of edge, 60% opacity)
4. Log it, paste disclosure A/B/C

### Before you publish TEXT
1. Rewrite every generated sentence by hand
2. Add one lived detail per section
3. Paste disclosure block under the title
4. Add origin record line + hash

### Before you upload AUDIO
1. Strip ID3 → re-encode twice (256 → 320 kbps)
2. Add room tone or your own intro for 2 seconds
3. Badge in the show notes + spoken intro
4. Log + disclose

### Before you ship VIDEO
1. Strip QuickTime atoms → re-encode through your NLE
2. Corner bug + end card (badge)
3. Description includes disclosure + verify link
4. Log + disclose

---

## Red flags — stop and rebuild

If **any** of these are true, do not publish:

- ❌ Someone else's provenance manifest is attached to your file
- ❌ GPS coordinates you didn't intend to share
- ❌ A paragraph you cannot confidently say you wrote
- ❌ An origin record you can't fill in honestly
- ❌ A disclosure claim you'd be embarrassed to defend in public

A rebuild costs you an hour. A reputation costs you everything.

---

**Pass the gate. Then publish like you mean it.**
