# Rebuild patterns

Open this file for material other than a system or design description (whose arc is in `SKILL.md`, step 3), or when the arc does not obviously fit. It gives the arc's evidence, the moves that change structure, the arc for each kind of material, and one short before-and-after. The example shows moves, not phrasing: never reuse its sentences.

## The arc, and how far to trust each step

| Step | What goes there | Ledger ID | Tier; confidence |
|---|---|---|---|
| 1 | The point and the reason, inside the runway (about 100 words, hard maximum 150) | A1 | P, U, A; high that he poses the question early, low for the answer by word 100 |
| 2 | The smallest concrete case that shows the thing, carrying much of the piece | A2 | P, L; high for a small case, low for its share of the piece |
| 3 | Names and notation, as nicknames for what the case already showed, each glossed | A3 | P, U; moderate |
| 4 | The hard step by picture, trace or trick, with skips named and the reason given | A4 | P; moderate |
| 5 | The general statement, now | A5 | P, I; low (no report states it as a step) |
| 6 | The payoff: return to the opening question and state the intuition | A6 | P, L, U; high for the return, unmeasured for "intuition" |
| 7 | What it unlocks, its limits, or an open question; no repeating recap | A7 | P, I; moderate (the harm of recaps is folk wisdom) |

In `SKILL.md` steps 6 and 7 merge into one close that restates only what the body says; a limit or an open question belongs there only if the draft states it, because closing lines that added claims were a measured failure (development round 1). The arc is observed practice, not a law Strogatz states. His one stated ordering rule is negative: do not go assumptions, theorems, proofs, stop. Treat steps 1, 2 and 6 as firm and the rest as defaults, with one exception: in step 1, the answer by about word 100 is the author's calibration (tier A, low confidence), not his practice.

## Moves that change structure

Each move changes where something sits, which is what separates a rebuild from an edit.

1. **Lift the point.** The answer often sits in a closing "In short" or a sentence buried in the middle. Move it to the opening, with its reason, and delete the closing recap it came from.
2. **Dissolve the "why" block.** Reasons gathered under a "Why" or "Rationale" heading belong beside the steps they justify. Move each one there; the block disappears.
3. **Thread the case; do not copy it.** Bring the draft's worked case forward and let each rule enter at the moment the case needs it. The case is told once. Later sections point back to it ("in the case above, ..."), because telling it twice lengthens the text and teaches nothing new.
4. **Show, then name.** Where a term arrives before the thing it names, show the thing in the case first and then give the name.
5. **Turn dependent bullets into sentences.** Steps that depend on each other need "because", "so" and "but", which bullets drop. Keep a list or table only for independent items, such as a set of thresholds.
6. **Mark gaps; do not fill them.** A rule, exception, override or special case (never a bare value, and for an expert reader never a standard-practice rule) with no reason in the draft ends its sentence with `[why: ?]`. A reason derived from the draft's own statements by arithmetic or logic ends its sentence with `[added: verify]`. A purpose is never derived, however it is worded. A bare value (a floor, cap, limit, window, count, timeout, cutoff, delay or schedule constant) never gets a marker: it goes in one "Optional" line of the note. Markers carry no label and no text inside them.
7. **Delete only explanatory material.** Asides, history, analogies, restated points and hedges go if nothing later needs them. Constraints, warnings, numbers, preconditions, limits, edge cases and mechanism clauses stay, or are listed under "Removed".

## The arc by kind of material

**A system or design description** (how something decides or works; most design documents and READMEs). The point is what the system decides and its central mechanism, in up to three consecutive sentences, then why it exists. Next, one input traced through every step, each rule entering as the case needs it, with its reason beside it. Then the general rule set, compactly; a table is fine for thresholds. Special cases come after, each with its reason or `[why: ?]`; an unexplained bare number goes in an "Optional" line instead. Close by restating the point, with no new claim: if you cannot quote the sentence a closing line rests on, leave it out.

**A concept explanation or a lesson.** For an unmotivated newcomer, open with the question in a form they recognize, in a line or two, and answer it by a quarter of the piece. Then the smallest case they can work in their head, the name for what they just saw, the hard step by picture or trace, the general statement, and the payoff that answers the opening question. One sentence on where else the idea turns up is optional. For an informed reader, state the answer first and keep the rest of the order.

**A data-science write-up.** The finding and its size first, with the decision it bears on. Then the one comparison or plot that shows it. Method choices follow, each with its reason (why this baseline, why this window). Caveats once, where they apply. Close on what the finding changes, or the next question.

**A decision record, or the explanatory part of a pull request.** The decision and its reason first. Then the case or incident that forced it, traced. Then the options rejected, each with its reason, and the consequences and limits. Lists of changed files and test logs are reference material: leave them as they are.

**A chat answer that fell flat.** Usually short. The answer in the first sentence, one small case, the reason, and stop. Under about 120 words, apply only the short-material guard.

**A long document** (over about 1,500 words). Outline one row per section, diagnose each section, then rebuild the opening and the weakest sections one at a time, each against its original, checking retention per section. Never rewrite the whole in one pass.

**A story that is the explanation** (an onboarding history, a case study). Keep the story and its order. Check that the point is stated inside the runway, often in a line before the story starts, and that each turn of the story carries its reason.

## One before-and-after

An invented system, written for this file. Reader: a new member of a museum's visitor-services team. The After illustrates the moves; it is not a template. Do not clone its sentence frames onto another draft, because every draft needs its own point, case and order.

