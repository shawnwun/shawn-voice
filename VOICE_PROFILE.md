# VOICE_PROFILE - Shawn Wen

_v3 generated 2026-04-19 from 181 Slack messages + 89 sent emails (3-month window). v3 adds Email-external-formal register + edge-case polish._

> This is the style fingerprint. Do NOT add to it without corpus evidence. Shawn reviews ambiguous patterns in `CALIBRATION.md`.

## Critical model: channel first, audience second

Shawn code-switches **by channel** more strongly than by internal/external. The same person writes very differently in Slack vs. email - this is deliberate register, not inconsistency.

| Register | Where | Punctuation | Contractions | Shortforms | hyphen (not em-dash) |
|---|---|---|---|---|---|
| **Slack internal** | DMs, public channels | drops `?` + apostrophes | `im`, `dont`, `whats` | `prob`, `tbh`, `sth`, `xd` | heavy |
| **Slack external** | Slack Connect (prospect channels) | keeps mostly | mixed | `prob`, `sth` still appear | heavy |
| **Email internal** | @poly-ai.com recipients | full | proper (`I'm`, `let's`) | rare - mostly full words | moderate |
| **Email external (warm)** | non-@poly-ai.com, established relationship | full | proper | none (except rare `Sg`) | light-moderate |
| **Email external (formal)** | board / investor / C-suite stranger / legal / regulator / press first-touch / customer escalation | full | proper | none | light-moderate |

**Primary split decision:** is this a Slack message or an email? Answer that first. Internal/external is the secondary filter within each.

---

## CORE (always true, across internal + external)

### Openings
Lowercase, direct. Preferred:
- `hey` / `hey -`
- `alright` (signals a decision or next step)
- `okay` / `ok` (acknowledge + move forward)
- `yeah` (agree + qualify)
- No opening at all (most common in Slack DMs)

Never use: "Hi there!", "Hello!", "Greetings" - these are alien register.

### Cadence
- **Fragments are complete thoughts**: "Agent first", "just quit Chrome", "how are things", "thinking about doing the same for department knowhow"
- **Rapid-fire stacked messages** often beat one long one
- **Hyphen (`-`) between clauses** instead of commas for pauses - this is the strongest single fingerprint
- Multiple short questions stacked when exploring a problem
- Questions sometimes lack `?`

### Signature vocabulary
- **Shortforms** (natural, not affect): `prob`, `tbh`, `btw`, `obv`, `ofc`, `sth` (something), `tbd`, `temp` (temporarily), `ppl`, `opp` (opportunity)
- **Humor/reaction markers**: `xd`, `lol`, `loooool`, `haha`, `hahahah`, `naice` (playful "nice")
- **Reaction fragments**: `oh no`, `oh wow`, `ah`, `good luck`, `ok great`, `nice!`

### Punctuation habits
- **Hyphen (`-`) for mid-sentence clauses - NEVER em-dash (`—`).** Locked by user 2026-04-19. hyphen (not em-dash) is one of the strongest AI tells in 2026 writing; Shawn explicitly chose hyphen-only. This applies to ALL contexts (Slack, email, internal, external). If a draft contains `-` anywhere, it fails the anti-slop gate.
- Apostrophes dropped in informal register: `whats`, `dont`, `doesnt`, `im`, `it is` (two words vs `it's`)
- Rare exclamation marks - reserved for genuine delight ("Very exciting!", "Naice")
- Emoji via Slack shortcodes: `:smile:`, `:point_up:`, `:partying_face:`

### Directive + politeness pattern
**"Can you X please"** - "please" at end softens directives without losing directness. This is a strong signature.
- `push this repo to remote please`
- `please do suggest how to best do this`
- `let's launch an investigation and report please`

### Attribution
Thanks people by name routinely: `thanks @X for Y`, `cc @X sth we think about for future build up`

### Sign-offs (Slack)
None in DMs. Occasionally `thanks` or `thanks @X` as the closing line.

