# Distance-Antimagic Research

Research on distance-antimagic graph labelings: universal-labeling structure, group-valued and finite-field constructions, and exhaustive verification through nine vertices.

> [!IMPORTANT]
> This is unrefereed research. The order-nine result has a public computational reproduction package. The broader universal-labeling and finite-field results are author claims whose full manuscripts and verification artifacts are not yet committed here; treat them as theorem candidates until those materials are available and independently reviewed.

## The problem

Let $G=(V,E)$ be a finite simple graph with $|V|=n$. A bijection

$$
f:V\to\{1,2,\ldots,n\}
$$

is **distance antimagic** when the open-neighborhood sums

$$
w_f(v)=\sum_{u\in N_G(v)} f(u)
$$

are pairwise distinct. Equal open neighborhoods are an immediate obstruction. Kamatchi and Arumugam conjectured that this is the only obstruction: every graph with pairwise-distinct open neighborhoods should admit a distance-antimagic labeling.

## Results at a glance

| Research track | Main result described by the project | Public evidence | Current status |
|---|---|---|---|
| Universal labelings | A graph is distance antimagic under **every** labeling into $\mathbb Z_n$—equivalently, into every abelian group of order $n$—exactly when it is $K_n$ or an even-order perfect matching | Summary and theorem ledger in this repository | Full manuscript not yet public here; unrefereed theorem candidate |
| Nonlinear finite-field constructions | Infinite families of nonlinear group-distance-antimagic labelings on finite-field Cayley graphs, plus a dimension-two obstruction for the full-line construction | Summary in this repository | Full manuscript, certificates, and verification code not yet public here; unrefereed theorem candidate |
| Exhaustive classification through order 9 | A simple graph on at most nine vertices is distance antimagic iff its open neighborhoods are pairwise distinct | [Dedicated code, manuscript, checksums, and deterministic replay](https://github.com/zach7036/distance-antimagic-order9) | Finite computer-assisted result; independently replayable, not peer reviewed |

The three tracks are related, but none is a proof of the general Kamatchi-Arumugam conjecture.

## 1. Universal-labeling structure

The project states that the following are equivalent for a graph $G$ of order $n$:

1. every bijection $V(G)\to\mathbb Z_n$ is distance antimagic;
2. every bijection from $V(G)$ into every abelian group of order $n$ is distance antimagic;
3. every two open neighborhoods differ by one deletion and one insertion;
4. $G\cong K_n$, or $n$ is even and $G$ is a perfect matching.

Related claimed results include an exact signed-subset-sum criterion for ordinary labels, Johnson-graph set-system rigidity, structural classifications for several graph classes, complementary-neighborhood obstructions, Cayley-graph phantom periods, and an elementary-abelian-2 switching classification.

See [the Paper 1 index](papers/universal-distance-antimagic/README.md), [the theorem ledger](THEOREM_LEDGER.md), and [current status](STATUS.md).

## 2. Nonlinear finite-field constructions

For a Cayley graph on the additive group of a finite field, the neighborhood-sum map is viewed as a translation filter:

$$
(T_S f)(x)=\sum_{s\in S} f(x+s).
$$

The project describes paired-affine-line constructions that send the nonlinear permutation monomial $x^{2p-1}$ to a sparse linearized weight polynomial. The claimed consequences include dimension-three, even-dimensional, and fixed odd-dimensional infinite families, explicit finite-field examples, and an obstruction in dimension two for connection sets built from complete affine $\mathbb F_p$-lines.

The full proof and certificates should be added before these claims are cited as established results. See [the theorem ledger](THEOREM_LEDGER.md) and [current status](STATUS.md).

## 3. Exhaustive verification through order nine

The companion repository reports a complete classification of all 274,668 unlabeled simple graphs on nine vertices:

- 205,914 have pairwise-distinct open neighborhoods and received explicit distance-antimagic labeling certificates;
- 68,754 have repeated open neighborhoods and therefore cannot be distance antimagic;
- two separate verifiers report zero failures.

The companion repository contains the constructor, independent verifiers, catalogue provenance, expected SHA-256 digests, manuscript, and deterministic reproduction script:

**[zach7036/distance-antimagic-order9](https://github.com/zach7036/distance-antimagic-order9)**

This is a meaningful finite frontier advance. It narrows any possible counterexample to order at least ten, but it does not settle the conjecture in general.

## How to review this work

1. Start with [STATUS.md](STATUS.md) for the evidence available for each research track.
2. Use [THEOREM_LEDGER.md](THEOREM_LEDGER.md) to separate theorem candidates, computer-assisted results, and open questions.
3. Reproduce the order-nine computation from its [dedicated repository](https://github.com/zach7036/distance-antimagic-order9).
4. Consult [LITERATURE_NOTES.md](LITERATURE_NOTES.md) for primary background sources and the limits of the novelty search.
5. Treat priority as provisional until the full manuscripts receive specialist review and database-level citation checking.

## Repository map

```text
papers/                 Research-track indexes (full Papers 1 and 2 not yet present)
verification/           Verification status and links
STATUS.md               Evidence and review status by track
THEOREM_LEDGER.md       Claimed results and explicit non-claims
OPEN_PROBLEMS.md        Open directions
LITERATURE_NOTES.md     Background sources and novelty caveats
AI_ASSISTANCE.md        AI/computational-assistance disclosure
CITATION.cff            Repository citation metadata
RELEASE_NOTES.md        Project notes (no GitHub release is currently published)
```

## Scope and non-claims

- No general solution of the Kamatchi-Arumugam conjecture is claimed.
- No proof-assistant formalization is available.
- The fixed noncyclic-group pair problem remains open for groups of exponent greater than two.
- The even-degree Cayley problem on elementary abelian 2-groups remains open.
- Priority and novelty remain provisional.

## AI and computational assistance

Large language models, computer algebra, exhaustive enumeration, and search programs were used during exploration, error detection, proof auditing, and drafting. No AI system is an author. The human author is responsible for every released claim and any eventual submission.

## Citation and licensing

Citation metadata is available in [CITATION.cff](CITATION.cff). No license file is currently included, so reuse rights have not yet been granted explicitly.

## Background

The terminology and conjecture originate with Kamatchi and Arumugam's 2013 paper. Group-valued variants were developed by Cichacz, Froncek, Sugeng, and Zhou, and later papers continue to resolve special graph families. See [LITERATURE_NOTES.md](LITERATURE_NOTES.md) for links.

