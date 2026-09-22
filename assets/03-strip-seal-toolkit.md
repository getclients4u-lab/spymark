# The Strip & Seal Toolkit™

**Deliverable 3 · SpyMark Protection System™**

Everything you paste, copy, and apply. No theory — just the exact words, snippets, and specs.

---

## Part 1 — Paste-in disclosure blocks

Paste one of these wherever you publish. Pick the version that matches your situation and **never overclaim.**

### Version A — Fully human (no AI in the chain)

> **Human-made.** Written, shot, and edited by a person. No generative AI was used in this work. Origin record available on request. — [Your name], [date]

### Version B — AI-assisted, human-directed (most common, most credible)

> **Human-directed. AI-assisted.** I used AI tools for [research / drafting / ideation]. Every published word, frame, and decision is mine. Origin record available on request. — [Your name], [date]

### Version C — AI-generated, human-curated

> **AI-generated, human-curated.** This piece was produced with generative tools and directed, fact-checked, and edited by me. Tools: [list]. Origin record available on request. — [Your name], [date]

### Version D — Short form (bio, footer, social profile)

> Human-made & origin-logged. Verify → [link]

### Version E — Client deliverable footer (for freelancers)

> **Provenance:** This deliverable was created by [Your name / Studio] and carries an origin record covering authorship, tools, and human input. C2PA-signed where applicable. Verify with [email / link].

**Rule of thumb:** if a claim would embarrass you in front of a client who reads the actual process, soften it. Credibility compounds; overclaiming collapses.

---

## Part 2 — The HumanBadge spec

Your badge is your **seal**. It must be small, consistent, and carried everywhere — like a signature.

### Design spec

- **Format:** monogram + one symbol, no more. Example: `AR◍` or `◍ Studio Rosa`.
- **Colors:** two colors max. High contrast. Must read at 16px.
- **Placement:**
  - **Images:** bottom-right, 2–3% of the shorter edge, 60% opacity.
  - **Documents:** footer of every page, 8pt, muted.
  - **Audio:** first 2 seconds, spoken or a subtle chime.
  - **Video:** persistent corner bug or an end card.
  - **Text:** inline at the end, part of the disclosure block.
- **Consistency:** one badge, one version number. Bump the version when your process changes (e.g. `AR◍ v2`).

### SVG starter (edit the initials)

```svg
<svg xmlns="http://www.w3.org/2000/svg" width="120" height="40" viewBox="0 0 120 40">
  <rect width="120" height="40" rx="6" fill="#0d0d0d"/>
  <text x="12" y="26" font-family="Inter, Arial, sans-serif" font-size="15"
        font-weight="700" fill="#ffffff">AR</text>
  <circle cx="48" cy="20" r="9" fill="none" stroke="#3ddc97" stroke-width="2.5"/>
  <circle cx="48" cy="20" r="3" fill="#3ddc97"/>
  <text x="64" y="25" font-family="Inter, Arial, sans-serif" font-size="10"
        fill="#9aa0a6">HUMAN-MADE</text>
</svg>
```

### Where the badge lives

- [ ] Image exports (bottom-right)
- [ ] PDF/doc footers
- [ ] Video end card + corner bug
- [ ] Audio intro
- [ ] Email signature
- [ ] Social bio
- [ ] Website footer
- [ ] Invoice / quote footer

If it isn't in all eight, it isn't a seal — it's a decoration.

---

## Part 3 — Cleaning commands by file type

### Images
```bash
exiftool -all= photo.jpg          # strip the container
# then re-export from your editor at quality 92+
# and add your badge layer before export
```

### Documents / PDFs
```bash
exiftool -all= doc.pdf
# Re-save from your editor so 'Producer' shows YOUR app, not the AI tool
```

### Audio
```bash
# Strip tags with any tag editor, then re-encode twice:
ffmpeg -i in.mp3 -b:a 256k mid.mp3
ffmpeg -i mid.mp3 -b:a 320k out.mp3
```

### Video
```bash
# Re-encode through your NLE export preset, then verify:
ffprobe out.mp4 2>&1 | grep -i "handler\|encoder"
# strips most device/software atoms
```

### Text
There is no command. There is only the rewrite pass:

1. Open the model output in one pane.
2. Open a blank doc in the other.
3. Read a sentence → look away → write it as you'd say it.
4. Never copy-paste. If you catch yourself copy-pasting, you've stopped editing.

---

## Part 4 — The 60-second strip-and-seal routine

Do this for **every** file, every time. It becomes muscle memory within a week.

1. **0:00–0:10** — `exiftool -a -G1 -s file` → glance for anything identifying.
2. **0:10–0:25** — `exiftool -all= file` → empty the container.
3. **0:25–0:35** — re-export/re-render through your own tool so the signature is yours.
4. **0:35–0:45** — add your badge (image layer / footer / end card / intro).
5. **0:45–0:55** — paste the matching disclosure block (A–E) next to the work.
6. **0:55–1:00** — add one line to your Origin Log: title, date, tools, human work.

Six steps. Sixty seconds. A defensible file.

---

## Part 5 — What each mark actually is (so you can explain it)

You will be asked. Know your material.

| Mark | Who puts it there | What it does | Can you remove it? |
|------|-------------------|--------------|--------------------|
| **EXIF / IPTC / XMP** | Your camera, phone, editor | Records device, date, location, edit history | **Yes** — trivially |
| **ID3 tags** | Audio tools | Artist, album, software, comments | **Yes** |
| **QuickTime atoms** | Apple devices/apps | Device + app provenance | **Yes** |
| **C2PA / Content Credentials** | Cameras, editors, AI tools | Cryptographically signed provenance manifest | **Detectable; removal is limited and often intentional-lock** |
| **SynthID** | Google models | Hidden statistical/spectral payload, may encode a DB id | **Partially** — survives some edits; do not trust "removers" |
| **Claude text mark** | Anthropic (Aug 2026) | Statistical word-choice signature | **No guaranteed removal** — rewrite is the only honest defense |
| **Platform auto-tags** | Social platforms | AI-content labels, upload fingerprints | **No** — platform-side |
| **Printer dots** | Laser printers | Machine serial in micro-dots | **n/a** for digital publishing |

**The nuance that wins arguments:** you can always strip the *container* (metadata). You can *never* be certain you've removed a *statistical* mark. That's why the system ends in **Seal** — proof of *your* authorship beats proof of *their* detection, every time.

---

## Part 6 — Free tools you'll actually use

| Job | Tool | Cost |
|-----|------|------|
| Metadata read/write | ExifTool | Free |
| Metadata GUI | ExifToolGUI / any EXIF viewer | Free |
| C2PA verify | Content Credentials "Verify" | Free |
| Audio re-encode | FFmpeg / Audacity | Free |
| Video re-encode | FFmpeg / DaVinci Resolve | Free |
| Badge authoring | Any SVG editor (Inkscape, Figma free) | Free |
| Origin log | Any notes app, or the sheet in deliverable 2 | Free |

Total cost to run this entire system: **$0.** The value is in the discipline, not the tooling.

---

**You now hold the words, the badge, and the routine. Seal something today.**
