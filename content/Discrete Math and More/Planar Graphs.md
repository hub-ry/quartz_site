Consider the problem of connecting 3 houses to 3 separate utilities.

Is it possible join these houses so none of these connections cross?


***Definition***

A graph is planar if it can be drawn in the plane without any edges crossing. NOTE: THIS MEANS 3D. (put if it is planar in any dimension it can be drawn in 2d without crossing they just need to be rearranged.)

***Euler's Formula (1)*** 

G is a simple planar graph with e edges and v vertices. Let r be the number of regions in a planar representation of G. 

r = e -v + 2

Or regions in a planar representation of G will equal edges - vertices + 2. 

Note the 'outside' is a region too.


***Kuratowski's Theorem***

$K_{3,3}$ and $K_{5}$ are the most basic nonplanar graphs. 

If a graph contains either of these as a subgraph then they are nonplanar. You can find a subgraph by eliminating connecting points.


-A-------B-------C---

-A---------------C---

Elementary Subdivisions


Final Topic:

[[Graph Coloring]]








**this note was imported from my other vault, ideas are not complete :(**