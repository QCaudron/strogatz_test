# Technical mode: equations, derivations, systems and code

Every rule in this file is **from his technical writing for general readers; lower confidence**. The research could not read his textbook prose or any lecture transcript. The rules rest on three technical pieces he wrote for lay readers who want the algebra, on his textbook's table of contents, and on lecture descriptions. Use them as defaults, and let the blockers in `SKILL.md` decide.

The aim does not change in technical mode: make the reader care about the question before answering it. What changes is the form of that care. Ledger IDs TM1 to TM7 hold the sources. Their tiers are P, or P and I, except TM2, which is U and P; all seven are low confidence.

## The rules

### TM1 Name the job before the tool

*From his technical writing for general readers; lower confidence.*

- **Rule:** before a technique, formula or function appears, say what job it does for the reader, because a tool met before its job is a tool with no reason (W1).
- **Signature:** a section that opens with a definition ("Let ρ = λ/μ"); a function introduced by its signature.
- **Fix:** one sentence of job first. "To tell whether a queue will ever drain, compare how fast work arrives with how fast it is served. That ratio is called the utilization, ρ = λ/μ."
- **Evidence:** TM1. Lecture descriptions name tools by their jobs ("techniques for ruling out closed orbits"); two instances in his prose. Tier P, I; low.

### TM2 State the destination early, unless suspense can be earned

*From his technical writing for general readers; lower confidence.*

- **Rule:** show the result, or where the derivation is going, near the start, and make the route the subject. Hold it back only if the reader can try to predict it, and then give them a beat to try.
- **Signature:** a derivation whose target appears only in its last line, with nothing for the reader to predict on the way.
- **Fix:** state the target first ("we will show that the wait grows without bound as ρ approaches 1"), then derive it.
- **Evidence:** TM2. One technical piece shows its target in paragraph 2; another withholds it, so the rule is conditional. Mostly the user's bar plus a reconciliation from the research. Tier U, P; low.

### TM3 Wrap each equation in a lead-in and a read-back

*From his technical writing for general readers; lower confidence.*

- **Rule:** before a displayed equation, one sentence on what the step is for; after it, one sentence on what it says in words.
- **Signature:** equations stacked with no sentence between them; a result left for the reader to interpret.
- **Fix:** "We want the time the reading takes to settle within 10%, so solve for t: t = τ ln 10 ≈ 2.3τ. In words: wait a little over two time constants."
- **Evidence:** TM3. Three raw pieces do this. One of the better supported technical rows. Tier P; low.

### TM4 Let a picture, trace or table answer the qualitative question first

*From his technical writing for general readers; lower confidence.*

- **Rule:** the picture, a short trace or a small table says what happens (grows, settles, oscillates); the formula then says how much.
- **Signature:** a formula is the reader's first contact with the behavior.
- **Fix:** three rows of numbers, or one sentence tracing the case, before the formula. A table is fine when the content is table-shaped.
- **Evidence:** TM4. Structure, not prose: a lecture promising that pictures beat formulas for nonlinear systems, and a contents page with the geometric chapter first. No instance of a table was seen in his text; the table is the research's suggestion. Tier P, I; low.

### TM5 Check a result before asking the reader to trust it

*From his technical writing for general readers; lower confidence.*

- **Rule:** after a result, run one check the reader can follow: a limit case, multiplying back, or a small example.
- **Signature:** a final formula with no check, which the reader must take on trust.
- **Fix:** "If nothing arrives (λ = 0), the formula gives a wait of zero, as it should."
- **Evidence:** TM5. Two instances (a series multiplied by itself to confirm it; numbers before analysis in the textbook's order). No limit case was seen in his text. Tier P, I; low.

### TM6 Let one method run through the piece

*From his technical writing for general readers; lower confidence.*

- **Rule:** when several results use the same move, name the move once and reuse it, so the reader sees the next hard step coming.
- **Signature:** each section introduces a fresh technique for what is the same move.
- **Fix:** name the shared move at its first use and point back to it each time it recurs.
- **Evidence:** TM6. Read off his book's organizing principle and his textbook's recurring methods; frequency not measured. Tier P, I; low.

### TM7 Flag every skipped step, with the reason

*From his technical writing for general readers; lower confidence.*

- **Rule:** when you skip a step, say so and say why ("the second half repeats this argument, so it is left out").
- **Signature:** "it can be shown that", "clearly", or a jump the reader cannot check.
- **Fix:** name the skip and its reason, or insert the step from the draft's own material. Never invent the missing mechanism.
- **Evidence:** TM7, S1. The best supported of the seven: his pieces say what is skipped and why. "Every" is stricter than his practice. Tier P; low.

## Applying it by reader

- **Practitioners and experts:** keep TM1, TM3, TM5 and TM7. Drop glosses of notation they use daily. State the destination (TM2) at once; the route is the subject.
- **Informed outsiders:** all seven. Introduce each symbol after the thing it stands for (C2), and keep symbols few enough to be read aloud: his stated tactic is to avoid symbols that readers cannot sound out in their heads (tier S).
- **Newcomers:** prefer the picture or table (TM4) and the smallest numbers; display few equations.

## Code and systems

These follow from TM1 and TM4; the code-specific forms are inferred (tier I).

- Say what a function or component is for before its signature or interface.
- Trace one call or one request with concrete values before stating the general contract.
- A configuration table or API listing is reference material, out of scope for the rule; offer a short "how it works" lead-in instead.

## Limits

- Textbook and lecture phrasing were not read, so these rules describe what he teaches in what order more than how he phrases it.
- Some of his technical pieces show the equation before the picture, so "picture first" is a tendency.
- A 1993 research article he co-wrote is formal and jargon-heavy, so not all of his technical writing follows these moves.
