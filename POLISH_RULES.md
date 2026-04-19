# POLISH_RULES - ESL Drift Fixes

Fix these errors WITHOUT removing Shawn's signature. Each rule lists exceptions.

---

## Articles (a / an / the)

**Rule:** Add missing articles where English requires them in complete sentences.

| Raw | Polished | Note |
|---|---|---|
| sent you PR | sent you a PR / sent you the PR | concrete |
| bring it to peaceful end | bring it to a peaceful end | abstract |
| In Feb | In Feb | fine - fragment reply |
| I need that answer guys | OK as-is | imperative |

**Exceptions (don't add articles):**
- Slack DM one-liners: "sent PR", "pushed fix" - informal register preserved
- Imperative fragments: "push repo to remote please"
- Technical shorthand: "use Bedrock", "check Datadog"

---

## Prepositions

**Rule:** Fix wrong preposition collocations.

| Raw | Polished |
|---|---|
| in you env | in your env (typo + prep) |
| implications to X | implications for X |
| depend of | depend on |
| impact to | impact on |
| help me to do X | help me do X (drop `to`) |

**Shawn-specific drifts:**
- `to` vs `for` in "implications/impact" - default to `for` unless literal direction
- `on` vs `about` in "think on/about" - default to `about`

---

## Plural / singular agreement

**Rule:** Match number between determiner, subject, and verb.

| Raw | Polished |
|---|---|
| these usage | this usage |
| those budget | those budgets |
| this numbers | these numbers |
| researches | research / research reports |
| feedbacks | feedback (uncountable) |

---

## Tenses & modals

**Rule:** Fix awkward modal + past-participle combinations.

| Raw | Polished |
|---|---|
| would got evicted | would get evicted |
| the session would got | the session would get |
| I thought I feedback here | I wanted to share it here |
| has already figured out | OK |

---

## Mandarin → English interference

**Rule:** Collapse interference patterns without killing the directness.

| Raw | Polished | Pattern |
|---|---|---|
| I don't necessarily don't want | I'm not against it / I don't necessarily not want | double negative |
| you are leading the usage there very impressive | you are leading the usage there - very impressive | adjective placement → use hyphen to reintroduce |
| is not sth can be shown easily | is not sth that can be shown easily | missing `that` |
| we we think about | we think about | duplicate word |
| very like it | really like it | adverb choice |
| more better | better / much better | ESL comparative |
| can you help me to X | can you help me X | drop `to` |
| which I think it is actually quite solid | - I think it's actually quite solid | split awkward relative clause with hyphen |

---

## Connectors (that / which / who)

**Rule:** Add missing relative pronouns where the sentence breaks without them.

| Raw | Polished |
|---|---|
| This is not sth can be shown | This is not sth that can be shown |
| an agent Claude Code built which I think... | an agent Claude Code built - I think... |
| something I been working on | something I've been working on |

---

## Email-specific ESL drift (from 89-email corpus)

Email register requires cleaner output than Slack. These appear repeatedly in Shawn's sent emails - always fix.

| Raw | Polished | Pattern |
|---|---|---|
| Apology to get back to you late | Apologies for getting back to you late | wrong singular + preposition |
| interested to reconnect | interested in reconnecting | prep + gerund |
| what's the title of the agreement (reported) | what the title of the agreement is | reported-question word order |
| There seem to be an issue | There seems to be an issue | subject-verb agreement |
| it would be great that we can prep | it would be great if we could prep / great to prep | subjunctive construction |
| these two days | the last couple of days | Mandarin time-reference calque |
| Which account id you are using | Which account ID are you using | question word order |
| I check my cal | I checked my cal / I just checked my cal | tense (check → checked) |
| I happen to be in the Bay Area | I'll be in the Bay Area / I happen to be in SF that week | "happen to" subtle misuse |
| one note | one other note / quick note | article missing |
| have started looking into agent development processes and using AI agents to automate issue tracking, ticket creation, or even self-improvement | OK - keeps long sentence intact in email register | preserve |

## Spelling typos

**Rule:** Fix genuine typos where intent is clear.

| Raw | Polished |
|---|---|
| swtich | switch |
| optiona b | option b |
| Nikolas bot (possessive) | Nikola's bot |
| tmw | tomorrow (external only - signature in internal) |

**DO NOT fix (deliberate casual style):**
- `doesnt`, `im`, `whats`, `dont`, `it is` vs `it's` - internal register
- `prob`, `sth`, `tbh`, `btw`, `obv`, `ofc`, `opp` - shortform shorthand
- `naice`, `xd`, `loooool` - play spellings
- `:smile:`, `:point_up:` - Slack shortcodes

---

## British vs American spelling

Shawn mixes both. Corpus shows: "practise" (British), but also American forms.
**Default to British English** for spelling (`colour`, `organise`, `practise`). Flag inconsistency in CALIBRATION for user lock-in.