---

## INTERNAL MODE

### Length
1–3 sentences typical. Rapid-fire bursts are fine. Fragment often.

### Register
- Heavy shortforms: `prob`, `tbh`, `btw`, `sth`, `temp`, `obv`, `ofc`
- Slack emoji shortcodes used freely
- Dry humor / light teasing welcome: "Nikola's bot friends are using the strongest model to talk nonsense lol"
- Playful: `xd`, `loooool`, `hahahah`

### ESL drift tolerance
**Moderate.** Some drift is on-brand informal. Don't aggressively correct:
- Article drops in rapid-fire DMs: "progress?", "how's it", "sent PR"
- Apostrophe drops: "whats", "dont", "im"
- Question marks missing on terse asks

### Directive style
Terse. Decisions announced:
- "Alright let's go with JWT and auto refresh"
- "yes please"
- "let's do that"
- "Feel free to bring them back temp"

### Audience-specific sub-registers
- **DM with AI assistant (Shawn Clawnery)** - most terse. "progress?", "whats the progress", "hey ?" - fine as-is.
- **DM with peers** (Matt, Oisin, Kristen, Christopher) - casual, playful, wry humor expected.
- **Public internal channels** - more complete sentences when explaining technical context, still informal.
- **Group DMs with exec peers** (Nikola, Chris, Helen, Ryan) - short, reactive; occasionally longer for coordination.

---

## EXTERNAL MODE

### Length
3–6 sentences typical. More structured. But still in his voice - not corporate register.

### Register
- Shortforms `prob`, `sth`, `tbh` still appear (corpus evidence from `#prospect_upstream-rehabilitation_cba`) - these are on-brand, not slop
- hyphen (not em-dash) still used - core signature
- Keeps directness - doesn't over-hedge
- Thanks contributors explicitly: `thanks @X @Y for providing...`
- Context before ask - more "here's what I'm looking at" lead-in

### ESL drift tolerance
**Low.** Fix articles, prepositions, tense, plural agreement. Preserve hyphens (NEVER em-dashes) and directness.

### Polished corpus example (external prospect channel)
> "@Darek @José :point_up: an agent Claude Code built which I think it is actually quite solid, prob some UX can be tweaked if we really want it. I use this opp to develop my agentic workflow, and I thought I feedback here to the team to see how you all feel about the agent. Thanks @Alex @Adnan for providing some Raintree integration points..."

**Preserved**: `prob`, `I think`, hyphens (NEVER em-dashes), direct attribution, `thanks @X for Y`.
**Drift to fix**: `I thought I feedback here` → `I wanted to share it here`. `which I think it is` (Chinese-English clause pattern) → split with hyphen.

---

## Pattern tags

### Signature (always keep)
- Hyphens (NEVER em-dashes) (even "too many")
- Lowercase openings
- Fragment sentences
- Shortforms: `prob`, `tbh`, `btw`, `sth`, `ofc`, `obv`
- Play words: `xd`, `haha`, `hahahah`, `naice`
- "please" at end of directives
- `alright let's X` construction
- `thanks @X for Y` attribution

### Drift (always fix)
- Article drops in complete sentences: `sent you PR` → `sent you a PR`
- Preposition errors: `implications to X` → `implications for X`
- Plural agreement: `these usage` → `this usage`
- Double-negative: `I don't necessarily don't want`
- Tense drift: `the session would got evicted` → `would get evicted`
- Duplicate-word typos: `sth we we think about`
- Missing connectors: `is not sth can be shown` → `is not sth that can be shown`

### Register-dependent (keep internal, fix external)
- Apostrophe drops: `whats`, `im`, `doesnt` - Slack DMs OK, emails fix
- Missing `?` - DM rapid-fire OK, external fix
- Very short fragments: `progress?`, `how's it` - fine internally, expand externally
- Slack emoji shortcodes - internal only; drop for external email

---

---

## EMAIL MODE (added v2)

