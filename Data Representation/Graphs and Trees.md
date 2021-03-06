# Graphs and Trees #

Graphs are a mathematical concept.

           Edge
        O--------O <--Node

Graphs are made up of vertices (aka nodes) connected by edges (aka arcs).

You can have weighted graphs, where each edge has a particular value/length, which can represent many different things.

A tree is a subset of a graph, but a graph cannot be a tree if cycles exist.

Edges can be directed, making them one-directional.

Graphs can be represented in computers using two main methods: adjacency lists and adjacency matrices.

# Adjacency List #

|Node   |  Connect to|
|:-----:|:----------:|
|  A    |  B1, C3    |
|  B    |  A1, C3    |
|  C    |  A3, B3, D10, E5|
|  D    |  C10       |
|  E    |  C5        |

The number after each connected node is the value of the vertex.

This can be represented in Python using dictionaries like this:

```
graph = {"A":{"B":1,"C":3},
         "B":{"A":1,"C":3},
         "C":{"A":3,"B":3,"D":10,"E":5},
         "D":{"C":10},
         "E":{"C":5}
        }
```

## Adjacency Matrix ##

|   |A  |B  |C  |D  |E  |
|:-:|:-:|:-:|:-:|:-:|:-:| 
|  A|0  |1  |3  |   |   |
|  B|1  |0  |3  |   |   |
|  C|3  |3  |0  |10 |5  |
|  D|   |   |10 |0  |   |
|  E|   |   |5  |   |0  |

This allows directed graphs to be formed easily as well by modifying the symmetry of the graph.

For using shortest path algorithms, an adjacency matrix is ideal.

## Trees ##

A tree is a graph that doesn't contain a cycle.

In Computer Science, binary trees are commonly used. Each node only ever has two branches.

In a binary tree, you will have a starting parent node, and the tree branches down from there.

```

                                P
                               / \
                              /   \
                             /     \
                            /       \
                           /         \
                          O           O
                         / \         / \
                        /   \       /   \
                       O     O     O     O
                      / \   / \   / \   / \
                     O   O O   O O   O O   O 
```

Adding to a binary tree is easy -- go left if the value is less than, or go right if it is greater than.

You can represent the binary tree as lots of pointers. This makes deleting easier as you are not required to move the entire tree, just the pointer.


## Traversing Binary Trees ##

Pre-order traversal -- V-L-R

In-order traversal -- L-V-R

Post-order traversal -- L-R-V

- V = Visit, return value of the node
- L = Left, go down left branch if it exists
- R = Right, go down right branch if it exists

These are all recursive algorithms.

```
                                1
                               / \
                              /   \
                             /     \
                            2       3
                           / \     / \
                          /   \   /   \
                         4     5 6     7
                                / \
                               8   9
```

Pre-order Traversal would produce 1,2,4,5,3,6,8,9,7

In-order Traversal would produce 4,2,5,1,8,6,9,3,7

Post-order Traversal would produce 4,5,2,8,9,6,7,3,1

But what's the point?

```
                                *
                               / \
                              /   \
                             /     \
                            +       C
                           / \
                          /   \
                         A     B
```

Pre-order Traversal: *+ABC  Prefix notation

Post-order Traversal: AB+C*  Postfix notation

In-order Traversal: A+B*C  Infix notation



## Graph Traversal ##

There are two main ways of traversing graphs.

- Depth-first traversal, where you go as deep into the graph as you can then work back up

This would be a recursive algorithm, as you would need to decend to the bottom of the graph before working your way back up. This can be accomplished in a binary tree using pre-order traversal.

- Breadth-first traversal, where you go level-by-level and output them before you descend lower down the graph.

The algorithm for this is:

 - Add node to queue
 - Visit node at front of queue
 - Add child nodes that are not already in the queue or fully explored to the queue
 - Set current node to fully explored
 - Next item in the queue