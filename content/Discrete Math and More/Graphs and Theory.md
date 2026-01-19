---
tags:
  - Discrete-Math
---

I have previous knowledge of this, so important stuff will be left out at first.


- Know what edge and vertex are
- Graphs can be directed or undirected.

***Simple Graph***

- Has no loops and no multiple edges.


***Multigraph and Pseudographs***

Multi: may have multiple edges connecting the same two vertices.

Use this if we care about the number of links between data centers.

Pseudo: may include loops as well as multiple edges connecting the same pair of vertices.

Use loops when modeling diagnostic links at data centers.


***Directed Graphs***

Graphs associated with an ordered pair of vertices. Usually just a graph but add some arrows.


Terminology:

in-degree and out-degree: to be honest this is exactly what you think it is, arrows pointing to a vertex vs arrows coming from a vertex.

Adjacency is only outgoing edges.


***Handshaking Theorem***

The added degrees must be divisible by 2, dividing that number by two yields the number of edges.



***Complete Graph***

A simple graph that contains exactly on edge between each pair of distinct vertices.

- Know cycle
- Know wheel
- Wheels are not complete graphs by definition**



***Bipartite Graphs***

This is a type of simple graph:

No edges connect two vertices in V1 or V2 (you split the vertices into to groups)

Theorem:

A simple graph is bipartite if and only if it is possible to color the vertices red or blue so that no two adjacent vertices have the same color.

Bipartite graphs are useful because of their structure, they can be used to model relationships between two classes, and there are algorithmic advantages.




***Representing Graphs with Adjacency Matrices:***

This is too annoying to type, just think

a b c d
b
c
d

and mark how many connections each has (row) with (column)


***Paths***

A path is a sequence of edges that begins at a vertex and travels from vertex to vertex along edges.

A *circuit* is a closed path.

***Connectedness:***


Undirected Graphs are connected if there is a path between every pair of distinct vertices.


***Reflexive, Symmetric, Transitive in Graphs***



***Euler Paths and Circuits*** 

An Euler Circuit is a simple circuit containing every edge of graph G.

An  Euler path in G is a simple path containing every edge of G.


***1.) EULER's THEOREM***

If G has a vertex of odd degree, then G cannot have an Euler circuit. 

Contrapositive: If G contains an Euler circuit, then all vertices of G have an even degree. 

Degree is each vertex must be even, because the circuit contributes one when it begins, one when it ends, and two every time it passes through a vertex.

***2.) Hierholzer's Theorem***

Assume every vertex in G has an even degree, does an Euler circuit exists? Yes!


Theorem 2:

A connected undirected graph G contains an Euler path but not a circuit if and only if G contains two vertices of odd degree (beginning and end).

Additional Graph Theory:

[[Planar Graphs]]







**this note was imported from my other vault, ideas are not complete :(**



[[Discrete Math]]