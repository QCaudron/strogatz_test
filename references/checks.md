# Checks: signatures, fixes and evidence

Open this file when a verdict is unclear, or when the user asks why a check exists. Each check gives its test, its signature (what a failure looks like on the page, so you can quote it as proof), the structural fix, and its evidence.

Evidence IDs (R1 to T2, A1 to A7, TM1 to TM7, NL1 to NL10) refer to the project's evidence ledger, which stays with the source project and is not shipped. Tiers:

- **U** the user's stated bar.
- **S** Strogatz's own words (his 2014 essay in the *Notices of the AMS*, read in full).
- **P** his observed practice (small samples, one rater).
- **L** learning-science support (mostly lab studies on short passages).
- **A** the skill designer's calibration: no source sets it, and the user can change it.
- **I** inferred.

**Baseline** marks what 15 rewrites made without this skill actually did (one model, five drafts, one rater). Those counts are patterns, not rates.

## Blockers

Any one blocker means the material does not yet obey the rule. Count a blocker only where you can quote the failing place; count each defect under one check (a missing or distant reason is W1 only; a term before the point is J1 only; where the case sits is C1, not X1), and list every failing place. Zero blockers: leave; one: patch every failing place of that check; two or more real blockers: rebuild. Wording you would choose differently is not a blocker, and neither is boilerplate, though a patch or rebuild deletes it.

### R1 The point