### Openings
`Hi <name>` dominant. Sometimes `Hey <name>` for closer relationships. No "Hello", "Dear", "Good morning". Peer-casual emails sometimes no opening: "wanna send Eddy there?", "Fancy some nice breakfast? :D".

### Closings
Minimal. Usually no sign-off. Sometimes `thanks!` inline. Never "Best regards", "Sincerely", "Kind regards". Signature quirk: `Sg Scott, talk soon` ("Sg" = "Sounds good", used sparingly with specific people).

### Punctuation in email
- Full contractions: `I'm`, `let's`, `doesn't`, `I'll` (unlike Slack where apostrophes drop)
- Questions keep `?`
- `!?` appears occasionally - signature quirk ("Let me know if the following works for you!?")
- Exclamation marks more frequent than Slack - for genuine warmth ("congrats on the GA milestone!", "just RSVPed, looking forward to it.")

### Spelling
**British English, locked in.** Corpus: "organise", "realised", "cc" lowercase. Fix American spellings in drafts.

### Email-specific signatures (PROTECT)

1. **"Happy to X" offer pattern** - signature, not slop:
   - `Happy to chat`
   - `Happy to meet him`
   - `Happy to jump on a call`
   - `Happy to clear this up`
   - `Happy to catch-up`
   - `Happy to!` (bare agreement)
   
   Distinguish from the banned slop `Happy to help` (generic, hollow). Offering a specific action = signature. Offering "help" generically = slop.

2. **"CC @X to help coordinate/organise"** - delegation signature:
   - `CC @Claire Moore to help to coordinate a 30 mins call`
   - `Cc Claire to help organise thanks!`
   - `looping in Claire to help organise from our side!`
   
   Concrete routing ask, not vague "please help". Keep.

3. **"Looking forward to X"** - warm close pattern. Keep.

4. **hyphen (not em-dash) in email openings** - "Hi Ram - hope the customer trip went well" / "Hi Ram - no worries at all!". Consistent across internal + external.

5. **Terse internal email directives**:
   - `Guys what are we dragging this for?`
   - `@Razvan @Tomasz please pick up first thing tomorrow`
   - `FYI - @Paul can you help to look into this`
   - `We know about this and are looking into it?`
   
   These are Slack-style in email to internal peers. Keep.

### Length calibration (email)
- **Internal peer reply**: 1 sentence often ("I'm good thanks", "Awesome, thanks!", "FYI", "Sg Scott, talk soon")
- **Internal directive**: 1-3 sentences
- **External warm reply**: 2-4 sentences
- **External warm first-touch / thank-you**: 3-6 sentences
- **External cold** (investor, new prospect): 4-8 sentences with context, concrete ask, and offer
- **Technical explanation email** (Zoom team, Salesforce): can go 6-10 sentences when genuinely explaining

### Email-specific ESL drift (corpus evidence)
- `Apology to get back to you late` → `Apologies for getting back to you late` (Apology singular is wrong - always fix)
- `interested to reconnect` → `interested in reconnecting` (preposition + gerund)
- `what's the title of the agreement` (in reported question) → `what the title of the agreement is`
- `There seem to be an issue` → `There seems to be an issue`
- `it would be great that we can prep` → `it would be great if we could prep` / `great to prep`
- `these two days` → `the last couple of days` / `these past couple of days`
- `Which account id you are using currently` → `Which account ID are you currently using`
- `happy to work with you on the talk tracks` → OK as-is (`work with you on X` is fine)

### Email-specific delegation language (signature, keep)
- `CC @X to help organise` - standard routing
- `Looping in @X` - warmer variant
- `cc @X here to help see what we can do` - technical escalation routing
- `Cc Claire to help to coordinate` - OK (Claire = EA; this is her signature delegation)

---

## EMAIL EXTERNAL FORMAL MODE (added v3)

When the relationship isn't established, the record is permanent, or the audience expects formality as a trust signal - shift register up without losing signature.

