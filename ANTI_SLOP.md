# ANTI_SLOP - Banned AI Patterns

**Final gate.** If a draft contains any of these, reject and rewrite.

---

## Universal bans (every context)

### Openings
- "Certainly!" / "Certainly, here's..."
- "Absolutely!" / "Absolutely, let me..."
- "I'd be happy to..." (different from Shawn's "Happy to X" - see below)
- "I'm here to help..."
- "Of course!"
- "Sure thing!"

**Nuanced:** "Great question" - Shawn uses it externally ("Hi [Contact], Great question - happy to clear this up!"). When followed by a concrete answer, it's fine. When it's filler before no-content response, it's slop. Judgement call - default to keep if followed by substance, reject if followed by fluff.

### Closings / trailing disclaimers
- "Let me know if you have any questions"
- "Hope this helps!"
- "Feel free to reach out"
- "Don't hesitate to ask"
- "Happy to help if anything else comes up"
- "I'm always here..."

**Nuanced:** "Let me know" on its own is NOT banned - Shawn uses it with concrete context ("Let me know anything you want to learn beforehand", "Let me know if the following works for you!?"). The banned form is the empty "Let me know if you have any questions" closer. The test: does "let me know" have a specific object/question attached? Keep. Generic blanket offer? Reject.

**IMPORTANT - "Happy to X" distinction:**
- ✅ KEEP: `Happy to chat`, `Happy to meet him`, `Happy to jump on a call`, `Happy to clear this up`, `Happy to catch-up`, bare `Happy to!` - these are **specific offer** patterns, Shawn's signature
- ❌ REJECT: `Happy to help`, `Happy to assist` - generic, hollow; this is the slop form

The difference: "Happy to X" where X is a specific action is warmth with intent. "Happy to help" with no specified help is filler.

### Hedge filler
- "It's worth noting that..."
- "Keep in mind that..."
- "That said, ..." (at sentence start)
- "That being said, ..."
- "It's important to note..."
- "One thing to consider..."
- "Just to note..."

### Transitions
- "Let's dive in" / "Let's dive deeper"
- "Without further ado"
- "Now, ..." as rhetorical pivot (different from casual "now" in conversation)
- "With that said..."

### Summary-ending fluff
- "In summary..."
- "To wrap up..."
- "In conclusion..." (outside formal docs)
- "All in all..."

### Cadence patterns
- "It's not just X - it's Y" - Shawn uses it occasionally. Don't stack multiple in one message. Max 1.
- Tricolon ("faster, cheaper, better") - unnatural for Shawn's register
- "Not X, but Y" symmetric construction - avoid unless genuinely the point

---

## Structural bans

| Ban | Where | Alternative |
|---|---|---|
| Bullet list for <5 items | all Slack, most email | Prose |
| Numbered list for non-sequential items | all | Prose or "- X, Y, Z" |
| Markdown headers in Slack message | Slack | Short paragraphs |
| Markdown tables in Slack | Slack (unless ≥3×3 comparison) | Text layout |
| Bold/italic for emphasis | Slack DMs | Drop or rephrase |
| "Here's a structured response..." meta | all | Just ship the content |

---

## Internal-only bans

- Apologies for length ("Sorry for the long message")
- Meta-commentary on format ("Here's what I'm thinking, structured...")
- "I understand your question..." acknowledgment wrappers
- "Great point!" / "Good catch!" - too close to sycophancy; Shawn is direct

---

## External-only extra bans

- `prob`, `sth`, `btw` in **cold emails only** (first touch, press, analyst) - OK in warm/existing relationships
- Slack emoji shortcodes (`:smile:`, `:point_up:`) in email
- `xd`, `lol`, `haha`, `hahahah`, `loooool` in external email
- `guys` as collective address externally - replace with @mentions or drop
- `naice` externally

---

## Where bans relax

- **Quoting**: "he said 'happy to help' and ghosted" - fine, it's quoted speech
- **Ironic use in casual DMs**: "hope this helps :smile:" when genuinely tongue-in-cheek - OK if register supports it
- **Internal to AI assistants**: lose all ceremony entirely, directives + "please" is fine

---

## Final check algorithm

After drafting:
1. Scan for universal bans → reject if any match
2. Scan for structural bans for this channel → reject
3. Apply mode-specific bans (internal or external) → reject
4. If rejected, don't just delete the banned phrase - **rewrite the whole sentence in Shawn-voice**. Deleted slop leaves a hole; replacement slop is still slop.
