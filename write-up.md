# Write-Up: Design Rationale for the Daily Reflection Tree

## Why These Questions

The hardest constraint in this assignment is also the most important one: **no free text**. Every question must offer fixed options that genuinely capture a psychological spectrum — not a survey with a "right answer" baked in.

This forced a discipline: before writing any option, I asked — *would a real person, tired at 7pm, recognise themselves in this?* Options that are too obviously "good" get clicked without thought. Options that feel slightly uncomfortable are the ones that trigger honest reflection.

### Axis 1 — Locus of Control

The opening question ("weather report") is deliberately indirect. Asking "did you feel in control today?" primes defensiveness. Asking for a weather metaphor invites honest description. A person who says "Stormy" is already doing the psychological work of Axis 1 — they've named their experience without being asked to evaluate it.

The follow-up branching then asks the harder question differently depending on which entry point the employee came from. Someone who said "Sunny" is asked *why* — which reveals whether they attribute success internally or externally. Someone who said "Stormy" is asked *what they did* — which surfaces whether they moved or waited.

The final question on this axis ("was there a choice available, even a small one?") is the most important node in the tree. It operationalises Rotter's internal locus construct: the belief that one's actions are connected to outcomes. The options are honest — "Not really — the situation was out of my hands" is a valid answer. The reflection that follows doesn't argue with it; it simply names what happened.

### Axis 2 — Contribution vs Entitlement

Campbell's entitlement research (2004) showed that entitled employees rarely self-identify as entitled. The construct is invisible from the inside. This means the questions cannot ask "do you feel entitled?" — they must surface the *behaviour pattern* instead.

The design choice was to split the axis on entry: employees who describe themselves as "mostly giving" enter through a contribution pathway that tests the *depth* of their giving (did it cost them anything?). Employees who describe themselves as "mostly receiving" enter through an entitlement pathway that tests whether recognition-seeking is present.

The motive question ("what was underneath that effort?") is the axis's most psychologically interesting node. Organisational Citizenship Behaviour (Organ, 1988) is discretionary — but the *motive* for discretionary effort matters enormously. "I hoped it would be noticed" is not contribution; it is contribution in the form of entitlement. The question surfaces this without naming it.

### Axis 3 — Self-Centrism vs Altrocentrism

Maslow's 1969 paper introduced self-transcendence as a developmental stage beyond self-actualisation — the orientation toward something larger than oneself. Batson's perspective-taking research (2011) showed that cognitive empathy (understanding another's position) is distinct from affective empathy (feeling their feeling), and that the former is more reliably generative.

The axis opens with a question designed to surface the *natural* frame of the employee — not what they think they should say, but what actually came to mind first. "Mine — it was mine to carry" is an honest answer for many days, and the tree does not penalise it. It simply follows that path into a gentle expansion: "did anyone else's experience cross your mind at any point?"

The four entry branches (self / team / specific colleague / end user) create four meaningfully different conversation paths — each with a different radius, each with a reflection that meets the employee where they are.

---

## How I Designed the Branching

The key structural decision was to make the tree **converge across axes but diverge within them**. Within each axis, the tree branches based on the employee's honest self-location. Across axes, all paths flow into the next axis's bridge node. This ensures:

1. No employee gets "stuck" in a judgment loop
2. Every employee, regardless of where they land on Axis 1, reaches Axis 2 with the same gentle transition
3. The summary node can reference all three axes regardless of path

**Trade-offs I made:**

- I chose 3–4 options per question rather than 5. Five options overwhelms tired employees. Three risks false dichotomy. Four allows a genuine spectrum while keeping the cognitive load manageable.
- I chose to *not* route on axis signals within an axis (e.g., "if you have 2 internal signals, skip to X"). This would create shortcuts that bypass the conversation's depth. Every employee answers at least 3 questions per axis.
- The decision nodes are invisible to the employee. This was a deliberate choice to keep the experience feeling like a conversation, not a branching quiz.

---

## Psychological Sources

| Framework | Author(s) | Year | How it shaped the design |
|-----------|-----------|------|--------------------------|
| Locus of Control | Julian Rotter | 1954 | Internal vs external attribution; branching on agency language |
| Mindset | Carol Dweck | 2006 | Growth vs fixed orientation; surfaced through "what made it happen" framing |
| Psychological Entitlement | Campbell et al. | 2004 | Invisible from the inside; requires behavioural (not attitudinal) questions |
| Organisational Citizenship Behaviour | Dennis Organ | 1988 | Discretionary effort as the signal for contribution orientation |
| Self-Transcendence | Abraham Maslow | 1969 | The largest radius — from "what do I need" to "what is needed of me" |
| Perspective-Taking | Daniel Batson | 2011 | Cognitive empathy as a navigable behaviour, not a feeling |

---

## What I Would Improve With More Time

1. **Longitudinal state.** The tree currently treats each session as independent. With persistent state, the summary could reference yesterday's axis scores: *"Yesterday you were external on agency. Today you're internal. What changed?"* This is where the tool becomes a practice, not a survey.

2. **More question nodes per axis.** The current tree meets the minimum (2+ per axis) but a richer version would have 5–6 questions per axis with more granular branching. Each question would peel another layer.

3. **Interpolation depth in reflections.** Currently reflections interpolate the opening answer (`{A1_OPEN.answer}`). A richer version would interpolate across axes: *"You said you felt '{A1_OPEN.answer}' — but you also helped someone outside your scope. That's more agency than the weather suggested."*

4. **Branch for mixed signals.** An employee who scores 2 internal and 2 external on Axis 1 currently gets the same reflection as one who scores 4 internal. A tie-breaking node would allow the tree to acknowledge genuine ambivalence rather than forcing a dominant read.

5. **Exit interview node.** The current END node is clean but brief. A richer closing would ask the employee to name one concrete intention for tomorrow — not as a commitment device, but as a closing ritual that consolidates the reflection into action.
