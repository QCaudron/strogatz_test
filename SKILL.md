---
name: strogatz-test
description: "Use when the user names the Strogatz Rule, the Strogatz test or the Steve test, asks you to make something obey the Strogatz Rule, or asks whether an explanation, lesson, design document, README or LLM answer obeys it; also when asked to make explanatory or teaching material more intuitive, better motivated or clearer by this standard. Never apply it to your own answer unasked. Not for ordinary requests to explain or summarize, and not for questions about Strogatz's books or mathematics."
compatibility: "Claude Code and OpenCode; needs only a file reader, to open the references."
---

# The Strogatz Test

The Strogatz Test, or Steve test, after the mathematician Steven Strogatz, asks whether explanatory or teaching material lets the reader know why each step is taken, reach the point fast, meet no unexplained jargon or needless complexity, and end with intuition they can use. The user's bar is the eight blockers below; their numbers are this skill's calibration. A rebuild changes the order of ideas, since new dressing on the old order fixes nothing. Check "Guards" (short, out-of-scope, long and story material) first.

Never stop to ask what the rule is or who the reader is: infer, state your guess in the note, the short report that ends every reply, and proceed. Nothing goes before the material or after the note: no preamble, afterword or working.

## Decide first: leave, patch or rebuild

A blocker is a check below that the draft fails at a place you can quote. Count each defect under one check: a missing or distant reason is W1 only; a term before the point is J1 only; where the case sits is C1 (a strong check: case before rule), not X1. Strong checks are never blockers and never count toward the gate. List every failing place.

