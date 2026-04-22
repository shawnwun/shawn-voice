# EXAMPLES - Raw (Shawn wrote) vs Polished (target)

Concrete transformations that preserve voice while fixing drift and sharpening. Grouped by bucket.

---

## Internal Slack DM (terse, directive)

### 1. To AI assistant - directive (keep as-is)
**Raw:** `please can you ingest all docs into the wiki : ~/Downloads/gartner-research-april26/`
**Polished:** (same)
**Note:** Signature register - lowercase, "please" at end, colon before path. No drift.

### 2. To AI assistant - status check (keep)
**Raw:** `whats the progress`
**Polished:** (same)
**Note:** Missing apostrophe + `?` deliberate. Terse on purpose.

### 3. To peer - playful
**Raw:** `[Peer]s bot friends are using the strongest model to talk nonsense lol`
**Polished:** `[Peer]'s bot friends are using the strongest model to talk nonsense lol`
**Change:** missing possessive `'s` (genuine possessive, not a signature drop).

### 4. To peer - routing decision
**Raw:** `Speak to him - he gave the clawbot to a few people so he is fully in charge of that spending`
**Polished:** `Speak to him - he gave the clawbot to a few people, so he's fully in charge of that spending.`
**Change:** `-` → em-dash, comma before "so", `he is` → `he's`.

### 5. To peer - metaphor (keep)
**Raw:** `The precise burst is [Engineer] surgically training models`
**Polished:** (same)
**Note:** Metaphor is voice. "The precise burst" is a signature noun phrase - keep.

### 6. To peer - dry humor (keep)
**Raw:** `we have this another guy using 2x of you, i feel that is prob a bit of ai slop there so i give you the gold medal`
**Polished:** `we have another guy using 2x of you, i feel that's prob a bit of ai slop there - so i give you the gold medal`
**Change:** "this another" → "another" (article drift), `that is` → `that's`, comma before "so" → em-dash (punchier). Keep lowercase, `prob`, "ai slop" usage.

---

## Internal Slack channel (more structured)

### 7. Update announcement
**Raw:** `Just built a polyai market wiki, currently ingested 48 gartner latest and most relevant researches, which I think can help us prepare the briefing next week [link] - I will try to get it into Claude tmw`
**Polished:** `Just built a polyai-market-wiki - ingested 48 of Gartner's latest research reports. Should help us prep the briefing next week. [link] I'll try to get it into Claude tmw.`
**Changes:** `currently ingested` → `ingested` (cut filler); `researches` → `research reports` (plural); em-dash instead of comma for structure; dropped "which I think" (assert); `I will` → `I'll`.

### 8. Tech decision
**Raw:** `I think ideally we kill the majority of those and move all to Claude otherwise we don't have visibility`
**Polished:** `Ideally we kill the majority of those and move everything to Claude - otherwise we have no visibility.`
**Changes:** Dropped `I think` (confident); `move all` → `move everything`; em-dash before consequence; `don't have` → `have no` (punchier).

### 9. Call for action
**Raw:** `I need that answer guys let's launch an investigation and report please`
**Polished:** `I need that answer, guys - let's launch an investigation and report back please.`
**Changes:** Comma before `guys`; em-dash before action; `report` → `report back` (clearer). Keep `guys` + `please` at end (signature).

### 10. Tool share
**Raw:** `btw I hosted this sales mcp here: https://github.com/PolyAI-LDN/sales-mcp for all the services that dont support native MCP yet`
**Polished:** `btw I hosted this sales mcp here: https://github.com/PolyAI-LDN/sales-mcp - for all the services that don't support native MCP yet.`
**Changes:** Em-dash before the qualifier; `dont` → `don't` (public channel, slight polish); period at end. Keep `btw`, lowercase.

---

## Internal email (longer form)

### 11. Update email (synthesized in voice - replace with real corpus in v2)
**Raw:** `Hey team, wanted to share update on the platform migration. We finished the backend cutover last week and tests are looking good. prob 2 more weeks to close out edge cases. Let me know if any concerns.`
**Polished:** `Hey team - quick update on the platform migration. Backend cutover finished last week, tests look good. Prob 2 more weeks to close out edge cases. Flag any concerns.`
**Changes:** em-dash after Hey; "wanted to share update" → "quick update" (direct); split into punchier sentences; `Let me know if any concerns` (slop) → `Flag any concerns` (direct + voice). Keep `prob`, em-dash.

---

## External Slack Connect (prospect / customer)

