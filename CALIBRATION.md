# CALIBRATION - Ambiguous Patterns (Shawn to decide)

Answer each; I'll update `VOICE_PROFILE.md` + related rule files. Default behavior (in parens) is what the skill does until you override.

**v2 update (email corpus added):** Some questions from v1 are now ANSWERED by the email corpus evidence - marked ✅ with the answer. A few new questions added at the bottom based on email patterns.

---

## 1. "I think" as hedge

You use "I think" a lot, even on assertive statements ("I think it is actually quite solid", "I think ideally we kill the majority").

**Question:** Keep "I think" as signature marker, or trim in sharpness pass when the claim is confident?

- [ ] Keep always - it's signature
- [ ] Trim when confident, keep when genuinely uncertain (**default**)
- [ ] Trim aggressively - replace with assertion

---

## 2. Shortforms in external emails ✅ ANSWERED BY CORPUS

**Evidence from 89 sent emails:** You do NOT use `prob`, `sth`, `tbh`, `btw` in emails. Email register is full words. Exception: `Sg` appears once ("Sg Scott, talk soon") with a close contact.

**Locked rule:** Shortforms in Slack only. No shortforms in email (with one personal-relationship exception, `Sg`, used sparingly).

---

## 3. "guys" as collective address

You use it internally: "I need that answer guys", "you all feel about the agent".

**Question:** External channels?

- [ ] Internal only (**default**)
- [ ] OK in Slack Connect, not in email
- [ ] OK everywhere

---

## 4. Em-dash density ✅ SUPERSEDED BY Q14

**Resolution:** Hyphen-only rule (Q14) makes this moot. No em-dashes at all. See Q14.

---

## 5. Slack emoji shortcodes

You use `:smile:`, `:point_up:`, `:partying_face:` in all Slack contexts including the external prospect channel.

**Question:** Keep in Slack Connect (warm), drop in email?

- [ ] Slack Connect yes, email no (**default**)
- [ ] All Slack yes, email no
- [ ] Drop in anything external

---

## 6. Humor words externally

`xd`, `haha`, `hahahah`, `loooool`, `naice` - natural internally.

**Question:** External?

- [ ] Never external (**default**)
- [ ] Slack Connect with warm customers OK
- [ ] Email no, Slack Connect yes

---

## 7. Questions without `?`

You drop `?` on rapid-fire asks internally: "whats the progress", "how's it".

**Question:** Fix where?

- [ ] Internal DM OK, internal channels + external all fix (**default**)
- [ ] Fix everywhere (you want precise)
- [ ] Fix only in external email

---

## 8. Apostrophe-less contractions ✅ ANSWERED BY CORPUS

**Evidence:** Email corpus has consistent proper contractions (`I'm`, `let's`, `doesn't`, `I'll`). Slack drops apostrophes (`im`, `lets`, `doesnt`, `whats`).

**Locked rule:** Slack-only signature. Fix in email output.

---

## 9. "Can you X please" with no comma

Your directive pattern. No comma before "please".

**Question:** Polish externally (add comma) or keep as signature?

- [ ] Signature everywhere (**default**)
- [ ] Add comma externally ("can you X, please")

---

## 10. British vs American spelling ✅ ANSWERED BY CORPUS

**Evidence:** Email corpus is consistently British - `organise`, `realised`, `cc` lowercase. The "practise" in Slack wasn't a one-off.

**Locked rule:** British English default. Fix American spellings.

---

## 11. "tbh" for prefacing a hot take

You use "tbh we can take out letter since John W has already figured it out".

**Question:** Keep in external when softening a critique?

- [ ] Slack Connect yes, email no (**default**)
- [ ] All external OK - softens well
- [ ] Internal only

---

## 12. Multi-question bursts

"Why tailscale can only support 3 funnels?" "Can I login remotely without the browser?" "Can I just attach the token in the url?" - 3 messages in a row.

**Question:** Allowed externally?

- [ ] Internal only - consolidate externally (**default**)
- [ ] OK in Slack Connect, single message externally
- [ ] Always consolidate into one message

---

## 13. "Alright" as decision-opener

"Alright let's go with JWT and auto refresh-..."

**Question:** External?

