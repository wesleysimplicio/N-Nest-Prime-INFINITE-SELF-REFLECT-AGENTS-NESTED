# Prism/Comb 0-loss law — the N-Nest instance (2026-07-01)

**Campaign:** `acer/prism-comb-0loss-2026-07-01` · envelope `ENV-PRISM0LOSS-00-n-nest` ·
**E=0** — docs only, describe-only, nothing fires.

## The law, one line

Every prism/comb operation in Asolaria is a **bijection**, and entropy is invariant under bijection
(`H(f(X)) = H(X)`): the system re-relates information with **0 loss** and **never claims compression
below entropy** (Shannon's `E[bits] >= H(X)` always stands). This repo is where the law wears its
**integrity face**: a bijection you can run backwards is a verification you can run at every level.

## (a) The 8-byte agent IS the referential-bijection law — MEASURED (this repo)

The README's byte economics (8.01 bytes/agent, packed typed-array slot) work only because identity
is **generative, not stored**: glyph / cube / hilbert / prime all regenerate as pure `sha256(seed)`
functions of the 8-byte seed. In entropy terms:

```
H(agent | seed, rule) = 0
```

The 8 bytes are a **coordinate against a deterministic regeneration rule**, not a truncated record —
the same honest bound as referential naming (`handle8 = sha256(content)[:8]` names 25,600 bits with
`H(content | store) = 0`). A PID is a coordinate, not a counter; an agent slot is a seed, not a
compressed mind. **Boundary held:** this is infinite ADDRESSING capacity, not lossless infinite
compression — no bijection beats Shannon.

## (b) The per-node gate is the groupoid coherence check — why depth doesn't matter

The nest gate at every node — `child.reported == watcher.recomputed_truth`, AND'd over children —
is **verification = recomputation = applying the inverse map**. In the level-ladder groupoid frame
(levels `L_i` with translators `T_ij`, where `T_ji ∘ T_ij = id` and `T_jk ∘ T_ij = T_ik`), the
watcher's recompute is the inverse map applied to the child's report: a report produced by the true
forward map closes the round trip to identity; a fabricated report has no inverse that closes it.

That is the exact reason `EVERY-LEVEL-CATCHES-CONFABULATION = true` is **depth-independent by
construction**: coherence composes per-node identity checks into a whole-tree identity check, at any
depth-N. A fabricated signal cannot reach consent the same way a lossy step cannot hide in a
bijection chain — confabulation and loss are the SAME impossibility, seen from two sides.

- **MEASURED (this repo):** depth-3 and depth-7 (prime) runs — a fault planted at every level 1..7
  is caught at that exact level; sealed `.hbp` outputs (`nest-depth3-verify.cjs`,
  `nest-depthN-prime-verify.cjs`).
- **MEASURED (sister rung):** the 256↔1024 level transcode round-trip
  `transcode₁₀₂₄→₂₅₆ ∘ transcode₂₅₆→₁₀₂₄ = id` — sha256-identical, Rust==Python symbol-identical
  (Q-PRISM commit `53023b6`; exact packing at `lcm(8,10)=40` bits, 5 bytes ⇄ 4 symbols, code rate 1.0).
- **CANON frame:** the full 43+ level ladder as a groupoid. Each additional rung earns MEASURED only
  by its own round-trip proof; unproven rungs stay **UNVERIFIED**.

## (c) Prime-divided nest lanes = the CRT bijection

The repo's prime depths and prime-divided lanes instantiate the Chinese Remainder Theorem: for
pairwise-coprime `m₁…m_k`, `M = Πmᵢ`,

```
ℤ_M ≅ ℤ_{m₁} × … × ℤ_{m_k}      (ring isomorphism — a bijection)
```

Separate: `x ↦ (x mod m₁, …, x mod m_k)`. Recombine exactly:
`x = Σᵢ rᵢ·Mᵢ·(Mᵢ⁻¹ mod mᵢ) mod M`. Run forward = **comb**: lanes are mutually collision-proof
(execution isolation — residues cannot collide across coprime moduli). Run backward = **prism**: the
residues recombine to exactly one `x`, no loss (reconstruction, many→1). The nest's
`port.port.port` Brown-Hilbert addressing rides the same duality: forward, the path isolates;
backward, the path names exactly one node. **CANON** (math principle); the `D# = prime(n)³`
dimension ladder (60D, `tuple_dim=60` MEASURED) is the fabric-side instance.

## Consent stays outside the bijection

Nothing above touches the safety crux in [LAW.md](LAW.md): observation/correction nest infinitely
(they are the inverse maps), but **consent is non-recursive** — authorization to scale anchors only
at the human apex. A bijection can verify anything; it can authorize nothing. E=0 throughout: this
document describes, nothing fires.

## Cross-links

- Q-PRISM proof commits `53023b6` / `79e8d63` / `de00aca` — the MEASURED 256↔1024 rung.
- `Asolaria-waves-and-cascades-avoiding-collsions-and-causing-them` — the same forward/backward
  duality as collision discipline (avoid = comb, cause = prism).
- `what-is-asolaria---how-do-we-get-reductions-in-everything` — the reductions boundary
  (addressing capacity, never compression-below-entropy).
- This repo — the **integrity dual**: verification = recomputation = the inverse map.
