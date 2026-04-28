# Daily Reflection Tree — DT Fellowship Assignment

A deterministic end-of-day reflection tool for employees. No LLM at runtime. No free text. Fully auditable paths.

---

## Repository Structure

```
/tree/
  reflection-tree.json     ← Part A: Full tree data (36 nodes)
  tree-diagram.md          ← Part A: Visual Mermaid diagram

/agent/
  index.html               ← Part B: Working web agent (open in any browser)

/transcripts/
  persona-1-transcript.md  ← Victor / Contribution / Altrocentric path
  persona-2-transcript.md  ← Victim / Entitlement / Self-centric path

write-up.md                ← Design rationale (2 pages)
README.md                  ← This file
```

---

## How to Read the Tree (Part A)

Open `tree/reflection-tree.json`. The tree is an array of node objects. Each node has:

| Field | Description |
|-------|-------------|
| `id` | Unique node identifier |
| `parentId` | Which node this descends from |
| `type` | `start` / `question` / `decision` / `reflection` / `bridge` / `summary` / `end` |
| `text` | What the employee sees. `{NodeId.answer}` = interpolated from earlier answer |
| `options` | For questions: fixed choices. For decisions: routing rules (`answer=X\|Y:TARGET`) |
| `target` | Where to jump after this node (overrides parent-child traversal) |
| `signal` | Axis tally tag: `axis1:internal`, `axis2:contribution`, `axis3:other`, etc. |

### Tracing a path manually

1. Start at node `id: "START"`
2. Auto-advance to the `target` node (`A1_OPEN`)
3. At question nodes, the employee selects one option
4. Find the next decision node (child with `type: "decision"`)
5. Read its `options` as routing rules: `answer=X|Y:TARGET_ID`
6. Match the selected answer → go to `TARGET_ID`
7. Apply `signal` at every node visited
8. Continue until `type: "end"`

### Decision rule format
```
"answer=Option A|Option B:TARGET_NODE_ID"
```
Multiple rules separated by `;`. First match wins.

### Signal accumulation
```
signal: "axis1:internal"  →  state.axis1.internal += 1
signal: "axis2:entitlement"  →  state.axis2.entitlement += 1
```
The summary node uses the dominant pole per axis to personalise the closing reflection.

---

## How to Run the Agent (Part B)

No installation. No dependencies. No server required.

```bash
# Option 1: Open directly in browser
open agent/index.html

# Option 2: Serve locally
python3 -m http.server 8080
# Then visit http://localhost:8080/agent/
```

The agent:
- Loads the tree data (embedded in HTML for portability)
- Renders each node with appropriate UI (question → buttons, reflection → read + continue, bridge → auto-advances)
- Routes deterministically based on selected options
- Accumulates axis signals
- Interpolates reflection text with the employee's earlier answers
- Produces a personalised summary with axis bars

**No API calls. No LLM. No randomness.**

---

## The Three Axes

| Axis | Spectrum | Psychology |
|------|----------|-----------|
| **Locus** | Victim ↔ Victor | Rotter (1954), Dweck (2006) |
| **Orientation** | Entitlement ↔ Contribution | Campbell et al. (2004), Organ (1988) |
| **Radius** | Self-centric ↔ Altrocentric | Maslow (1969), Batson (2011) |

---

## Node Count

| Type | Count |
|------|-------|
| start | 1 |
| question | 12 |
| decision | 9 |
| reflection | 10 |
| bridge | 2 |
| summary | 1 |
| end | 1 |
| **Total** | **36** |

Minimum requirements per assignment brief: 25+ nodes ✅, 8+ question nodes ✅, 4+ decision nodes ✅, 4+ reflection nodes ✅, 2+ bridge nodes ✅, all 3 axes ✅

---

## Hallucination Controls

This tool is inherently hallucination-free because:
1. **No LLM at runtime** — zero API calls during employee use
2. **Fixed options only** — no free text input, no classification
3. **Deterministic routing** — same answers always produce same path
4. **Template interpolation only** — reflection text uses `{nodeId.answer}` substitution, not generation
5. **Auditable** — every possible conversation path can be traced by reading the JSON

---

*Built for DT Fellowship Assignment · April 2026*
