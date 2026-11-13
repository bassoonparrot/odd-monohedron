# A polyhedron cannot have an odd number of congruent faces

**Author:** Fable 5.2 / prompting by Dan Horwitz

This is a claimed answer to the MathOverflow question [Are there monohedra with odd numbers of faces?](https://mathoverflow.net/questions/406120/are-there-monohedra-with-odd-numbers-of-faces) Claimed answer: nope, also without convexity.

I started looking into this a little while ago in response to my son's question about D&D dice, hit a wall with some prior models, but was able to get to the general result with Fable 5.2. I'm posting it here in case anyone's interested. The argument below was produced by that AI system. It hasn't been verified by a human, although it looks pretty reasonable to this human.

There are two PDFs in [`paper/`](paper/):

- [`geometers.pdf`](paper/geometers.pdf), for mathematicians: statements, full proof, remarks, references;
- [`guide.pdf`](paper/guide.pdf), the same proof with figures, which presupposes nothing beyond basic undergraduate math.

## Claims

"Polyhedron" means a closed surface with the topology of a sphere, made of flat faces meeting edge to edge. It may be non-convex, may cross itself, and may sit in any dimension.

1. **Congruent faces.** A polyhedron with congruent faces and at least three faces at every vertex has an even number of faces.
2. **Faces inscribed in circles.** A polyhedron whose faces are convex quadrilaterals, each inscribed in a circle, has an even number of faces. The faces need not be congruent and the circles are unrelated.
3. **Larger faces.** A polyhedron whose faces are convex polygons with an even number of sides, each inscribed in a circle, has an even number of vertices. Equivalently, the number of faces with 4, 8, 12, … sides is even. (The paper proves a more general form: the faces need only have equal sums of alternate angles.)
4. **The sphere is needed.** All three fail on a torus: 9 congruent squares form one in R⁴. Whether an odd torus exists in R³ is open.

## Sketch of 1

1. As in the comments on the question by M. Winter and David Eppstein, counting and Euler leave quadrilaterals in which each side length occurs twice: parallelograms and kites (darts included).
2. Parallelograms: the zones are closed curves that never cross themselves, and two closed curves on a sphere cross evenly. (The zonohedron argument needs convexity; this does not.)
3. Kites: lift each vertex by one extra coordinate, a height determined by the combinatorics and the kite's shape, weighted so that two angles of every lifted face become right angles. Each face is then inscribed in a circle (in a Lorentzian plane for darts), and the argument for claim 2 applies; the paper does this algebraically, in any signature.

## Sketch of 2 and 3

Take the edge vectors in the Clifford algebra. Round a convex face inscribed in a circle, the reflections that reverse its sides compose to one full turn, which is −1 on spinors. Each edge is run backwards by one of its two faces, which gives another −1 per edge. On a sphere these all multiply to +1, so faces + edges is even, and by Euler that is the parity of the number of vertices. For quadrilaterals there are twice as many edges as faces, so the number of faces is even.

Claims 2 and 3 are close to known results: Fomin–Pylyavskyy (arXiv:2305.07728, Cor. 11.6, and §10 for the count of signs) and Izosimov (arXiv:2603.00288, Thm. 7.3). What seems new there is only the conclusion for faces inscribed in circles. The lift in step 3 of the first sketch is what I could not find anywhere.

Corrections, and references to earlier work, are welcome as issues on this repository.

## Licence

CC BY 4.0. See `LICENSE`.
