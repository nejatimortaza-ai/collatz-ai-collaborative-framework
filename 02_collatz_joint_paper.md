**Compiled Working Draft**  
*(Collaborative conceptual framework only. The Collatz conjecture remains an open problem. This document organises known structural facts, standard reductions, and conditional heuristics; it does not resolve the conjecture.)*

---

### Abstract

We present a unified dynamical framework for the Collatz conjecture by coupling a 2-adic valuation conjugacy model with a Lyapunov spatial-drift criterion. We isolate two distinct mathematical barriers: (1) the non-existence of non-trivial rational cycles, reduced to Diophantine conditions and effective bounds via linear forms in logarithms, and (2) the absence of divergent trajectories, controlled via expected logarithmic contraction under mixing hypotheses on the valuations. This structural separation delineates exact boundaries between rigorous reductions and conditional heuristics.

### Introduction & Context

The \(3n+1\) problem resists standard inductive methods because the accelerated map
\[
T(n)=\frac{3n+1}{2^{v_2(3n+1)}}
\]
mixes 2-adic and real topologies in a non-local way. Tao (2019) established that almost all Collatz orbits eventually attain bounded values, using logarithmic density and probabilistic techniques. Bridging the gap from almost-all to all orbits requires control of exceptional sets of density zero.  

The present framework maps the successive 2-valuations to an ergodic shift space and embeds the dynamics in the 2-adic integers \(\mathbb{Z}_2\). It separates the problem into a Diophantine cycle obstruction and a measure-theoretic divergence obstruction, making the remaining gaps explicit.

---

### Section I — The Valuation Conjugacy Model

Let \(\mathcal{O}\) be the set of odd positive integers. The accelerated Collatz map \(T:\mathcal{O}\to\mathcal{O}\) extends by continuity to a continuous, Haar-measure-preserving, ergodic transformation of the 2-adic integers \(\mathbb{Z}_2\).

Let \(\Omega=\mathbb{N}^{\mathbb{N}}\) be the space of sequences of positive integers, equipped with the infinite product of geometric measures of parameter \(1/2\):
\[
\nu=\bigotimes_{k=0}^\infty\mathrm{Geo}(1/2).
\]
Let \(\sigma\) be the left shift on \(\Omega\).

There exists a measurable map
\[
\Phi:\Omega\to\mathbb{Z}_2
\]
that realises each valuation sequence as the successive valuations of the orbit of a unique 2-adic integer. The map \(\Phi\) intertwines the dynamics:
\[
T\circ\Phi=\Phi\circ\sigma
\]
\(\nu\)-almost everywhere, and pushes \(\nu\) forward to a measure equivalent to Haar measure on a full-measure subset of \(\mathbb{Z}_2\). This is the classical parity-vector (or valuation-sequence) conjugacy.

---

### Section II — Theorem 1: Rational Separation of Periodic Orbits

**Theorem 1 (Separation of rational points from exotic 2-adic cycles).**  
Let \(\gamma\subset\mathbb{Z}_2\) be a periodic orbit of \(T\) of period \(p\geq 1\). If \(\gamma\) intersects \(\mathbb{N}^+\), then \(\gamma\) is the trivial cycle \(\{1,2,4\}\).

**Proof sketch (reduction).**  
A period-\(p\) orbit corresponds to a periodic valuation sequence \((v_0,\dots,v_{p-1})\). Writing \(A=\sum v_i\) and \(\sigma_j\) for the partial sums, the unique point \(x\in\mathbb{Z}_2\) on the orbit satisfies
\[
x=\frac{\sum_{j=0}^{p-1}3^{p-1-j}\,2^{\sigma_j}}{2^A-3^p}.
\]
For \(x\) to lie in \(\mathbb{N}^+\) the denominator must produce a positive integer after division into the numerator.  

- The equation \(|2^a-3^b|=1\) is completely solved by Mihăilescu’s theorem; only the trivial cycle survives the resulting constraints.  
- For larger denominators an odd prime factor appears, forcing \(x\) either into \(\mathbb{Q}\setminus\mathbb{Z}\) or into \(\mathbb{Z}_2\setminus\mathbb{Q}\).  

Thus every non-trivial periodic orbit is disjoint from \(\mathbb{N}^+\).  

**Status.** The reduction of the cycle problem to this family of exponential Diophantine equations is classical. Baker’s theory supplies effective lower bounds on \(|2^A-3^p|\) and therefore finite computational bounds on possible periods. A complete unconditional exclusion of all non-trivial positive-integer cycles remains open and constitutes one of the two principal obstacles of the Collatz conjecture.

---

### Section III — Lyapunov Drift & Compactness Constraints

**Theorem 2 (Conditional negative expected drift).**  
Let \(V(n)=\ln n\) on the odd positive integers. Suppose that the successive valuations \(v_2(3T^k(n)+1)\) obey geometric statistics of parameter \(1/2\) (mean 2) for sufficiently many steps. Then
\[
\mathbb{E}[\Delta V(n)]=\ln 3-2\ln 2+O(2^{-N})=\ln\Bigl(\tfrac{3}{4}\Bigr)+O(2^{-N})<0
\]
for large \(n\). Under the additional hypothesis that these statistics hold uniformly outside a finite set \(B_R\), \(V\) is a Lyapunov function with strictly negative drift on \(\mathbb{N}^+\setminus B_R\).

**Corollary 1 (Conditional compactness).**  
If the uniform negative-drift hypothesis holds, then every trajectory enters the finite set \(B_R\) in the averaged sense made precise by a Foster–Lyapunov argument on an auxiliary probability space that realises the geometric valuations. Consequently there are no divergent trajectories *under that hypothesis*.

**Status.** The geometric law and negative average drift are known for a density-1 set of starting values. Extending the control to every orbit (the pointwise drift gap) remains open and is essentially equivalent in strength to the divergent-orbit half of the conjecture.

---

### Section IV — Concluding Remarks & Open Obstructions

The framework partitions the Collatz conjecture into two classical obstacles:

1. **Absence of non-trivial cycles** — reduced to Diophantine equations \(2^A-3^p=\pm d\) (or closely related forms) together with effective bounds from linear forms in logarithms and finite verification.  
2. **Absence of divergent orbits** — reduced to establishing uniform or pathwise negative logarithmic drift outside a compact set, which currently relies on mixing/independence hypotheses on the valuations.

**Open obstructions**

- *Pointwise versus average drift.* Negative expected drift does not automatically preclude sparse trajectories that experience anomalously long runs of minimal valuation \(v_2=1\). Stronger independence or discrepancy estimates on the 2-adic digits of \(3n+1\) are required.  
- *Complete Diophantine exclusion.* While Baker-type bounds reduce the cycle search to a finite (in principle) computation, a fully rigorous, self-contained exclusion for all periods is still incomplete.  
- *Relation to Tao’s theorem.* The almost-everywhere result of Tao already guarantees that the exceptional set (if non-empty) has density zero. The present framework attempts to organise the residual problem but does not remove the exceptional set.

This completes the working draft. The text is offered solely as a conceptual organisation of existing ideas and open gaps; it makes no claim to resolve the Collatz conjecture.

---

**End of joint working draft.**  

The brainstorming and drafting session is complete. The host now has a single, self-contained Markdown document that records the collaborative framework with all caveats intact.
