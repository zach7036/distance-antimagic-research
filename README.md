# Distance-Antimagic Research

**Canonical research repository** for Zach Waddle's work on universal distance-antimagic labelings, group-valued obstructions, nonlinear finite-field constructions, and exhaustive computation.

**Status:** research manuscripts and reproducibility materials; not yet peer reviewed.  
**Current release:** v1.1.0, August 2026.

## What is here

This project contains three connected but logically distinct research threads.

### 1. Universal distance-antimagic labelings

The main classification theorem says that for a graph `G` of order `n`, the following are equivalent:

- every bijection `V(G) -> Z_n` is distance antimagic;
- every bijection into every abelian group of order `n` is distance antimagic;
- every two open neighborhoods differ by one deletion and one insertion;
- `G` is `K_n`, or `n` is even and `G` is a perfect matching.

The same work develops an exact signed-subset-sum theorem for ordinary labels `1,...,n`, yielding a complete cancellation/range/parity test for whether a fixed vertex pair is separated under **every** integer labeling.

Further consequences include Johnson-graph set-system rigidity, cluster-graph and forest classifications, connected universal-integer families, complementary-neighborhood obstructions, phantom periods in Cayley graphs, and a complete elementary-abelian-2 switching classification.

See [`papers/universal-distance-antimagic/`](papers/universal-distance-antimagic/).

### 2. Nonlinear finite-field constructions

For Cayley graphs on the additive group of a finite field, the neighborhood-sum operator

`T_S f(x) = sum_{s in S} f(x+s)`

is treated as a finite-field translation filter. Paired affine lines collapse the nonlinear permutation monomial `x^(2p-1)` to a sparse linearized weight polynomial.

The resulting constructions give nonlinear group-distance-antimagic labelings even when every additive automorphism labeling is distance magic. The project includes dimension-three, even-dimensional, and odd-dimensional infinite families, together with explicit finite-field certificates and a dimension-two obstruction for the full-line architecture.

See [`papers/nonlinear-finite-field/`](papers/nonlinear-finite-field/).

### 3. Exhaustive verification through order nine

Every simple graph on at most nine vertices with pairwise distinct open neighborhoods is distance antimagic. At order nine, all 274,668 unlabeled graph classes were classified; all 205,914 eligible classes received explicit independently verified labeling certificates.

The large certificate archive, constructor, independent verifiers, catalogue provenance, and deterministic reproduction workflow remain in the dedicated computational repository:

**https://github.com/zach7036/distance-antimagic-order9**

See [`papers/order-nine/`](papers/order-nine/) for the research-suite summary.

## Repository guide

```text
papers/
  universal-distance-antimagic/
  nonlinear-finite-field/
  order-nine/
STATUS.md
THEOREM_LEDGER.md
OPEN_PROBLEMS.md
AI_ASSISTANCE.md
LITERATURE_NOTES.md
CITATION.cff
RELEASE_NOTES.md
```

## Scope

This repository does **not** claim a solution of the Kamatchi-Arumugam conjecture in general. The order-nine computation advances its finite frontier; the universal-labeling results concern the much stronger all-labelings quantifier; the finite-field work concerns group-valued Cayley labelings.

The fixed-noncyclic-group pair classification is complete for elementary abelian 2-groups but remains open in full generality for groups of exponent greater than two.

## Verification philosophy

Computations are used as regression tests, finite certificates, and falsification tools, not as hidden substitutes for proofs. The project records corrected false starts and narrowed claims explicitly. Where an external theorem is load-bearing, the mathematical literature—not AI output—is the cited source.

No GitHub Actions workflows are used for this research repository.

## AI and computational assistance

Large language models, computer algebra, exhaustive enumeration, SAT/search experiments, and exact verification programs were used during exploration, error detection, proof auditing, and drafting. No AI system is an author. The human author is responsible for all released claims and submissions.

## Citation

See [`CITATION.cff`](CITATION.cff). Priority and novelty remain provisional pending specialist and database-level review.
