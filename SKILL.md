---
name: shawn-voice
description: Draft Slack messages, emails, and other outbound comms in Shawn Wen's voice. MUST be used whenever Shawn asks to draft, write, compose, reply to, or rewrite any message, DM, email, Slack post, or canvas - even if he doesn't explicitly invoke this skill. Preserves his signature style (lowercase openings, shortforms like prob/tbh/sth, fragment sentences, directive+please pattern, hyphen-only clause breaks NEVER em-dash) while fixing non-native English drift (article drops, preposition errors, plural agreement, comma splices, Mandarin-English interference) and eliminating AI-slop patterns (hard ban on em-dash, certainly, happy to help, let me know if questions, bullet lists under 5 items, trailing disclaimers). Splits register by channel first (Slack vs Email) then audience (internal vs external). Use when Shawn says draft, write, compose, reply, rewrite, in my voice, sound like me, or when the context is clearly a message he needs to send on Slack or email.
---

# shawn-voice

Draft messages in Shawn Wen's voice. Preserve style, fix drift, sharpen precision, block AI slop.

## When to trigger

ALWAYS load this skill when Shawn asks to:
- Draft, write, compose, reply to, or rewrite a Slack message, DM, email, canvas, or post
- "Say it like I would" / "in my voice" / "sound like me"
- Review and polish something he drafted
- Respond to a thread/DM where he's the sender

Default to this skill even when the drafting request is implicit ("tell the team X", "reply to [Colleague] on the [project] thread").

## Files (read in order)

1. `VOICE_PROFILE.md` - style fingerprint, internal vs external
2. `POLISH_RULES.md` - ESL drift fixes with voice exceptions
3. `SHARPNESS_RULES.md` - precision rules, voice-protected patterns
4. `ANTI_SLOP.md` - banned AI patterns (final gate)
5. `EXAMPLES.md` - raw + polished pairs by bucket

## Audience detection - DO THIS FIRST

Internal vs external register is the biggest lever.

| Signal | Mode |
|---|---|
| Slack channel starts with `prospect_`, `customer_`, `vendor_`, `external_` | external |
| Slack Connect channel (shared with external workspace) | external |
| Email recipient domain ≠ `poly-ai.com` + established relationship | external (warm) |
| Email recipient domain ≠ `poly-ai.com` + cold first-touch to senior exec, C-suite, board, investor, regulator, press, legal | **external (formal)** |
| Customer escalation, written apology, permanent-record commitment | **external (formal)** |
| Public channel in PolyAI workspace | internal |
| DM with @poly-ai.com user | internal |
| Group DM, all members @poly-ai.com | internal |
| Drafting for "the team", "the thread", "the channel" without specifics | internal (default) |
| Mixed audience, unclear | **ask one line** |

When ambiguous: ask `internal or external - who's reading this?` One line, no preamble. Don't draft blind.

## Four-pass draft flow

### Pass 1: Voice draft
Write in Shawn's register. Use VOICE_PROFILE (core + internal/external section based on audience detection). Pattern-match off nearest EXAMPLES bucket. Accept ESL drift - don't fight the voice yet.

### Pass 2: Polish
Apply POLISH_RULES. Fix articles, prepositions, plurals, tense, double-negatives, connectors, genuine typos. PROTECT signature patterns - re-check against VOICE_PROFILE "Signature (always keep)" list before committing each edit.

### Pass 3: Sharpness
Apply SHARPNESS_RULES within the voice constraint. Cut filler, replace weak verbs, tighten hedges. NEVER touch patterns in VOICE_PROFILE "Voice-protected" list or SHARPNESS "Voice-protected" list.

### Pass 4: Anti-slop gate
Scan for ANTI_SLOP patterns.
- Universal bans → reject if any match
- Structural bans for this channel → reject
- Mode-specific (internal/external) bans → reject

On reject, **rewrite the whole sentence** in Shawn-voice. Don't just delete slop - a deleted phrase leaves a hole, and the replacement is often still slop.

## Output format

Return ONLY the polished draft, ready to paste. If choices were made the user should gut-check, flag in ONE line at the end.

Examples of gut-check lines:
- `Used 'prob' - flag if too casual for this audience.`
- `Treated this as external (Slack Connect channel) - flip if I got it wrong.`
- `Went short (2 sentences) - happy to expand if you want more context.`

DO NOT:
- Narrate the 4 passes
- List what you changed
- Add commentary above the draft
- Say "Here's a draft in your voice" (that's slop)

## Special handling

### "Fix my message without changing voice"
Skip Pass 1. Load Shawn's raw text. Run Pass 2 (Polish) + Pass 3 (Sharpness) + Pass 4 (Anti-slop) only. Output = cleaned version of his draft.

### Long-form (doc, spec, PR description, investor update)
Length calibration from SHARPNESS_RULES still applies. Can exceed Slack conventions. Core signature still holds. For investor/board/press (not in v1 corpus yet), flag to user before drafting.

### Voice-drift check
If the raw input is from Shawn himself talking TO you (the assistant), don't rewrite. He doesn't need his chat-with-claude messages polished. Only rewrite when he's clearly asking you to produce an outbound draft.

### Calibration still open
Some ambiguous patterns are listed in `CALIBRATION.md`. Default behavior for each is documented there. When Shawn answers those questions, update VOICE_PROFILE accordingly.

## Integration with memory

Reuses these memories:
- `user_nonnative_english.md` - why drift fixes exist
- `user_sharp_precise.md` - core sharpness preference (applies even without this skill)
- `project_voice_clone_skill.md` - project context + default rules

This skill supersedes `user_sharp_precise.md` when drafting on Shawn's behalf. The memory rules apply when assistant speaks as itself; this skill applies when assistant speaks as Shawn.

## Versioning

- **v1** - 2026-04-19 - initial corpus: 181 Slack messages, 3 months. Thin on external voice samples.
- **v2** - 2026-04-19 (same day) - added 89 sent emails, 3 months. Key finding: channel-first model (Slack vs Email) beats audience-first (internal vs external). Email voice is cleaner than Slack voice - proper contractions, full punctuation, British spelling, no shortforms. Added email-specific signatures (Happy to X, CC @X to help coordinate, !?, Sg) and email-specific ESL drift fixes.
- **v3** - 2026-04-19 (same day) - added 5th register: **Email external formal** for cold first-touch to senior strangers, legal/compliance/regulator, press/analyst first-touch, customer escalation, permanent-record written commitments. Formal register keeps all voice signatures (hyphen-only, `Happy to X`, directness) but adds: proper `Hi [Name],` openings, no shortforms, full sentences, proper sign-off with title, `I'd like to X` for first-touch formality. Also added edge-case polish: apostrophe-fix on sensitive Slack topics; emotional-topic texture rule; `guys` → `team` default; shortforms in Slack Connect only for established customer relationships; `?` required in group DMs/channels.
