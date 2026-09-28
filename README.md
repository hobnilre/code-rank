# Ranking Structured Objects

Composable bijections, constrained rhythms and meaningful melody orders

## What this article adds, and why it matters

How can a list, a permutation or a tree acquire an integer coordinate that
reconstructs it exactly? This article gives one common construction: divide the
space into finite groups, count their objects, and combine the coordinates of
the parts. It derives both directions and follows a complete example from the
list `(2,0,1)` to coordinate **45** and back.
An explicit square-root inverse also recovers the pair `(110,134)` directly
from coordinate **30000**, showing how to invert the counts themselves.

A Fibonacci-tree application gives the five-part **long–long–short–short–long**
limerick contour and eight-part “super-limerick” continuations. An exact
recognition criterion determines which duration patterns belong to the family.
Counted restrictions give direct access to extensions that preserve a chosen
phrase: **four of sixteen** eight-part patterns retain the selected limerick
motif. Higher levels distinguish single and repeated appearances.

For melodies, a larger coordinate can mean something specific: **total pitch
movement never decreases**. The article derives a reversible order by accumulated
semitone travel, with explicit counts, tie order and a complete example:
C4–D4–C4 has coordinate **36** at the declared rhythm and starting pitch.
Finite rhythm families and instrument ranges fit into the same construction.
The measured movement is guaranteed; its relationship to perceived movement
is an explicit question for listening studies.

Labeled progression trees show how local compatibility rules produce new
completion counts and reversible coordinates. Reduced tuning ratios make
the distinction between a description and a unique value concrete: equivalent
fractions and octave classes require their own canonical domains. Compact
examples in expression syntax, subsets and labeled graphs show how the same
framework extends beyond music.

The same mathematics supports direct access without constructing every preceding
object, reproducible enumeration, disjoint work intervals and uniform sampling
from finite spaces. Finite grading extends the construction to infinite spaces.
The article makes the conditions explicit: object equality, empty cases,
compatible domains, terminating recursion and a fixed ordering convention.

Comparisons across Mathematica, Haskell, Java, Kotlin and Rust implementations
show why matching counts and a few successful round trips can miss an incomplete
object domain. Exact checks accompany the mathematical derivations. The result
also distinguishes bounded catalogue orders based on circular pitch classes
from counted orders that retain absolute semitone travel. The article
is a code-free account of an established combinatorial method with exact
constructions for constrained musical exploration. It separates reversible
identity, a deliberately ordered musical quantity, and judgments of similarity
or preference.

## Article and build

[Read the article (PDF)](ranking-structured-objects.pdf) · [Manuscript source](ranking-structured-objects.md)

Install GNU Make, GNU Coreutils, Pandoc, XeLaTeX and the TeX Gyre fonts, including the LaTeX
packages used by `preamble.tex` and `preamble-local.tex` and the TikZ/PGFPlots standalone figures.
Run `make pdf` from this repository. It regenerates changed figures and builds
the article without any sibling repository or private working files.

The first page gives the PDF creation time in UTC, followed by the
[GitHub repository](https://github.com/hobnilre/code-rank). An up-to-date PDF keeps its timestamp;
`make -B pdf` forces a rebuild. Intermediates go to ignored `build/` by default;
`BUILD_DIR=/absolute/path` selects another location. `make clean` removes that
build directory and keeps the published PDF and figure assets.

Shared typography is installed locally in `article-style.yaml`, `preamble.tex`
and `figures/figure-style.tex`. Article-specific definitions are in
`preamble-local.tex`. These files are complete build inputs; no tools checkout
is required.
