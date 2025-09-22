#Maths/Combinatorics 
# Definition
A *(simple)* graph is defined as a set of vertices $V$ and a set of edges $E$ which connect two vertices *(undirected)*. And edge $e \in E$ is written as $xy$, *sometimes written as $(x,y)$*, where $x,y \in V$.
Graphs must have no loops and two vertices can only be connected by a single edge.
A finite graph is a graph with a finite number of vertices.
The degree *(also called order)* denoted as $|x|$ of a vertex $x$ is the number of edges incident to it - the number of edges connect to it.
***
# Properties
1. $\displaystyle G\text{ finite}\implies 2\Bigg|\sum_{v\in V}|v|$
2. $\displaystyle G\text{ finite}\implies\sum_{v\in V}|v|\leq (n-1)|V|$
## Explanations
1. $\displaystyle G\text{ finite}\implies 2\Bigg|\sum_{v\in V}|v|$
	1. Start with a finite graph with no edges so $\displaystyle \sum_{v\in V}|v|=0$
	2. Adding any edge has to connect two vertices and it will increase the order of each of those vertices by one increasing the sum by 2.
2.  $\displaystyle G\text{ finite}\implies\sum_{v\in V}|v|\leq (n-1)|V|$
	1. Given a finite graph any vertex can be connected to at most all other vertices.
	2. For a graph with $n$ vertices, for all vertices $v$, there are at most $n-1$ edges it can be connected so $|v|\leq n-1$
***
# Isomorphism
2 (simple) graphs are isomorphic if they have the same structure e.g. same number of vertices connected in the same way.
Rigorously two graphs $G=(V_{G},E_{G}), \ H=(V_{H}, E_{H})$ are isomorphic if there exists a function $f:V_{G}\to V_{H}$ called a graph isomorphism that satisfy the following properties
1. $f$ is [[Functions#Bijective|Bijective]]
2. $(u,v)\in E_{G} \Leftrightarrow (f(u),f(v))\in E_{H} \quad\forall u,v \in V_{G}$
***
# Subgraphs
A subgraph of $G$ is a graph each of whose vertices and edges belongs to $G$.
***
# Walks
A **Walk** is a route through a graph along the edges from one vertex to the next.
A **Path** (denoted as $P_{n}$) is a walk where no vertex is visited more than once.
A **Trail** is a walk in which no edge is visited more than once.
A **Cycle** *(denoted as $C_{n}$)* is a walk in which the end vertex is the same as the start vertex but no other vertex is repeated more than once. *(Basically a path that starts and ends at the same place, but strictly it is not a path as the star/end vertex is visited twice.)*
A **Hamiltonian Cycle** is a cycle that includes every vertex in a graph.
****
# Connection
Two vertices are connected if there exists a path between them. A graph is connected if every vertex is connected. If it is not connected it is disconnected.
***
# Complete Graph
A *Complete Graph (denoted as $K_{n}$)* is a graph in where every vertex is connected to every other vertex by an edge. 
It has $\displaystyle\frac{n(n-1)}{2}$ edges.
***
# Planar
A graph is planar if it can be drawn on a plane with no edges meeting/crossing over other than at the vertices.
***
# Tree
A tree is a *connected* graph which contains no cycles.
A spanning tree of a graph is a subgraph which contains all the vertices in $G$ and is also a tree.