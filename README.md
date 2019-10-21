a) 
APPROXIMATIONS ALGORITHM

An algorithm that runs in polynomial time and outputs a solution close to the optimal solution is called an approximation algorithm.

There are several optimization problems such as Minimum Spanning Tree (MST), Min-Cut, Maximum matching, in which you can solve this exactly and efficiently in polynomial time. But many practical significant optimization problems are NP-Hard, in which we are unlikely to find an algorithm that solve the problem exactly in polynomial time.

Examples of the standard NP-Hard problems with some of their brief description are as following:

• Vertex Cover - find minimum set of vertex that covers all the edges in the graph (we will describe this in more detail)
• Set Cover - find a smallest size cover set that covers every vertex

STATEMENT: find minimum set of vertex that covers all the edges in the graph (we will describe this in more detail) 
Definition: Vertex Cover 
Given a G = (V, E), find a minimum subset C ⊆ V, such that C “covers” all edges in E, i.e., every edge ∈ E is incident to at least one vertex in C.

ALGORITHM 
1) C←∅
2) while E 6= ∅
     pick any {u, v} ∈ E
     C ← C ∪ {u, v}
     delete all eges incident to either u or v
   return C
   
Observation:
The set of edges picked by this algorithm is a matching, no 2 edges touch each other (edges disjoint). In fact, it is a maximal matching. We can then have the following alternative description of the algorithm as follows. 

Conclusion:
A set of vertices such that each edge of the graph is incident to atleast one vertex of the set, is called vertex cover
Greedy algorithm may or may not produce the optimal solution
Approximation algorithm doesn’t always guarantee optimal solution but its aim is to produce a solution which is as close as possible to the optimal solution

STATEMENT : Approximating Set Cover
Definition : An Instance (X, F) of the set-covering problem consists of a finite set X and a family F of subset of X, such that every elemennt of X belongs to at least one subset of F :
 X = [ S∈F S 
We say that a subset S ∈ F covers all elements in X. Our goal is to find a minimum size subset C ⊆ F whose members cover all of X.
 X = [ S∈C S (1) 
The cost of the set-covering is the size of C, which defines as the number of sets it contains, and we want |C| to be minimum. An example of set-covering is shown in Figure 1. In this Figure, the minimum size set cover is C = {T3, T4, T5} and it has the size of 3.

Algorithm : Greedy-Set-Cover (X, F)

1)	U ← X 
2)	 C ← ∅ 
3)	 While U is not equal to 0
4)	do select an S ∈ F that maximizes |S ∩ U|
5)	U ← U – S
6)	C ← C ∪ {S}
7)	return C

b) As many moves as possible for a Knight (Horse) on a chess board starting from any arbitrary position. Knight cannot touch any square (place) second time.
 
 A knight's tour is a sequence of moves of a knight on a chessboard such that the knight visits every square only once. If the knight ends on a square that is one knight's move from the beginning square (so that it could tour the board again immediately, following the same path), the tour is closed; otherwise, it is open.
 
 The knight's tour problem is an instance of the more general Hamiltonian path problem in graph theory. The problem of finding a closed knight's tour is similarly an instance of the Hamiltonian cycle problem. Unlike the general Hamiltonian path problem, the knight's tour problem can be solved in linear time.


