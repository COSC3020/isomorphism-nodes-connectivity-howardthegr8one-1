[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ppBU16qM)
# Isomorphism

Prove that if two graphs $A$ and $B$ have the same number of nodes and are
completely connected, they must be isomorphic. I have started with the formal
definition of isomorphism below. Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$G_1=(V_1 , E_1)$ is isomorphic to $G_2 = (V_2, E_2)$ if there exists a
one-to-one and onto function (bijection) $f: V_1 \rightarrow V_2$ such that $(u,v)
\in E_1$ iff $(f(u),f(v)) \in E_2$.

## My Proof
Using a proof by induction let $P(n)$ be the statement: "If two graphs $A$ and $B$ are completely connected and have the same number of nodes then they *must* be isomorphic." We'll do this by showing that $P(n)$ is true for any $n$ where $n$ is the number of nodes of each graph. 

First let's look at $P(1)$ as our base case will be a graph containing a single node with zero edges as there are no other nodes for it to connect to. If we have two graphs $A$ and $B$ that each have a single node, then we can obviously map the node in $A$ to the node in $B$, and since neither graph has any edges to account for then we know these two graphs are isomorphic. 

Now that we've shown $P(k)$ is true for $k = 1$, we must show that $P(k+1)$ is true. We know that if we add a node to a completely connected graph we must also add $(k-1)$ edges as well since the new node must connect to all other nodes besides itself. So if we add a single node to each of our graphs from the base case we now have two graphs that each have a single edge and two nodes. Since we've already mapped the first node of each graph, then we only need to map this one new node from $A$ to $B$, and this mapping of nodes obviously will map the only corresponding edge in $A$ to the only edge in $B$. 

Since every additional node we add only adds $(n-1)$ edges, and if we've already mapped all $n$ nodes correctly and maintained the correct mapping of edges to those corresponding nodes, then no matter how many nodes we add to each graph, so long as they remain completely connected they will also remain isomorphic to one another. Therefore if two graphs $A$ and $B$ are completely connected and have the same number of nodes then they must be isomorphic. $ \blacksquare$