### 12. Demo share - real corpus
**Raw:** `@Colleague1 @Colleague2 :point_up: an agent Claude Code built which I think it is actually quite solid, prob some UX can be tweaked if we really want it. I use this opp to develop my agentic workflow, and I thought I feedback here to the team to see how you all feel about the agent.`
**Polished:** `@Colleague1 @Colleague2 :point_up: an agent Claude Code built - I think it's actually quite solid, prob some UX can be tweaked if we really want. I used this opp to develop my agentic workflow, and wanted to share it here so the team can feel out the agent.`
**Changes:** `which I think it is` (ESL interference) → em-dash + `I think it's`; `if we really want it` → `if we really want` (trim); `I use` → `I used` (past tense); `I thought I feedback here` (drift) → `wanted to share it here`; `see how you all feel` → `the team can feel out`. Keep `prob`, em-dash, `:point_up:`, casual tone.

### 13. Routing decision - real corpus
**Raw:** `Whether you want to use it or not, up to the deal team @Colleague1 @Colleague2`
**Polished:** `Whether you want to use it or not - up to the deal team. @Colleague1 @Colleague2`
**Changes:** Em-dash for pivot; period before mentions. Minimal - the voice is clean.

---

## External email warm (existing customer / prospect, mid-engagement)

### 14. Incident flag (synthesized)
**Raw:** `hey - wanted to flag that we're seeing some intermittent issues on the call routing, prob impacting 1-2% of calls. my team is digging in and I will update you by EOD.`
**Polished:** `Hi [Customer] - quick heads up: we're seeing intermittent issues on call routing, probably affecting 1–2% of calls. My team is digging in. I'll update you by end of day.`
**Changes:** `hey` → `Hi <name>` (email convention, named recipient); `wanted to flag that` → `quick heads up:` (direct); `prob` → `probably` (external email polish); `impacting` → `affecting` (precise); `my team` → `My team` + period (split sentence). Keep em-dash, standalone action sentence.

---

## External email cold (first touch, press, analyst)

### 15. Reconnect (synthesized)
**Raw-style:** `Hi, we met at the [Conference] summit last week. I wanted to reconnect on what we discussed re conversational ai roadmap - happy to set up a call if useful. Let me know.`
**Polished:** `Hi [Contact] - we met at the [Conference] summit last week. I'd like to reconnect on the conversational AI roadmap we discussed. I can set up a call next week if that works - here are a couple of slots that work on my side: [link].`
**Changes:** Named recipient; em-dash after `Hi [Contact]` (signature); `wanted to reconnect on what we discussed re X` → `reconnect on the X we discussed` (clean); `happy to` → `I can` (direct, not slop); `Let me know` (banned) → concrete offer + slot link. Keep em-dash.

---

## Real email corpus examples (v2 from sent mail)

### E1. Internal peer forward - terse directive
**Raw (sent):** `guys anything you need to do here?`
**Polished:** (same)
**Note:** Signature. Lowercase in this context is casual internal email forward. Keep.

### E2. Internal peer forward - directive with deadline
**Raw (sent):** `@Colleague1 @Colleague2 please pick up first thing tomorrow`
**Polished:** (same)
**Note:** Classic directive pattern. "please" before the ask. No ceremony. Keep.

### E3. External customer - tech explanation
**Raw (sent):** `Hi [Contact], we identified that the issue stems from long Chinese title encoding during processing, which invalidates the Azure length limit. We have a fix in place…`
**Polished:** (same)
**Note:** Clean external-warm technical explanation. Good template for customer support replies.

### E4. External - warm check-in
**Raw (sent):** `Hi [Contact] - hope the customer trip went well. Still around until Saturday if you want to find a window this week.`
**Polished:** `Hi [Contact] - hope the customer trip went well. Still around until Saturday if you want to find a window this week.`
**Change:** `-` → em-dash (signature). Minimal.

### E5. External - declining with warmth
**Raw (sent):** `Hey [Contact] - no worries at all! Saturday doesn't quite work as I'm heading back to London. Let's make it happen next time I'm in the valley. Hope Spain is good!`
**Polished:** `Hey [Contact] - no worries at all! Saturday doesn't quite work as I'm heading back to London. Let's make it happen next time I'm in the valley. Hope Spain is good!`
**Change:** `-` → em-dash only. This is a model external warm decline - preserves warmth while being direct about constraint.

### E6. External investor - brief reply
**Raw (sent):** `Hi [Investor], I have asked the team to look into it. Do you remember the names of the two voices you are referring to?`
**Polished:** `Hi [Investor], I've asked the team to look into it. Do you remember the names of the two voices you were referring to?`
**Changes:** `have asked` → `I've asked` (contraction for flow); `are referring` → `were referring` (tense match - the investor was referring to them, past action). Direct, no slop. Keep short.

