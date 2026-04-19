# SHARPNESS_RULES - Precise and Punchy

After Voice draft + Polish, tighten construction. **Never touch protected signature patterns.**

---

## Weak verbs → specific verbs

Replace `be / have / do / make / get` where a concrete verb exists.

| Raw | Sharper |
|---|---|
| we have a meeting | we meet |
| make it work | ship / fix / land |
| get it done | ship / close |
| do some testing | test |

**Exception**: conversational turns, existential "there is/are" when natural.

---

## Cut filler

Delete unless load-bearing:
- `really` (exception: `Happy to pay really` - signature agreement pattern)
- `actually` (except when signaling correction/surprise: "this is actually a great bossy move")
- `basically`
- `just` (exception: imperative "just quit Chrome", "just added you" - signature)
- `kind of`, `sort of`
- `I think` - **trim when claim is confident**, keep when genuinely hedging

**Shawn-specific signature**: "I think it is actually quite solid" - `I think` is hedge AND signature. Keep in voice pass; sharpen only when claim is demonstrably certain.

---

## Hedges → assertions

Replace hedges where the claim is actually confident.

| Raw | Sharp |
|---|---|
| I think we should do X | Let's do X |
| It might be worth considering Y | Y is worth trying |
| Maybe we could... | Let's... |
| Happy to chat if useful | I can set up a call next week |

**Exception**: when genuinely uncertain - then hedge is correct.

---

## Concrete > vague

| Raw | Sharp |
|---|---|
| some issues | 3 tests failed |
| a lot of traffic | 2x traffic |
| soon | by Friday |
| we'll look into it | I'll check X by tomorrow |

---

## Cut bloat constructions

| Raw | Sharp |
|---|---|
| in order to X | to X |
| There is a problem with Y | Y is broken |
| There are three options | We have three options |
| in terms of | (usually just cut) |
| due to the fact that | because |

---

## Shortest word wins

Guard against Claude importing these into drafts (Shawn doesn't use them):
- `utilize` → `use`
- `implement` → `build` / `ship`
- `commence` → `start`
- `endeavor` → `try`
- `facilitate` → `help` / `enable`

---

## Length calibration by channel

| Context | Target length | Notes |
|---|---|---|
| Slack DM to AI assistant | 1–2 sentences | fragments fine |
| Slack DM to peer | 1–3 sentences | rapid-fire OK |
| Public internal channel | 3–6 sentences | explanatory |
| Slack Connect (prospect/customer) | 3–6 sentences | context + ask |
| External email (warm) | 4–8 sentences | greeting + context + ask + close |
| External email (cold) | 5–10 sentences | more ceremony, named recipient |

**Rule:** Default to the shorter end of each range. Every extra sentence must earn its place.

---

## Voice-protected (DON'T sharpen these away)

These look like rule violations but ARE the voice:
- Hyphens for clause breaks (NEVER em-dashes - see ANTI_SLOP hard ban)
- Fragment sentences ("Agent first.", "Naice")
- Shortforms: `prob`, `tbh`, `btw`, `sth`, `obv`, `ofc`
- "please" at end of directives
- `alright let's X` construction
- `thanks @X for Y` attribution
- `xd`, `haha`, `hahahah` in casual contexts
- "I think" when genuinely expressing a view (not just hedging)

---

## Mode-specific sharpness

### Internal sharpness (aggressive)
- Cut every hedge that isn't genuinely uncertain
- Drop ceremony ("I wanted to flag that..." → "Flagging:")
- Fragment where possible
- Directive + "please" at end, no softener

### External sharpness (careful)
- Preserve necessary context (don't start with the ask cold)
- Keep "I'd like to" / "I wanted to" openers when warming up
- Replace slop hedges ("Happy to help") with concrete offers ("I can set up a call next week")
- Keep hyphen and voice markers - they humanize
- Trim ruthlessly after warmth is established
