
# Graphs (part 01)

Motivation: 
- The seven bridges of Königsberg
- Icosian puzzle
- [(Bakhshandeh et al., 2011) - Degrees of Separation in Social Networks](https://ojs.aaai.org/index.php/SOCS/article/view/18200/17991)
- [Indonesia submarine cable map](./figures/indonesia-submarine-cable-map.png)

## Graphs and graph models

**Definition 1**  
> A _graph_ $G = (V, E)$, consists of $V$, a nonempty set of _vertices_
> (or _nodes_) and $E$, a set of _edges_.  
> Each edge has either one or two vertices associated with it, called
> _endpoints_. An edge is said to _connect_ its endpoints.

<br>

**Definition 2**  
> A _directed graph_ (or _digraph_) $(V, E)$ consists of a nonempty set
> of vertices $V$ and a set of _directed edges_ (or _arcs_) $E$.  
> Each directed edge is associated with an ordered pair of vertices.  
> The directed edge associated with the ordered pair $(u, v)$ is said  
> to _start_ at $u$ and _end_ at $v$.


**TABLE 1** Graph terminology
| Type | Edges | Multiple Edges Allowed? | Loops Allowed? |
|------|-------|-------------------------|----------------|
| Simple graph | Undirected | No  | No  |
| Multigraph   | Undirected | Yes | No  |
| Pseudograph  | Undirected | Yes | Yes |
| Simple directed graph | Directed | No  | No  |
| Directed multigraph   | Directed | Yes | Yes |
| Mixed graph           | Directed and undirected | Yes | Yes |


## Graphs terminology and special types of graphs

### Basis terminology

**Definition 1**

**Definition 2**

**Definition 3**

**Definition 4**


### Some special simple graphs

- Complete graphs
- Cycles
- Wheels
- $n$-cubes

## Connectivity

**Definition 1** (for undirected graph)
> 

**Example 1**

**Definition 2** (for directed graph)   
> Let $n$ be a nonnegative integer and $G$ a directed graph.  
> A _path_ of length $n$ from $u$ to $v$ in $G$ is a sequence of edges
> $e_1, e_2, \ldots, e_n$ of $G such that $e_1$ is associated with
> $(x_0, x_1), $e_2$ is associated with $(x_1, x_2)$, and so on, with
> $e_n$ associated $(x_{n-1}, x_n)$, where $x_0 = u$ and $x_n = v$.  
> When there are no multiple edges in the directed graph, this path is  
> denoted by its vertex sequence $x_0, x_1, x_2, \ldots, x_n$.  
> A path of length greater than zero that begins and ends at the same
> vertex is called a _circuit_ or _cycle_.   
> A path or circuit is called _simple_ if it does not contain the same 
> edge more than once.

## Euler and Hamilton paths

**Definition 1** 
> An _Euler circuit_ in a graph $G$ is a simple circuit containing every  
> edge of $G$. An _Euler path_ in $G$ is a simple path containing
> every edge of $G$

**Example 1**


**Definition 2**   
> A simple path in a graph $G$ that passes through every vertex exactly  
> once is called a _Hamilton path_, and a simple circuit in a graph $G$  
> that passes through every vertex exactly once is called a
> _Hamilton circuit_. That is, the simple path $x_0, x_1, \ldots, x_{n-1}, x_n$  
> in the graph $G = (V, E)$ is a Hamilton path if $V = \{x_0, x_1, \ldots, x_{n-1}, x_n, x_0\}$ (with $n > 0$) is a Hamilton circuit if 
> $x_0, x_1, \ldots, x_{n-1}, x_n$ is a Hamilton path.

**Example 5**