### E7. External first-touch (cold intro via mutual contact)
**Raw (sent):** `Hi [Contact], Nice to e-meet you… topics: 1. per user token usage [and more discussion points]`
**Polished (fuller version):** `Hi [Contact], Nice to e-meet you - thanks for setting this up. Topics I'd like to cover: 1. per-user token usage, 2. ..., 3. ... Looking forward to it.`
**Note:** "Nice to e-meet you" - signature. "e-meet" keeps in external-cold intros. Add em-dash + concrete list.

### E8. External warm - tech setup reply
**Raw (sent):** `Hi [Contact] and team, [new_user]@[vendor].com has been added to the account. Regarding next week's session, could you let us know what time works?`
**Polished:** (same)
**Note:** Model external technical-warm email. "Regarding X" pivot is clean. Keep.

### E9. Internal peer email - ultra-casual
**Raw (sent):** `wanna send [Colleague] there?`
**Polished:** (same)
**Note:** Peer DM-style in email. Shawn writes to the cofounder this way. Preserve. Don't add greeting/closing.

### E10. Internal peer email - playful
**Raw (sent):** `Should we just do PE play? Lol`
**Polished:** (same)
**Note:** Internal exec DM in email. "Lol" OK here. Preserve.

### E11. External chase - frustrated directive (internal-to-team forward)
**Raw (sent, internal):** `Guys what are we dragging this for?`
**Polished:** (same)
**Note:** Signature bluntness. Fragment. No apostrophe on "what are we" is fine (already grammatically OK). Keep.

### E12. External warm - offer + routing
**Raw (sent):** `Hi [Contact], Happy to chat - looping in [EA] to help organise from our side!`
**Polished:** `Hi [Contact] - Happy to chat. Looping in [EA] to help organise from our side.`
**Changes:** Em-dash after name. Period after "chat" (split from routing). Trailing `!` - keep if warmth needed, drop if neutral. Signature offer pattern + CC-routing preserved.

### E13. External cold - intro accept
**Raw (sent):** `Hi [Contact], Great to meet you, just RSVPed, looking forward to it.`
**Polished:** `Hi [Contact] - great to meet you. Just RSVPed, looking forward to it.`
**Changes:** Em-dash after name. Lowercase "great" (start of clause after em-dash). Period between "you" and "Just RSVPed" (tighten comma splice).

### E14. External - customer technical response about routing
**Raw (sent):** `Hi [Contact], Great question - happy to clear this up! [Customer] uses several numbers with different traffic splits… The [specific line] is already 100% [platform]…`
**Polished:** `Hi [Contact] - great question. Happy to clear this up: [Customer] uses several numbers with different traffic splits. The [specific line] is already 100% [platform]...`
**Changes:** Em-dash after name; "great question" lowercase; colon instead of "!" for lead-in; cleaner punctuation. "Great question" kept because substance follows (per ANTI_SLOP nuance).

### E15. External - quick no
**Raw (sent):** `I'm good thanks`
**Polished:** (same)
**Note:** Signature minimal reply. Perfect as-is.

### E16. Signature abbreviation
**Raw (sent):** `Sg [Contact], talk soon`
**Polished:** (same)
**Note:** "Sg" (Sounds good) is a rare Shawn-signature. Use only with specific close contacts. Don't deploy generically.

### E17. Internal forward with FYI
**Raw (sent):** `FYI - @[Colleague] can you help to look into this and maybe share some thoughts in the slack channel?`
**Polished:** `FYI - @[Colleague] can you help look into this and share some thoughts in the slack channel?`
**Changes:** `-` → em-dash; `help to look` → `help look` (drop "to"); dropped "maybe" (filler). Keep FYI + @-routing + "please"-free directive (terseness is appropriate for internal peer).

---

## Anti-pattern examples (what NOT to produce)

### Bad (AI slop)
> Hi team! I hope you're all doing well. I wanted to take a moment to share a quick update on our platform migration. It's worth noting that we've made significant progress this week. The backend cutover has been successfully completed, and the tests are showing promising results! That said, we still have approximately 2 more weeks of work to address the remaining edge cases. Please don't hesitate to reach out if you have any questions or concerns. Thanks!

**Why it's slop:**
- "I hope you're all doing well" (filler)
- "I wanted to take a moment" (filler)
- "It's worth noting" (banned hedge)
- "Successfully completed" (filler adverb)
- "Promising results!" (ceremony + exclamation)
- "That said" (banned transition)
- "approximately" → "about" or drop
- "Please don't hesitate to reach out" (banned closing)
- "Thanks!" (lazy close)

### Good (Shawn-voice equivalent)
> Hey team - quick update on the platform migration. Backend cutover finished last week, tests look good. Prob 2 more weeks to close out edge cases. Flag any concerns.

---

## External email FORMAL (v3 - cold first-touch to stranger, legal/regulator, customer escalation, permanent record)

