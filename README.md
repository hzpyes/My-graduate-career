# Brandes-algorithm
Concurent implemenation of brandes algorithm. In simple words it allows to deiscover the most important nodes in graphs, for
example to find the most important influencers in social network. The code is capable to use power of all threads avaiable in computer.

**Node betweenness centrality: the definition**

Betweenness centrality for a node v is defined in terms of the proportion of
shortest paths that go through v. Specifically:
1. Assume a directed, unweighted, connected graph G =< V, E >.
2. Define σ(s, t) as the number of shortest paths between nodes s and t.
3. Define σ(s, t|v) as the number of shortest paths between nodes s and t
that pass through v.
4. CB(v), the betweenness centrality of v is defined as:
CB(v) = X
s,t∈V
σ(s, t|v)
σ(s, t)
If s = t, then σ(s, t) = 1. If v ∈ s, t, then σ(s, t|v) = 0.
Brandes’ algorithm is for the case where we want to calculate this efficiently for
every node.

*taken from : [http://www.cl.cam.ac.uk/teaching/1617/MLRD/handbook/brandes.pdf]*

<!--g++ -std=c++11 -o bd betweenness.cpp  -->
<!--./bd 1 test.txt output.txt 3-->
<!--输入参数：进程数 数据集文件名  输出文件名  k个点-->

<!--# Undirected graph: as-skitter.txt-->
<!--# Autonomous Systems (From traceroutes run daility in 2005 by skitter - http://www.caida.org/tools/measurement/skitter)-->
<!--# Note: There were 22622 nodes with degree 0-->
<!--# Nodes: 1696415 Edges: 11095298-->
<!--# FromNodeId    ToNodeId-->