**Before** (161 words, counted by script with hyphenated words split; 156 by whitespace):

> Great question! Here is how Pellam Museum handles timed-entry tickets.
>
> **Slots**
>
> - Entry runs in 15-minute slots of 40 visitors.
> - For each slot, 32 tickets go on sale online seven days ahead.
> - The other 8 are held at the front desk for walk-up visitors.
>
> **Release**
>
> - 30 minutes before a slot starts, any held tickets still unsold are released online.
> - No slot ever admits more than 40 people.
>
> **Rationale**
>
> - Holding tickets back: visitors who arrive without booking, often tourists, would otherwise be turned away on busy days.
> - The cap of 40: the first gallery is a narrow corridor that holds about 40 people comfortably.
>
> **Example**
>
> The 11:00 slot sells all 32 online tickets by Tuesday. On the day, 5 walk-ups buy held tickets before 10:30, so the remaining 3 go online at 10:30.
>
> In short, Pellam keeps a few tickets for walk-ups until half an hour before each slot, then sells whatever is left online. Hope this helps!

The diagnosis lists the steps in draft order, each with the reason the draft states: 1 slot size (none), 2 online sale (none), 3 desk hold ("would otherwise be turned away"), 4 release (none), 5 cap ("a narrow corridor"), then 6 and 7, the two reasons in their separate block, 8 example, 9 summary, 10 boilerplate. The gate finds two blockers:

- R1: only the closing summary, at word 136 of 161 (132 of 156 by whitespace), says how holding and release work.
- W1: the release rule has no stated purpose, and the two stated reasons sit apart from their steps.

So the draft is rebuilt. Three things are not blockers:

- The bullets and bold labels carrying a sequence fail F1, a strong check.
- The boilerplate is deleted in the rebuild anyway.
- The 15-minute length, the seven-day lead, the 30-minute timing and the choice of 8 are bare values, so they share one "Optional" line and get no `[why: ?]`. The release itself, by contrast, is a rule that changes what happens, so it needs a reason or the marker.

**After** (137 words by the same script; 133 by whitespace):

> Pellam Museum holds back 8 of the 40 tickets in each timed-entry slot for visitors who walk up without booking, and releases any still unsold online 30 minutes before the slot starts [why: ?]. It holds them back because walk-ups, often tourists, would otherwise be turned away on busy days.
>
> At 11:00, for instance, all 32 online tickets, on sale seven days ahead, are sold by Tuesday while 8 wait at the front desk. On the day, 5 walk-ups buy held tickets before 10:30, and at 10:30 the remaining 3 go online.
>
> Slots last 15 minutes. None admits more than 40, because the first gallery is a narrow corridor that holds about 40 people comfortably. Walk-ups have first claim on 8 places until half an hour before entry; the online queue gets what they leave.

The note:

```
Strogatz Test
Reader assumed: a new visitor-services team member  (guess); glosses resting on it: none
Gate: R1, W1 -> rebuild
Point (draft: later; now: first paragraph): "Pellam Museum holds back 8 of the 40 tickets in each timed-entry slot for visitors who walk up without booking, and releases any still unsold online 30 minutes before the slot starts."
Outline before -> after
  summary (row 9) -> opening, merged with the release (row 4) and the reason for holding (row 6)
  example (row 8) -> second, carrying the online sale and the desk hold (rows 2, 3)
  slot size, cap and the cap's reason (rows 1, 5, 7) -> merged, then the close
  boilerplate (row 10) -> dropped
  moved 3, merged 6, dropped 1, added 0
Length: paragraphs 6 -> 3; words (est.): shorter by over 5%
Reasons: stated 2, supplied 0, open gaps 1
Removed: "Great question!", "Here is how Pellam Museum handles timed-entry tickets." and "Hope this helps!", because they are boilerplate
Added, verify: none
Because check: none new (both "because" clauses only restate links the draft states)
Variant check: if 8 walk-ups buy held tickets before 10:30, what goes online at 10:30? -> draft: nothing, from "30 minutes before a slot starts, any held tickets still unsold are released online"; rebuild: nothing, from "Pellam Museum holds back 8 of the 40 tickets ... and releases any still unsold online 30 minutes before the slot starts"
Optional: no reason is given for 15-minute slots; for the seven-day lead; for releasing 30 minutes before the slot; or for holding 8 rather than another number
Your bar: met except open gaps (why unsold held tickets are released)
Strogatz: nearly (state why unsold held tickets are released online)
Declined for your bar: none
```

The note places the point and judges length in coarse terms, because an agent cannot count words reliably; the word counts in the headings above come from a script.

What the example shows:

- The point moved from the closing summary to word 1, and the summary's recap went with it.
- Each stated reason now sits beside its step, and the separate "Rationale" block is gone. Both "because" clauses restate links the draft states.
- The rule with no stated purpose (the release) ends its sentence with `[why: ?]`, with nothing inside the marker. The bare numbers (15 minutes, seven days, 8) share one "Optional" line instead.
- The case is told once, early, with the draft's numbers unchanged. The close restates the point sentence and adds no claim.
- The variant check computes an untraced case from the text's own rule.
- No headers or bullets were added, and the text got shorter.
- The verdict lines describe this reply: only one open gap remains, so "Your bar" is "met except open gaps", and the one fix named is that gap, the release's purpose.