### F1. Cold first-touch to senior analyst (stranger)
**Bucket:** Email external formal (analyst, no prior contact)
**Polished:**
> Hi [Analyst],
>
> [Colleague] mentioned you just joined [Analyst Firm] covering voice AI - good to connect. I run engineering at PolyAI; we build voice agents for enterprise customer service, mostly Fortune 500 in banking, hospitality, and utilities.
>
> I'd like to set up a 30-minute briefing to walk you through what we're doing and hear your research priorities for the year. A few slots that work on my side: [link]. If you'd prefer to start async, our latest product notes are here: [link].
>
> Best,
> Shawn Wen
> CTO, PolyAI

**Register shift from warm-external:** Proper `Hi [Name],` (no hyphen), `good to connect` warmth marker, `I'd like to set up` (first-touch formality) instead of `Happy to set up`, sign-off with title. Hyphen kept. Voice kept. 80 words instead of 215 in AI-slop version.

### F2. Customer escalation / written apology
**Bucket:** Email external formal (customer escalation)
**Polished:**
> Hi [Customer],
>
> Apologies for the disruption on the call-routing yesterday. We identified the root cause within [X] minutes (a race condition triggered by the new [subsystem] rollout) and deployed a fix at [time]. Service has been stable since.
>
> I'd like to walk you through what happened and our plan to prevent a recurrence. Are you free for a 20-minute call this week? A few slots on my side: [link].
>
> Best,
> Shawn

**Register shift:** `Apologies for` (plural, ESL-correct), specific detail (timing, subsystem cause), direct ownership `I'd like to walk you through`, concrete call slot. No "We deeply apologise" / "Please rest assured". Voice stays Shawn. Formality adds proper close.

### F3. Board / investor formal update (excerpt)
**Bucket:** Email external formal (board/investor, permanent record)
**Polished:**
> Hi [Investor],
>
> Quick update ahead of Wednesday's call. Q1 ARR landed at $X.XM (+Y% QoQ); three of the top five deals in pipeline slipped to Q2, two for procurement reasons and one timing. We are on track for H1 targets.
>
> On the platform side, we shipped the [integration] to GA last week and three enterprise customers have adopted it. [Colleague] can walk through the architecture on the call if useful.
>
> Best,
> Shawn

**Register shift:** Facts-first, `I think` trimmed, specific numbers, concrete adoption (`three enterprise customers`), offer specific follow-up (`[Colleague] can walk through`). No "We're very excited to report" / "thrilled to share". Sign-off `Best, Shawn` since the investor knows you.

### F4. Regulator / legal response
**Bucket:** Email external formal (legal/compliance, high formality)
**Polished:**
> Dear Ms Thompson,
>
> Thank you for your letter dated 14 April regarding our data processing arrangements. I confirm the following in response to your three questions:
>
> 1. [concrete answer]
> 2. [concrete answer]
> 3. [concrete answer]
>
> If you need further documentation, I can arrange a call with our Head of Security and Compliance, or provide written materials - whichever is more useful.
>
> Kind regards,
> Shawn Wen
> CTO, PolyAI

**Register shift:** `Dear Ms Thompson` (regulator formality), numbered list appropriate here (3 distinct concrete answers), `I confirm the following` precise legal tone, two concrete next-step offers. `Kind regards` + full title since permanent record. No slop. Voice stays professional Shawn, not corporate-counsel Shawn.

---

## Sensitive-topic Slack (v3 edge-case polish)

### S1. Internal Slack - sensitive topic texture
**Context:** Announcing a teammate's exit to the team.

**❌ Too flat (old rule allowed this):**
> heads up - alex is leaving end of month. sam ping me re transition.

**✅ With texture rule applied:**
> Heads up - Alex decided to move on end of month. His call, and I think it's the right one for him. Sam - can you take the lead on transition planning this week? I'll ping you separately on scope.

**What changed:** Proper capitalisation (apostrophe-fix applied because sensitive topic). One sentence of texture acknowledging Alex's agency. Specific ask to Sam with concrete timing. Still terse - just not FLAT.

---

## Usage notes

When drafting, find the closest bucket + closest example. Transform the ask through the same rule set. Check Anti-slop last.

When a raw draft is ambiguous between two buckets (e.g. email that's technically to an external domain but basically internal because of long relationship), ask the user: `internal or external register?` - one line, don't guess.

**For formal register detection:** default to formal when any of these flags are present:
- Recipient is senior exec / board / investor / regulator / press
- Topic is legal, compliance, customer escalation, or permanent-record commitment
- Recipient doesn't know Shawn yet (first contact, no warm intro chain beyond mutual name-drop)

When in doubt between warm and formal: **ask Shawn one line** - "warm or formal register for this one?"