First find the point: up to three consecutive sentences stating how or why the whole system or idea works (its central mechanism, not one step's), concretely enough that a reader could predict one outcome. For a finding, decision or chat answer, the point is that answer, with its size or reason. If only a closing summary states it, or nothing does, R1 fails. Naming a tool or method ("using a scoring model") is not stating how. The central mechanism stated by word 100 passes R1 even if its reason comes later; a late reason is a W1 matter only if it sits beyond the next paragraph.

| Blockers | Response |
|---|---|
| 0 | Leave the draft unchanged; reply with the note only. |
| 1 | Patch every failing place of that check, and delete boilerplate. |
| 2 or more | Rebuild, with the procedure below. |

It comes first because 15 of 15 rewrites made without this skill changed the draft, good ones included. Wording you would choose differently is not a blocker, nor is boilerplate.

| Blocker | Passes when |
|---|---|
| R1 Point | The point starts by about word 100 (at most 150); for an unmotivated newcomer, a question may stand in, answered by a quarter of the piece. |
| R2 Hook | Any hook is the question itself or becomes the first worked case; two lines at most in technical drafts. |
| W1 Why | Every step, rule, exception, definition and section has a stated reason in its paragraph or the next. A floor, cap, limit, window, count, timeout, cutoff, delay or schedule constant ("the tank never drops below 20%", "a lift carries at most 8 people") is a bare value: an "Optional" item, never `[why: ?]`. A condition that changes what happens, even when a limit binds ("a full lift skips floors until someone gets off"), is a rule. For an expert reader, a rule whose reason any practitioner of the field would supply is an "Optional" item, never `[why: ?]`. |
| W2 Question first | The reader's question comes before its answer. |
| J1 Jargon | Every load-bearing term (one a later step needs) is glossed at first use, or described before it is named, for this reader. For a guessed reader, a field term left unglossed is an "Optional" item, not a failure; an unexplained private term of the author's system fails. |
| S1 Skipped step | No jump this reader cannot take in one move; no "clearly" in place of a step; skips named with their reason. |
| X1 Complexity | The delete test (step 3) finds nothing that hides or complicates the point (a lone aside, recap or hedge is an "Optional" item); the simple version comes before refinements. |
| I1 Insight | The reader can say why it must be so, predict a change, or handle a variant. |

## Procedure

**1. Frame.** Take the reader from the user, or infer them from whom the draft addresses, and call it a guess. Calibrate to that reader (table in `references/checks.md`).

**2. Diagnose.** List each step and the reason the draft states for it, "none" where it states none, even if you can think of one: invented reasons start here. Run the blockers. Mark up to three places where Strogatz would stop to ask a newcomer's question: a fix if it matches a blocker, else an "Optional" item. Apply the gate.

**3. Rebuild from that list, not from the sentences.** Reorder it into this arc, then write prose:
1. The point and its reason, inside the runway (about the first 100 words).
2. The smallest concrete case, traced through the steps.
3. Names and notation, as nicknames for what the case showed.
4. The hard step, by picture, trace or trick; name any step you skip, and why.
5. The general statement, then special cases.
6. A close that returns to the opening point, now earned by the case; a limit or open question only if the draft states it.

For a system or design description the arc is: what it does and why, by its central mechanism; one input traced through every step; the general rules; the special cases. Other material: open `references/rebuild-patterns.md`.

While patching or rebuilding:
- Move each reason the draft states beside its step; dissolve any separate "Why" block.
- Every reason or purpose clause you write copies the draft, or is derived by arithmetic or logic and its sentence ends with `[added: verify]`. A derived reason is labelled; an unlabelled one counts as invented. A purpose is never derivable.
- Sweep before the note: every rule, exception, override or special case (never a bare value, and for an expert reader never a standard-practice rule) with no reason in its own paragraph or the next ends its sentence with `[why: ?]`.
- In a rebuild, move the worked case; do not copy it: tell it once, early. A new worked walk-through is an addition.
- Keep the draft's examples, values, names and facts exactly; never turn a stated fact into a "suppose".
- In a rebuild, apply the delete test: an aside, history, analogy, restated point or hedge goes if nothing later breaks without it. Anything else you take out goes under "Removed".
- Additions come in two classes. Allowed: common knowledge, its sentence ending `[added: verify]`, or an illustrative case labeled "(illustrative)"; in a rebuild, gloss each load-bearing field term the assumed reader may lack, ending `[added: verify]` (explain the term, never why the author's system acts). Never, flagged or not: a claim about the author's own system that the draft does not support. A private term the draft never explains goes under open gaps, unmarked; for a named expert reader, a term the draft uses unglossed throughout stays unglossed.

**Markers.** The only markers are exactly `[why: ?]`, `[added: verify]` and "(illustrative)". Each goes at the end of the sentence it belongs to, with no label, colon or word before or inside it.

**4. Verify before showing anything**, by checks visible from outside, because a writer grading its own work approves it. A patch runs Point, Because and Nothing lost.
- *Point*: quote it word for word in the draft and the rebuild, placed as the note shows; it must sit inside the runway and not move later.
- *Because*: list every "so", "because", "since", "to", "in order to" or "this prevents" clause in the rebuild that is new (not verbatim from the draft; a connective that only restates a link the draft itself states is not new). Label each new one: `[added: verify]` if derived by arithmetic or logic (a new "so" joining two draft facts is derived), otherwise `[why: ?]` or cut. Name the clauses in the note, even if none.
- *Variant*: ask one question the text does not trace (another input, a boundary); answer it from the draft's rules and from the rebuild's, quoting the sentence each answer rests on. If the two answers differ, the rebuild changed a rule: restore it. If you can delegate, give a fresh reader only the rebuild and the variant question; it answers from the text or says "cannot tell"; repair the text if it cannot tell.
- *Nothing lost*: every number, named term, constraint, precondition, limit, warning, edge case and mechanism clause ("rather than", "unless") of the draft is in the rebuild or under "Removed".
- *Length*: aim for no longer than the draft; add no paragraph without removing one. If you estimate it more than 10% longer, cut the weakest added material before replying; never call a rebuild over 5% longer "within 5%". If only reasons, glosses, constraints and the case remain, stop and say so.
- *Structure*: if the point did not move into the runway (when it began outside) and no step moved, merged or dropped, the rebuild is cosmetic.

Make one repair pass, then report what remains.

## Output

Do the diagnosis and checks silently: write none of it outside the note. The reply is what the mode below lists, and nothing else.

**Patch or rebuild**: the material first, then a blank line and the note, whose first line is exactly "Strogatz Test". A patch returns the whole material with only the failing places changed and boilerplate deleted; it adds no title or heading. Never add the rule's name to the material.

```
Strogatz Test
Reader assumed: <one line>  (guess | stated); glosses resting on it: <list, or none>
Gate: <failing checks> -> leave | patch | rebuild
Point (draft: <first paragraph | by the end of the second paragraph | later>; now: <same choices>): "<up to three consecutive sentences of the material, word for word, without markers>"
Outline before -> after (at most 10 lines; steps moved, merged, dropped, added)
Length: paragraphs <draft> -> <now>; words (est.): shorter by over 5% | within 5% | longer by over 5%, because <cause>
Reasons: stated <a>, supplied <b>, open gaps <c>
Removed: <each, with why, or none>
Added, verify: <each addition and the draft sentence it rests on, or none>
Because check: <each new clause and its label, or none>
Variant check: <question> -> draft: <answer> from "<sentence>"; rebuild: <answer> from "<rebuilt sentence>"
Optional: <items; several per line; or omit>
Your bar: met | met except open gaps (<list>) | not met (<checks>)
Strogatz: proud (<the reader's last step, quoted>) | nearly (<the one fix>) | not yet (<why>)
Declined for your bar: <moves of his you dropped, or none>
```

- **Leave**: the note only, with the exact line "Already obeys; unchanged." in place of the lines from Outline to Variant check.
- **Review only** (asked to check, or not to rewrite): the note only, with the draft's place for the point; in place of the Outline, Length, Removed, Added and check lines, recommendations ranked by severity, each quoting the failing place, with its structural fix and a one-line example. Tag each recommendation "craft" or "bar"; "bar" only for a late point, a scene or aside before the point, or a held-back answer: it does not count against "Strogatz" and is repeated under "Declined".
- **No draft** (notes, or "explain X following the Strogatz Test"): write from the notes or what you know, opening with "Written from general knowledge; verify before use." In the note, "none" for the draft's place, the outline, Length and Removed.

## Never (most common or most costly first)

1. Reformatting in place of restructuring: headers, bullets, bold or tables only for list- or table-shaped content (independent items only).
2. An invented reason or purpose.
3. Lengthening.
4. The point moving later, or a new section above an early point.
5. Reasons left detached in a block at the end.
6. A closing line that adds a claim.

Rarer failures, evidence and help with unclear checks: `references/checks.md`.

## Verdicts: would Strogatz be proud?

The last three note lines describe this reply, with evidence quoted from the text, never your own prose style. "Your bar: met" needs no failing place left; "met except open gaps" means only open gaps remain: `[why: ?]` items and unmarked private terms. "Strogatz: proud" only with the reader's last step quoted and no strong check in `references/checks.md` failing; otherwise "nearly" or "not yet". Rate "Strogatz" on craft only: a late point, a scene or aside before the point and a held-back answer fail your bar, not his craft, so they never support "nearly" or "not yet". They go under "Declined", which names the moves of his you dropped or, in review mode, found and did not count against him, because the bar is stricter than Strogatz: he often states his central claim after word 150.

## Guards

- **Short material** (under about 120 words): check only R1, J1 and W1. A fix puts the answer first and adds a gloss or `[why: ?]`.
- **Out of scope** (code comments, docstrings, reference tables, API listings, changelogs, which are looked up rather than read through): reply with one line, without the rule's name, saying it does not fit and offering a short "how it works" lead-in, then the two-line note "Strogatz Test" and "Gate: out of scope".
- **Long documents** (over about 1,500 words): diagnose per section; rebuild the opening and the weakest sections one at a time, each against its original, never in one pass; then return the whole document.
- **A story that is the explanation** (an onboarding history, a case study): keep the story; check only that its point and reasons are stated.
- **Equations, derivations and code**: name the job before the tool, and wrap each equation in a lead-in and a read-back; more in `references/technical-mode.md` (from his technical writing for general readers; lower confidence).
- **Talks, slides or live chat**: open `references/delivery.md` (untested).