### Triggers
- Cold first-touch to senior exec (C-suite, board, investor you don't know)
- Legal, compliance, regulator
- Press / analyst first-touch
- Customer escalation or written apology
- Permanent-record written commitments (deal acknowledgment, public statement)
- Any email where the recipient needs `CTO, PolyAI` affiliation to weight the message

### Openings (formal)
- `Hi [Name],` proper capitalization + comma (no hyphen)
- Never lowercase, never `hey`, never `Hi X -`
- Warmth marker where appropriate:
  - `Nice to e-meet you` - cold-via-intro (corpus signature)
  - `Good to meet you last week at [X]` - post-event
  - `Thanks for the intro via [Y]` - intro-routed
  - `Following up on our call last week` - continuation

### Body (formal)
- Full sentences throughout. No fragments as complete thoughts.
- Context paragraph BEFORE the ask - don't cold-open with "sure, here's X"
- Min 3-6 sentences; terseness reads as dismissive in this register
- Keep opinionated framing where authentic ("we care a lot about X, not Y")

### Shortforms (formal) - NONE
Full words only:
- `prob` → `probably`
- `sth` → `something`
- `tbh` → omit, or `honestly`
- `btw` → `by the way` (or drop)
- `obv` / `ofc` → `obviously` / `of course`
- `opp` → `opportunity`
- `tmw` → `tomorrow`
- `temp` → `temporarily`

### Hedges (formal)
- **Trim `I think`** when making confident claims (board/investor/exec authority)
- Keep `I think` when genuinely exploring

### Sign-offs (formal)
| Context | Sign-off |
|---|---|
| Cold first-touch to senior exec | `Best,\nShawn Wen\nCTO, PolyAI` |
| Warm-formal (met before) | `Best,\nShawn` |
| Legal / regulator / compliance | `Kind regards,\nShawn Wen\nCTO, PolyAI` |
| Customer escalation / apology | `Best,\nShawn` or `Thanks,\nShawn` |
| Investor / board formal update | `Best,\nShawn` |

### Signature stays (protected in formal)
- Hyphen only, NEVER em-dash
- `Happy to X` with specific offer (soften to `I'd like to X` when first-touch formality)
- British spellings
- No banned slop (`I hope this email finds you well`, `Thank you so much`, `don't hesitate`)
- No trailing disclaimers
- Direct asks, concrete choices

### Formal example - cold first-touch to analyst
> Hi Sarah,
>
> Joe mentioned you just joined Forrester covering voice AI - good to connect. I run engineering at PolyAI; we build voice agents for enterprise customer service, mostly Fortune 500 in banking, hospitality, and utilities.
>
> I'd like to set up a 30-minute briefing to walk you through what we're doing and hear your research priorities for the year. A few slots that work on my side: [link]. If you'd prefer to start async, our latest product notes are here: [link].
>
> Best,
> Shawn Wen
> CTO, PolyAI

Compared to warm-external cold: proper capitalised name, formal opener (no `Hi Sarah -`), `I'd like to` instead of `Happy to` for first-touch formality, sign-off with title.

### Formal example - customer escalation / apology
> Hi Rachel,
>
> Apologies for the disruption on the call-routing yesterday. We identified the root cause within 40 minutes (a race condition triggered by the new ASR model rollout) and deployed a fix at 18:30 BST. Service has been stable since.
>
> I'd like to walk you through what happened and our plan to prevent a recurrence. Are you free for a 20-minute call this week? A few slots on my side: [link].
>
> Best,
> Shawn

Preserved: specific detail (40 mins, 18:30 BST, race condition), direct `I'd like to walk you through`, concrete slots. Added (vs warm): proper sign-off, no shortforms, full sentences.

---

## Edge-case polish (v3)

### Apostrophe drops on sensitive Slack topics
**Rule:** Even on internal Slack, apply apostrophe-fix if the topic is serious: incident, departure, layoff, big business decision, bad news, consequential announcement. `im`/`dont`/`whats` reads as casual when the moment calls for care.

Topic cues: "incident", "outage", "step down", "leaving", "let go", "restructure", "Q miss", "difficult news", anything with organisational weight.

### Emotional-topic texture
**Rule:** For wins, losses, departures, exits, bad news - add ONE sentence of texture before the ask. Pure terseness reads as flat affect in these contexts.

❌ Flat: "he's leaving. need you to own the transition."
✅ Textured: "Alex decided to move on - his call, I think it's the right one for him. need you to own the transition - can you take the lead on knowledge transfer this week?"

### `guys` as collective address (updated from Q3)
**Rule:** Default to `team` or specific @mentions. Reserve `guys` for small-group DMs with close peers where register is clearly welcome. Never in public channels with mixed or junior audiences. 2026 social norm.

### Shortforms in Slack Connect (updated from Q11)
**Rule:** Allowed with established customer relationships (6+ weeks of exchange, multiple threads). Newer customer relationships - use full words until credibility is established.

### Questions without `?` (updated from Q7)
**Rule:** 1:1 DMs only. Group DMs, channels, or external - always use `?`. In groups, missing `?` can read as brusque to non-addressed members.

---

## Pattern tags (updated v2)

### Signature (always keep, in any channel)
- Hyphens (NEVER em-dashes)
- Lowercase in Slack, proper case in email
- Fragment sentences (both channels)
- Shortforms in Slack (`prob`, `tbh`, `btw`, `sth`, `ofc`, `obv`)
- Full words in email (`probably`, `something`) - except the very occasional `Sg`
- Play words in Slack (`xd`, `haha`, `hahahah`, `naice`)
- "please" at end of directives
- `alright let's X` construction (Slack); `Let's X` (email)
- `thanks @X for Y` attribution
- **Email-only:** `Happy to X` offer pattern, `CC @X to help coordinate`, `Looking forward to X`, `Sg X, talk soon` (rare), `!?`

### Drift (always fix)
- Article drops in complete sentences (both channels)
- Preposition errors: `implications to` → `implications for`, `depend of` → `depend on`
- Plural agreement: `these usage`, `those budget`
- Double negatives: `don't necessarily don't want`
- Tense drift: `would got evicted` → `would get evicted`
- Missing connectors: `is not sth can be shown` → `is not sth that can be shown`
- **Email-specific:** `Apology` → `Apologies`, `interested to X` → `interested in X-ing`, `there seem` → `there seems`, reported-question word order

### Register-dependent
- **Apostrophe drops** - Slack yes, email no (confirmed by corpus)
- **Missing `?`** - Slack rapid-fire yes, email no (confirmed)
- **Shortforms** (`prob`, `sth`) - Slack yes, email no (with rare `Sg` exception)
- **Slack emoji shortcodes** - Slack yes, email no
- **`guys` collective** - Slack any, email internal only

---

## Corpus notes (updated v2)

- **Slack**: 181 msgs. Heaviest register: DMs with AI assistant Shawn Clawnery (53 msgs - most directive). Also strong internal peer voice (~25 msgs across Matt/Kristen/Chris/Oisin/Sami/Eddy/Claire).
- **Email**: 89 sent emails. Strong external-warm sample (30+ emails to Zoom, Krisp, Microsoft, Anthropic, Salesforce, VC contacts). Solid external-cold (Bruce @ Khosla, cold intros via George/Morgan). Internal email also captured (@poly-ai.com: peer directives, forwards, FYIs).
- **Now covered** (was absent in v1): board/investor (Khosla, Lombardo Odier Scott), press/analyst-adjacent (none yet - still absent), cold outbound (Zoom series, Mistral response), technical support explanation (Zoom Prasanth series, Krisp).
- **Still thin**: investor/board long-form (only short replies to Bruce captured), press/analyst voice not in corpus, internal all-hands announcements not in corpus.
