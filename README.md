APPROXIMATIONS ALGORITHM
An algorithm that runs in polynomial time and outputs a solution close to the optimal solution is called an approximation algorithm.
There are several optimization problems such as Minimum Spanning Tree (MST), Min-Cut, Maximum matching, in which you can solve this exactly and efficiently in polynomial time. But many practical significant optimization problems are NP-Hard, in which we are unlikely to find an algorithm that solve the problem exactly in polynomial time.
Examples of the standard NP-Hard problems with some of their brief description are as following:
• Vertex Cover - find minimum set of vertex that covers all the edges in the graph (we will describe this in more detail)
• Set Cover - find a smallest size cover set that covers every vertex
1.2 Approximation Algorithm for Vertex Cover Given a G = (V, E), find a minimum subset C ⊆ V , such that C “covers” all edges in E, i.e., every edge ∈ E is incident to at least one vertex in C.
. 
Observation: The set of edges picked by this algorithm is a matching, no 2 edges touch each other (edges disjoint). In fact, it is a maximal matching. We can then have the following alternative description of the algorithm as follows. 
Conclusion:
A set of vertices such that each edge of the graph is incident to atleast one vertex of the set, is called vertex cover
Greedy algorithm may or may not produce the optimal solution
Approximation algorithm doesn’t always guarantee optimal solution but its aim is to produce a solution which is as close as possible to the optimal solution