- [ ] All contexts (**default** - it's signature)
- [ ] Internal only
- [ ] Replace with "OK - let's go with X" externally

---

## 14. "—" (em-dash) vs "-" (hyphen) ✅ LOCKED 2026-04-19

**Answer:** **Hyphen (`-`) only. NEVER em-dash (`—`).** All contexts - Slack, email, internal, external.

**Why:** Em-dash is the #1 AI writing tell in 2026. Banning it kills the strongest "this reads AI" signal. All other voice markers stay intact - this is the single typographic cut.

**Implementation:** Any `—` in output fails the anti-slop gate and gets rewritten with `-`.

---

## 15. Handling of existing drafts

When you paste a draft and ask "fix this", the skill currently runs Polish + Sharpness + Anti-slop but preserves voice-draft as-is.

**Question:** Should it also apply Pass 1 (voice redraft) when the raw draft doesn't feel voice-aligned?

- [ ] Preserve raw, polish only (**default** - trust the raw intent)
- [ ] Redraft if raw feels generic/AI-ish
- [ ] Ask "keep as-is or redraft?" each time

---

## Bonus: channel classification review

These channels from your corpus were classified automatically. Flip any that are wrong:

| Channel | Classified | Confirm? |
|---|---|---|
| `#prospect_upstream-rehabilitation_cba` | external | ✓ / ✗ |
| `#ai-enablement-marketing` | internal | ✓ / ✗ |
| `#ai-enablement-sales` | internal | ✓ / ✗ |
| `#bot-exchange-intel` | internal | ✓ / ✗ |
| `#bot-founders` | internal | ✓ / ✗ |
| `#claude-tips-share` | internal | ✓ / ✗ |
| `#claude-usage-monitoring` | internal | ✓ / ✗ |
| `#raven-omni-rollout` | internal | ✓ / ✗ |
| `#sales-intel-daily` | internal | ✓ / ✗ |
| `#tech-team-leaders` | internal | ✓ / ✗ |
| `#product-management` | internal | ✓ / ✗ |
| `#series-d-extension` | internal | ✓ / ✗ |
| `#analyst_relations` | internal | ✓ / ✗ |
| `#ai-tool-enablement` | internal | ✓ / ✗ |

Any DMs where the counterparty isn't @poly-ai.com? Flag for external tagging.

---

---

## NEW QUESTIONS (v2 - from email corpus)

## 16. "Happy to X" offer pattern

Corpus: 10+ uses in email - "Happy to chat", "Happy to jump on a call", "Happy to!", "Happy to clear this up".

**Currently:** Protected as signature (differs from banned "Happy to help" slop).

**Question:** Confirm?

- [ ] Yes, keep "Happy to X" as signature (**default**)
- [ ] Only keep in external emails
- [ ] Retire - too close to AI slop

## 17. "Sg Scott, talk soon" - the "Sg" abbreviation

Rare corpus use, once with Scott Hutchinson.

**Question:** Where should skill deploy this?

- [ ] Only with the specific close contacts where corpus shows it (safest) (**default**)
- [ ] Any internal-peer email
- [ ] Any warm external relationship
- [ ] Never auto-generate - keep it exclusively your own hand-typed marker

## 18. "!?" punctuation ("Let me know if the following works for you!?")

Quirky signature you use occasionally.

**Question:** Reproduce in drafts?

- [ ] Yes, when warmth-with-a-question fits (**default** - rare, but yours)
- [ ] Avoid - too eccentric, use standard `?`

## 19. `CC @X to help coordinate/organise` delegation

Signature in email. Heavily used with Claire Moore (EA).

**Question:** When a draft needs routing, which form?

- [ ] `CC @Claire to help organise` (matches corpus - keep `to help` infinitive) (**default**)
- [ ] `Looping in @Claire to coordinate` (also in corpus)
- [ ] Whichever fits the flow of that specific message

## 20. "Great question" at external email openings

Corpus: "Hi Apoorva, Great question - happy to clear this up!" (PG&E response to Salesforce).

**Question:** Use when substance follows, reject when it's just filler?

- [ ] Yes - keep when followed by concrete answer, reject when followed by fluff (**default**)
- [ ] Always reject (too close to AI slop)
- [ ] Always OK in external warm emails

## 21. Email internal register - "guys what are we dragging this for?"

You write to internal peers in email very much like Slack.

**Question:** When drafting internal emails to peers, default to which register?

- [ ] Slack-like casual with full contractions (**default**)
- [ ] Email-standard Hi/opening/full sentences - even to peers
- [ ] Match the thread's existing register

## 22. Email signatures / sign-offs

Corpus shows minimal sign-offs: often none, sometimes `thanks!`. Never `Best`, `Regards`, `Sincerely`.

**Question:** Confirm skill default?

- [ ] No sign-off by default, `thanks!` when warmth called for (**default**)
- [ ] Always include `thanks` or similar
- [ ] Use `Shawn` as name sign-off in external cold/first-touch

---

**Once you've answered (can skip ones you don't care about), I'll update VOICE_PROFILE + rule files + install the skill at `~/.claude/skills/shawn-voice/`.**
