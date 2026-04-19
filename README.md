# shawn-voice

Personal voice-clone skill for Claude Code. Drafts Slack messages, emails, and other outbound comms in my voice — not AI slop.

Built 2026-04-19 from 3 months of my own Slack + Gmail corpus. The corpus is gitignored and never committed.

## How it works

5-register model (channel-first, audience-second):

1. **Slack internal** — DMs, public channels
2. **Slack external** — Slack Connect with customers/prospects
3. **Email internal** — @poly-ai.com recipients
4. **Email external (warm)** — established customer/prospect relationships
5. **Email external (formal)** — cold first-touch to senior strangers, legal/regulator, press first-touch, customer escalation, permanent-record commitments

Each register has its own rules for openings, shortforms, punctuation, and sign-offs. The core signature (hyphen-only, `Happy to X` offer pattern, direct concrete framing, no AI slop) is constant across all 5.

## Files

| File | Purpose |
|---|---|
| `SKILL.md` | Entrypoint. Trigger rules, audience detection, 4-pass draft flow. |
| `VOICE_PROFILE.md` | Style fingerprint. Core signature + 5 register modes. |
| `POLISH_RULES.md` | ESL drift fixes with signature carve-outs. |
| `SHARPNESS_RULES.md` | Precision rules, voice-protected patterns. |
| `ANTI_SLOP.md` | Banned AI patterns. Hard bans (em-dash) + nuanced ones. |
| `EXAMPLES.md` | Raw → polished pairs across all 5 register buckets. |
| `CALIBRATION.md` | Ambiguous patterns decided by me; defaults for the rest. |

## Install on a new machine

```bash
git clone git@github.com:shawnwun/shawn-voice.git ~/.claude/skills/shawn-voice
```

Claude Code auto-discovers skills in `~/.claude/skills/`. No additional config needed.

## Hard rules (locked)

1. **Hyphen only. NEVER em-dash (`—`).** The #1 AI tell in 2026 writing. Any em-dash in output fails the anti-slop gate.
2. **British English spelling.** `organise`, `realised`, `practise`.
3. **Slack register:** drops apostrophes (`im`, `dont`), uses shortforms (`prob`, `tbh`, `sth`).
4. **Email register:** proper contractions (`I'm`, `don't`), no shortforms (except rare `Sg` with specific close contacts).
5. **No slop:** never `Happy to help`, `Let me know if you have any questions`, `I hope this email finds you well`, `That said`, `Best regards`, trailing disclaimers, or bullet lists under 5 items.

## Corpus

Not in this repo. Kept locally at `_corpus/` on origin machine and gitignored. Rebuild corpus from fresh Slack + Gmail pulls if needed on a new machine; profile itself travels with the repo.