- **Passes when** the point, how or why the whole system or idea works (its central mechanism, not one step's), starts by about word 100 (hard maximum 150) (a term before the point counts under J1). The point may span up to three consecutive sentences, and must be concrete enough that a reader could predict one outcome from it. The central mechanism stated by word 100 passes even if its reason comes later; a late reason is a W1 matter only if it sits beyond the next paragraph. For a finding, decision or chat answer, the point is that answer, with its size or reason. This patch reading keeps a draft with one real blocker from being rebuilt. For an unmotivated newcomer only, a question may stand in by about word 100 if the answer arrives by a quarter of the piece.
- **Edge cases:** if only a closing summary states how or why, or no sentence does, R1 fails. An opening that names a tool or method ("... using a scoring model") does not state how, so it does not pass. When the mechanism is stated at the start, a closing summary that adds only a consequence does not make R1 fail.
- **Signature:** no claim, question or result in the first 100 words; background, history or a restated prompt first; a topic sentence where an answer belongs ("This note describes the cache", or "The cache speeds up reads with an eviction policy", which names a tool but not how); a sentence on how one step works standing in for the whole; the point stated only in a closing summary ("In short").
- **Fix:** lift the sentence that states the answer, often the closing summary, into the opening, with its reason. Move or cut what stood above it. State the answer, not the topic.
- **Evidence:** R1, A1. Tier U, A. Confidence moderate for the direction, low for the numbers. Strogatz poses his question or promise by word 25 to 140 in all 12 pieces measured (median about 60), but states his central claim later (median about word 156; 4 of 8 written pieces within 150). R1 is stricter than Strogatz by design; say so under "Declined for your bar" when it matters.
- **Baseline:** by one rater's manual positions, the point moved more than 10 words later in 6 of 15 rewrites; on a good draft, a new framing section pushed it from word 41 to word 115. With the skill, one smoke run took an opening topic sentence for the point, passed R1 and patched a draft whose answer sat in its closing summary; the how-or-why test above was added for that.

### R2 Hook

- **Passes when** any hook is the question itself or comes back as the first worked case; two lines at most in technical drafts.
- **Signature:** an opening scene, anecdote or quotation that the rest never uses; a hook longer than the point it delays.
- **Fix:** cut it, or make it the worked case and move it to where the case belongs.
- **Evidence:** R2, NL6. Tier U, P, A (the two-line cap is a proposal, not a measurement). Confidence moderate. 7 of 12 of his hooks carry the question. One long separate hook (in one piece, Q2) worked because it returned as the worked case; that rests on a single piece.
- **Baseline:** 0 of 15 rewrites added a hook.

### W1 Why

- **Passes when** every step, rule, exception, definition and section has a stated reason in its paragraph or the next. A bare value is never a step and never gets `[why: ?]`: a floor, cap, limit, window, count, timeout, cutoff, delay or schedule constant with no stated reason ("the tank never drops below 20%", "at most 12 per batch") goes in one "Optional" line of the note, on every path. A condition that changes what happens when a limit binds is a rule. For an expert reader, a rule whose reason any practitioner of the field would supply is an "Optional" item, never `[why: ?]`. Before the note, sweep every rule, exception, override or special case: each with no reason in its own paragraph or the next ends its sentence with `[why: ?]`. A new worked walk-through counts as an addition. In development round 2, bare numbers were still marked in 6 of 15 rewrites while 16 rules went unmarked. A rule, exception, override or special case is a step: it needs its reason, or its sentence ends with `[why: ?]`, because the non-obvious design choices usually live there. Test: in "a lift carries at most 8 people", "why 8?" is a value (Optional); "a full lift skips floors until someone gets off" is a condition (its reason, or `[why: ?]`).
- **Signature:** runs of "Next, X" with no "so that", "because" or "the problem this solves"; bare-noun headings; a separate "Why" or "Rationale" block far from the steps it explains; a rule stated only as a rule.
- **Fix:** move each stated reason beside its step. Where the draft states none, derive one only by arithmetic or logic from the draft's own statements and flag it `[added: verify]`; otherwise end the rule's sentence with `[why: ?]`. A purpose is never derivable, and a reason that says what a rule is for, however worded, is a purpose. Then list every "so", "because", "since", "to", "in order to" or "this prevents" clause in the rebuild that is new (not verbatim from the draft; a connective that only restates a link the draft itself states is not new), and label each new one: `[added: verify]` if derived by arithmetic or logic (a new "so" joining two draft facts is derived), otherwise `[why: ?]` or cut. Name the listed clauses in the note, even if none; in development round 3 the check said "all copied" 13 of 13 times beside unlabelled derived clauses. A marker is exactly `[why: ?]` or `[added: verify]`, at the end of its sentence, with no label, colon or word inside or before it; in development round 1, labelled markers in 3 of 10 rewrites leaked into the text readers saw.
- **Evidence:** W1. Tier U, S. Confidence moderate. This is the user's first complaint. Strogatz states a reason about once per 195 words, and reasons for definitions are rare in his pieces (2 of 62 counted moves), so "every definition" is the user's bar, not his rate.
- **Baseline:** under the prompts that did not restructure, the end block stayed where it was (4 of 4 drafts that had one). Under the prompt "say why before how", the rewrites wrote in reasons that neither the draft nor its fact sheet gave, on 5 of 5 drafts.

### W2 Question first

- **Passes when** the reader's question is posed before it is answered.
- **Signature:** assumptions, then definitions, then results; a mechanism described before the reader knows what problem it solves.
- **Fix:** open with the problem the material solves, or the question it answers, in one line, then the answer.
- **Evidence:** W2. Tier S, L. Confidence high. In the Notices essay he names answering questions the reader has not yet asked as the failure of the usual format. Lab evidence (pretesting) supports question-first only when the reader can try to answer; a rhetorical question may not count.

### J1 Jargon

- **Passes when** every load-bearing term (one a later step needs) is glossed where it first appears, or described before it is named, relative to the stated reader. Decorative terms are cut. When the reader is a guess, a field term the draft uses unglossed throughout is an "Optional" line at the gate, not a J1 failure, because the guess may be wrong in either direction. A private term of the author's own system that the draft never explains is a failure.
- **Signature:** a term of art with no gloss at first use; an undefined acronym; the same thing named three ways; "it" or "this" with no clear referent; a definition several paragraphs after first use.
- **Fix:** move the draft's own definition to first use; describe the thing, then name it; cut a term no later step needs. In a rebuild, gloss in a few words each load-bearing field term the assumed reader may lack, from common knowledge, its sentence ending `[added: verify]`, and list it on the note's reader line ("glosses resting on it"). A gloss explains a term, never why the author's system acts. For a named expert reader, a term the draft uses unglossed throughout stays unglossed. A private term of the author's system that the draft never explains stays a gap: keep it, invent no meaning, and list it under open gaps without a marker.
- **Evidence:** J1. Tier U, P, L. Confidence moderate. He glosses a median of 67% of terms within a sentence (73% within four); that the rest are not load-bearing is the rater's inference. Glossing what an expert already knows hurts experts, hence "relative to the stated reader".
- **Baseline:** one rewrite glossed a basic field term for an expert reader; two added general-knowledge glosses without a flag.

### S1 Skipped step

- **Passes when** no jump is too big for a reader at the stated level to take in one move; no "clearly", "obviously" or "it follows" stands in for a step; a deliberate skip is named with its reason.
- **Signature:** a result where a calculation should be; a symbol used before it is defined; a worked example with fewer steps than the reader could check in their head.
- **Fix:** insert the missing step from the draft's own material, or name the skip and say why ("the second case repeats this argument, so it is left out"). If the step is not in the draft, mark the gap; do not invent the mechanism.
- **Evidence:** S1, TM7. Tier U, P, L. Confidence moderate. An LLM reader fills in steps that a novice could not, so this check is weaker when a model runs it.

### X1 Complexity

- **Passes when** the delete test finds nothing that hides or complicates the point, the simple version comes before refinements, and the system is not made to sound harder than it is. A lone aside, recap or hedge in an otherwise clear draft is an "Optional" line, not a blocker; a rebuild still cuts it.
- **Signature:** long words where plain ones exist; stacked caveats before the main idea; the general case before the small one; notation or edge cases introduced and never used; impressive but irrelevant detail.
- **Fix:** run the delete test on explanatory material only (asides, history, analogies, restated points, hedges): if removing it breaks nothing later, remove it. Put the simple version first. Never delete constraints, warnings, numbers, preconditions, limits, edge cases or mechanism clauses; move them, or list them under "Removed".
- **Evidence:** X1, NL7. Tier U, L. Confidence moderate. More complex text was judged to come from less intelligent authors (Oppenheimer 2006, abstract), and irrelevant detail lowers transfer in short lessons. The delete test is the design's tool; no study tests it.

### I1 Insight

- **Passes when** the reader can say why it must be so, predict what changes if an input changes, or handle a variant.
- **Signature:** every claim asserted and none traced; components listed with what each "does" and no case run through them; nothing the reader could try.
- **Fix:** trace the smallest case through the steps, and close by returning to the opening point, now earned by the case, with no new claim. Then run the variant check: one question the text does not trace (another input, a boundary), answered from the draft's rules and from the rebuild's, quoting the sentence each answer rests on; if the answers differ, the rebuild changed a rule, so restore it. By default (design M7, settled by the user), a fresh reader that sees only the rebuild and the variant question answers it, or says "cannot tell", and the text is repaired if it cannot tell; the inline check is the fallback. In round 3 the inline check reported "same" 13 of 13 times with no working shown, which is why the note now quotes both sentences. In development rounds 1 and 2, self-run checks certified every rewrite (10 of 10, then 15 of 15), including one whose closing line contradicted its source.
- **Evidence:** I1, NL8. Tier U, L. Confidence moderate. A smooth explanation can raise confidence without raising learning, so insight is shown by questions the text must answer, not by how it feels. Weak point: an LLM reader overstates insight; a human reader is the backstop.

## Strong checks

These feed the "Strogatz" verdict, not the gate. (`SKILL.md` points here for them.)

| ID | Check | Signature | Fix | Tier; confidence |
|---|---|---|---|---|
| W1b | No stretch over about 500 words without a stated reason | A long run of steps or description with no "because" | Bring in the draft's reason, or mark the gap | P, A; low (500 is a calibration; his longest stretches ran 273 to 543 words) |
| C1 | One small case, small enough to list or trace in full, runs through the parts before the general statement; checked once per document | Parts described with no case, or the case only at the end | Move the case up and thread it through the steps | P, L; moderate |
| C2 | Names and notation arrive after the thing they name | A definition or symbol before the reader has seen what it names | Show the thing in the case, then name it | P; moderate |
| C3 | The hard step goes by picture, trace, trick or the story of someone stuck, and what is not the point is said | The hardest step asserted in one sentence | Trace it on the case; say which details do not matter | P; moderate |
| C4 | An analogy carries structure the reader needs, states its mapping and names where it breaks | "X is like Y" with no mapping; several analogies in a row | State which part maps to which and where it fails, or cut it | L; moderate (mapping), low (break point) |
| E1 | The payoff returns to the opening question | The end answers a different question, or none | Close on the opening point, now earned by the case | P; high |
| F1 | Reasoning in sentences with connectives; formatting only for list- or table-shaped content | Bold lead-in bullets; a header every 100 words; table cells holding sentences; few "because", "so", "but" | Turn dependent steps into prose; keep lists for independent items | U, I; low |
| H1 | Simplifications and unknowns stated once, plainly; no stacked hedges | "May", "typically", "generally" piled up; a caveat repeated | State each simplification once, where it applies | S, P; moderate |

## Polish checks

Not in `SKILL.md`. Use them only after every blocker passes.

| ID | Check | Signature | Fix | Tier; confidence |
|---|---|---|---|---|
| E2 | The ending adds something (an implication, a limit, an open question) and does not repeat | A last paragraph whose sentences map onto earlier ones | End on what it unlocks, a limit or an open question that the draft states; add no new claim | P (folk evidence); low |
| T1 | No praise without a mechanism ("fascinating", "powerful") and no topic-level enthusiasm. Naming a trick and saying why it works is fine; Strogatz does it. Wonder attaches to a consequence. The reader's ignorance is never their failing | Exclamation marks; praise of the topic or method; "simply" or "just" before a hard step | Cut the praise; if something is surprising, say what follows from it | S, P, I; low |
| T2 | Where cheap, the idea turns up somewhere unexpected. Skip in technical documents | None needed | One sentence naming a second place the same mechanism appears | P; moderate |

## The never-list, with evidence

`SKILL.md` orders the list with the most common or most costly first. The ledger IDs are in design order.

| Never | Ledger ID | Tier | Baseline (15 rewrites) |
|---|---|---|---|
| Reformatting in place of restructuring | NL3, NL9, F1 | U, I | One prompt kept the draft's order on 5 of 5; headers in 10 of 15; bullets rose on all 9 rewrites of prose drafts |
| An invented reason or purpose | NL7 | I | 5 of 5 drafts, under the prompt "say why before how"; with skill v1.2, unsupported claims in 4 of 10 rewrites (development round 1) |
| The draft's example altered, or a stated fact turned into a hypothetical | NL7 | I | 1 altered example; 3 facts recast as "suppose" |
| Lengthening (aim for no longer than the draft; add no paragraph without removing one) | NL5 | L, A | 9 of 15 grew more than 10%, up to 48%; causes: a framing section, a duplicated example, unneeded glosses |
| A new section above an early point | NL4, R1 | U, A | 1 (word 41 to 115) |
| Reasons left in a block at the end | W1 | U, S | The block stayed in 4 of 4 drafts that had one, under two of three prompts |
| A closing line that adds a claim | NL7, E2 | I | With skill v1.2: one closing line contradicted its source, and one turned an observation into a pattern (development round 1) |
| The same example told twice | NL5 | L, A | 2 |
| A general-knowledge addition without `[added: verify]` | NL7 | I | 1 to 3 per rewrite under one prompt (4 of 5 drafts), 1 to 2 under another (1 draft), by an auditor |
| Scaffolding for an expert | J1 | U, P, L | 1 |
| A lost mechanism clause | NL7 | I | 2 clauses lost, in 3 rewrites; no number or named term lost |
| Enthusiasm, praise, friendly boilerplate | NL2 | I | 0 added; the draft's own was removed in 6 of 6 |
| A hook that is not the question | NL6 | U, P | 0 |
| Preamble, stacked hedges, "In summary", restated question | NL4 | L, I | 0 preambles; the draft's closing "In short" kept in 3 of 3 rewrites of one draft |
| Analytic-sounding sentences with no mechanism | NL10 | I | 0 |
| An analogy without a mapping | NL1 | L, I | 2 added; both carried structure, neither named where it breaks |
| Parts described without a traced case | NL8 | L, I | Not testable: every draft already had a case |

`SKILL.md` lists the six most common or costly; the rest live here, kept because a weaker model may show what this one did not.

## Calibration by reader

The principle (empathy for a specific reader) is constant; the surface changes.

| Reader | What changes |
|---|---|
| Newcomer, unmotivated | Spend the first lines making them care. A short scene is allowed only if it is the question. Smallest case, pictures, every term glossed. |
| Informed outsider | Point and reason first. One small case. Gloss each term once. |
| Practitioner | Point and reason first. Make the route the subject. Drop scaffolding they already have. Keep a reason for each step, and flag what is skipped. |
| Expert | Claim, then evidence. No re-explaining. Keep the reasons for non-obvious choices. |

## The final test, in five questions

`SKILL.md` carries the short form (two verdicts and "Declined for your bar"). This is the fuller version, for review mode or when the user asks for more.

1. **Whose question is this answering?** Is it one this reader would ask, and does the material make them care before it answers? (W2, R1)
2. **Where does the reader take the last step?** Quote the small case, picture or prediction that lets them reach the insight themselves. If you cannot quote one, the answer is "nowhere". (I1, C1, A6)
3. **Is every step motivated?** Count steps with a stated reason, a supplied reason and an open gap. (W1)
4. **Is it honest and no harder than necessary?** Simplifications named once; nothing that flatters the explainer; nothing invented about the author's system. (H1, X1, NL7)
5. **Would an anxious reader feel welcome?** Ask only when the reader may be a newcomer. No "simply", no "obviously", no gate of jargon. (T1, J1)

Then the verdicts: "Your bar" (met with no failing place; "met except open gaps" with the open gaps listed, meaning `[why: ?]` items and unmarked private terms; or not met with the checks named); "Strogatz" (proud only with the reader's last step quoted and no strong check failing; otherwise nearly with the one fix, or not yet with the reason; rated on craft only, so a late point, a scene or aside before the point or a held-back answer never supports nearly or not yet); "Declined for your bar" (his moves left out because the user's bar overrides them, or, in review mode, found and not counted against him: a late point, a scene before the point, an answer held back for suspense, a warm aside, a heavy term left named but unglossed, as he does on the podcast).

## Numbers with no source

These are the author's calibration (tier A). The user can change any of them.

- The point by about word 100, hard maximum 150 (R1).
- No stretch over about 500 words without a reason (W1b).
- Net length within about 10% of the original (NL5). This is pass mark 2; the skill itself now asks for no longer than the draft.
- Two lines at most for a hook in technical drafts (R2; a proposal in the research, not a measurement).
- The short-material guard (about 120 words) and the long-document guard (about 1,500 words).
