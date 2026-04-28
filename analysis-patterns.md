# Analysis Patterns — Borderline Case Heuristics

> Read this file when confidence is borderline (0.4–0.65) or when you're unsure whether
> something is a genuine fallacy vs. valid-but-unusual reasoning.

---

## The Steelman Test

Before flagging any argument, ask:

> "Can I construct a version of this argument that is NOT fallacious and still makes
> the same core point?"

If yes → lower your confidence significantly. If the steelman version is clearly what
the author intended, do not flag. If the steelman requires significant reconstruction
of the argument, flag with a caveat and provide the steelman as your "charitable reading."

---

## High False-Positive Risk Fallacies

These fallacies are commonly misidentified. Apply extra scrutiny.

### Appeal to Authority — Common Misfires

**Valid appeals (do NOT flag):**
- Citing a domain expert on a question within their domain where expert consensus exists
- Citing institutional data (CDC, peer-reviewed meta-analyses, government statistics) with
  appropriate caveats
- Citing personal experience for claims *about that experience*

**Invalid appeals (flag):**
- Expert from domain A used to settle question in domain B
- Anecdotal testimony of a famous person used as data
- Consensus cited in a field where the consensus is the *very thing in dispute*
- "Studies show" with no citation + used to end discussion

---

### Slippery Slope — Common Misfires

**Valid slippery slope reasoning (do NOT flag):**
- Mechanism is explicitly described
- Historical precedent shows the chain has occurred before
- Empirical studies document the causal pathway
- The argument is about *risk* or *probability* (not inevitability), with evidence

**Fallacious (flag):**
- No mechanism given
- Each step in the chain treated as inevitable without justification
- The end state is wildly disproportionate to the first step
- Historical or empirical evidence contradicts the causal chain

---

### Ad Hominem — Common Misfires

**Valid (do NOT flag):**
- Questioning credibility when credibility is directly at issue (testimony, expert opinions)
- Noting conflicts of interest as *one factor among several* (not as the only reason)
- Pointing out that someone doesn't practice what they preach when the claim is about the
  speaker's own behavior

**Fallacious (flag):**
- Personal attack used as a *substitute* for addressing the argument
- Attack used to dismiss the argument entirely
- Irrelevant personal characteristics invoked (appearance, unrelated past behavior)

---

### Generalization — When to Hold Back

Generalizations are the engine of inductive reasoning. Flag only when:
- Sample size is stated or implied to be very small (1–5 cases) for a broad claim
- Selection bias is evident in how examples were gathered
- The conclusion uses absolute language ("always," "never," "all") without qualification
- Counter-examples are readily available and well-known

Do NOT flag:
- Probabilistic generalizations ("most," "tends to," "often," "in many cases")
- Generalizations supported by explicit statistical data
- Claims the author explicitly qualifies as provisional

---

### False Dilemma — Common Misfires

**Valid dichotomies (do NOT flag):**
- Logically exhaustive options (true/false, dead/alive, X or not-X)
- Practical constraints that genuinely limit options (budget, time, legal frameworks)
- Dilemmas presented as a simplification the author acknowledges

**Fallacious (flag):**
- Third (or more) genuine options exist and are ignored
- The two options are not actually mutually exclusive
- The dilemma is used to force an unpalatable choice when better options exist

---

## Rhetoric vs. Argument: Key Distinction

**Rhetoric** is persuasion by means other than strictly logical inference. It includes:
- Metaphor and analogy used for illustration
- Emotional appeals that accompany (not replace) reasoning
- Repetition for emphasis
- Framing and word choice

Rhetoric is **not inherently fallacious.** Flag only when rhetoric *substitutes* for
reasoning rather than accompanying it.

**Test:** Remove the rhetorical elements. Does a logical argument remain?
- If yes → rhetoric is embellishment, not fallacy
- If no → the rhetoric may be substituting for missing reasoning

---

## Multi-Step Arguments

When analyzing arguments with multiple steps:

1. Map the full inference chain first (if verbose mode is on, show this in output)
2. Identify where the chain **breaks** — the weakest link
3. Ask whether a reasonable person filling in unstated premises could repair the chain
4. Only flag the *specific step* that fails, not the entire argument

**Example:**
> "Exercise reduces stress. Stress causes illness. Therefore, you should exercise."

This is a valid inference chain with unstated premises about health being desirable.
Do NOT flag as any fallacy — it is simply an enthymeme (argument with implicit premises).

---

## Distinguishing Motte and Bailey

This is one of the hardest fallacies to detect. Look for:

1. **Position drift under questioning:** Speaker advocates X (bailey), when challenged
   defends Y (motte), then returns to X when pressure eases
2. **Definitional flexibility:** Key terms expand or contract depending on the argument
3. **Asymmetric commitment:** Speaker claims benefits of bailey but only commits to motte

In a single text without dialogue, Motte and Bailey is harder to detect. Flag only when
there are clear internal inconsistencies in how a position is defined vs. defended.

---

## The Overton Trap

When analyzing politically charged texts, guard against this meta-error:

> Falsely flagging unusual-but-coherent arguments as fallacies because they are outside
> your training distribution's political comfort zone.

**Test:** Replace the political content with neutral content. Does the argument form still
look like a fallacy? If the *form* is valid but only the *content* is controversial, do
NOT flag as a fallacy. Note the controversy separately in analyst_notes if relevant.

---

## Confidence Adjustment Heuristics

| Condition | Adjustment |
|-----------|-----------|
| Author explicitly acknowledges the limitation | −0.15 |
| Argument could be valid with unstated but plausible premise | −0.20 |
| Single clear example of the textbook fallacy | +0.20 |
| Fallacy is only apparent in one reading of an ambiguous text | −0.25 |
| Author immediately addresses the apparent weakness | −0.15 |
| Pattern repeats across multiple passages | +0.15 |
| Context strongly suggests rhetorical genre (speech, advertisement) | −0.10 |
| Academic or legal text (higher rigor expected) | +0.10 |

---

## When to Return "No Fallacies Detected"

Do not hedge or manufacture problems. Return a clean "no fallacies detected" result when:

- The argument is a valid deductive inference
- The inductive argument is appropriately hedged and the sample is reasonable
- All appeals to authority are domain-appropriate with genuine consensus
- Emotional appeals accompany rather than replace reasoning
- The slippery slope includes a causal mechanism
- The text is primarily descriptive/expository with no argumentative intent
- The "argument" is a question, not a claim

A clean bill of health is **useful and rigorous output**, not a failure to find anything.
