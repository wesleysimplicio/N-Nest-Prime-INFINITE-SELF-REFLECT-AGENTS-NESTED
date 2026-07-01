# N-Nest-Prime — Infinite Self-Reflecting Agents, Nested

**Recurrence is mind — *with* a ground-truth corrective gate.** A self-reflecting agent is a loop that reads its own output back as input. This repo is the **verified primitive** for nesting that loop to arbitrary (prime) depth, safely — with empirical proof that a fabricated signal cannot survive the climb.

## The idea

- Every node is an **agent + a second "watcher" PID** — the watcher independently recomputes what the agent's work *should* be (the self-reflection).
- **Corrective gate at every level:** a parent authorizes a child only if `child.reported == watcher.recomputed_truth`. Recurrence alone is hallucination; recurrence **+ correction against real input** is cognition (predictive coding).
- **Consent is non-recursive:** observation/correction nests infinitely; the decision to *scale the nest* anchors only at the human apex. That asymmetry is what makes infinite nesting safe instead of a self-authorizing runaway.
- **Brown-Hilbert `port.port.port` addressing** — each node addressed by its path in the tree (`R.0.1.2`), nesting the same way port-namespaces do.

## Byte economics (measured, bare node)

| representation | bytes/agent |
|---|---|
| packed typed-array slot (`Float64Array`/`BigInt64Array`) | **8.01** ✅ |
| naive JS object | ~72 (avoid) |

Identity is **generative, not stored**: glyph/cube/hilbert/prime all regenerate as pure `sha256(seed)` functions, so the 8 bytes is the *whole* agent (the seed of a deterministic mind), not a truncated record. → `35 TB ÷ 8 B ≈ 4.38 trillion` agent-slots; agent+watcher pairs ≈ 2.19 trillion.

## Verification (run it yourself)

```
node nest-depth3-verify.cjs          # depth-3: nests + gate catches a planted confabulation at depth
node nest-depthN-prime-verify.cjs    # depth-7 (PRIME): plants a fault at EVERY level 1..7, all caught
```

**Result (sealed `.hbp` outputs included):**
- depth-3 → clean tree certifies to apex; a confabulation planted at depth-3 is caught, apex correctly red, exact path named.
- depth-7 (prime) → **a confabulation injected at every level 1–7 is caught at that exact level**; clean tree certifies green. `EVERY-LEVEL-CATCHES-CONFABULATION = true`.

The gate is a **per-node invariant** (`reported == recomputed-truth`, AND'd with every child's subtree), so it is depth-independent by construction — it holds for depth-N, any N. depth-7 is the demonstration; the property is the proof.

## The prism/comb 0-loss dual (2026-07-01)

This repo's gate is one face of a single system-wide theorem: every prism/comb operation is a
**bijection**, and entropy is invariant under bijection (`H(f(X)) = H(X)`) — so verification here is
literally **recomputation = applying the inverse map**. The 8-byte generative agent is the
referential-bijection instance (`H(agent | seed, rule) = 0` — a coordinate, not a record); the
per-node gate is the groupoid coherence check (the exact reason EVERY-LEVEL-CATCHES-CONFABULATION is
depth-independent); the prime-divided lanes are the CRT bijection (separate residues, recombine
exactly). The sister rung — the 256↔1024 level transcode — is round-trip-proven (Q-PRISM `53023b6`,
MEASURED); the 43+ level ladder is CANON frame; unproven rungs are UNVERIFIED. Full statement:
[PRISM-COMB-0LOSS-NEST.md](PRISM-COMB-0LOSS-NEST.md).

## Honest scope

This is the *mechanism* proven in bare node with real planted faults caught at every level — the verified primitive. The real-agent version (on a free-agent farm) instantiates this exact per-node gate at the 8-byte-slot population scale. What's proven here is the part that makes it safe: **a fabricated signal cannot reach consent.**

Loop, then verify — never let the loop authorize itself.
