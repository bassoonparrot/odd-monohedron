# A polyhedral sphere with congruent faces has an even number of faces

**Author:** Fable 5.2 / prompting by Dan Horwitz

This repository holds a claimed proof of the following.

> **Theorem 1.** Let a polyhedral sphere in Rᵈ have congruent faces: a cell decomposition of the sphere, its vertices mapped to Rᵈ, every face a planar simple polygon, all faces congruent (mirror images allowed) and meeting edge to edge. If every vertex has degree at least 3, or if the faces are quadrilaterals, then the number of faces is even.

Convexity and embeddedness are not assumed, and the dimension is arbitrary. For convex polyhedra in R³ the statement goes back to Grünbaum (1960). The general question was asked on MathOverflow in 2021 ([Are there monohedra with odd numbers of faces?](https://mathoverflow.net/questions/406120/are-there-monohedra-with-odd-numbers-of-faces)) and stated as open by Hungerbühler, Hungerbühler and Pirron (*New families of monohedral polyhedra*, J. Math. Arts 19, 2025).

## Status: not verified by a human

The proof was found in November 2026 by an AI system (Claude Fable 5.2, Anthropic). **No human mathematician has verified it.** It is published here so that it can be read and checked. Corrections, and references to earlier work, are welcome as issues on this repository.

## The argument in brief

1. **Reduction.** Counting sides and Euler's formula leave quadrilateral faces in which every side length occurs twice: parallelograms and kites (darts included).
2. **Parallelograms.** Strips of faces joined through opposite sides (zones) are closed curves that never cross themselves, and two closed curves on a sphere cross an even number of times.
3. **Kites.** Lift every vertex by one extra coordinate, a height that depends only on the combinatorics and on the shape of the kite, and weight that coordinate so that two angles of every lifted face become right angles. Every face is then inscribed in a circle (in a Lorentzian plane if the weight is negative, as for darts).
4. **The sign.** Round a quadrilateral inscribed in a circle, the reflections that reverse its four sides compose to one full turn, which is −1 on spinors. With the edge vectors as elements of a Clifford algebra, every face has holonomy exactly −1.
5. **The sphere.** On a sphere, face holonomies that are central multiply to 1. So (−1)^F = 1.

Step 5 fails on other surfaces, and so does the theorem: 9 congruent squares form a torus in R⁴, and 27 congruent squares form a two-coloured torus in R⁶.

Steps 4 and 5 give a statement of their own (Theorem 2 of the paper): a polyhedral sphere whose faces are convex polygons with an even number of sides and equal sums of alternate angles, for instance polygons inscribed in circles, has an even number of vertices. The faces need not be congruent. This is close to known results: Fomin and Pylyavskyy, *Incidences and tilings* (arXiv:2305.07728), Corollary 11.6, in the plane; and Izosimov, *Surface topology and incidence theorems over division rings* (arXiv:2603.00288), Theorem 7.3, on the sphere. Fomin and Pylyavskyy also count signs (their §10: an even number of anticoherent tiles), for points and lines. What is new there is only the parity conclusion for faces inscribed in circles. Step 3 is the part we did not find anywhere.

## Contents

| path | what it is |
|---|---|
| `paper/geometers.pdf` | the paper: statements, full proof, remarks, references. Start here |
| `paper/guide.pdf` | the same proof for readers with first-year university mathematics, with figures |

## Licence

CC BY 4.0. See `LICENSE`.
