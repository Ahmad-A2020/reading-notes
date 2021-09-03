- [Resources](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)
### Graphs
- Definition: A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.
- terminology :
            - Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
            - Edge - An edge is a connection between two nodes.
            - Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
            - Degree - The degree of a vertex is the number of edges connected to that vertex.
- **Undirected Graph**: is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.
- **Directed Graph**: also called a Digraph is a graph where every edge is directed.  Each node is directed at another node with a specific requirement of what node should be referenced next.
- types of graphs:
            - **Complete Graphs:** A complete graph is when all nodes are connected to all other nodes, on which  each vertex is actually connected to every other node on the graph
            -  **connected graph:** is graph that has all of vertices/nodes have at least one edge.
            -  **disconnected graph:** is a graph where some vertices may not have edges.


- An acyclic graph is a directed graph without cycles.

##### Graph Representation: 
- Adjacency Matrix: An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix
. Each Row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn’t a connection.
- Adjacency List:  An adjacency list is the most common way to represent graphs.An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.

##### Weighted Graphs
- Definition: A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.

##### Traversals: 
There are many concepts in traverse through the graph: 
- Breadth First: In this way the function visit all the nodes that are closest to the root as possible the below code for breadth first:
                ALGORITHM BreadthFirst(vertex)
                DECLARE nodes <-- new List()
                DECLARE breadth <-- new Queue()
                DECLARE visited <-- new Set()

                breadth.Enqueue(vertex)
                visited.Add(vertex)

                while (breadth is not empty)
                DECLARE front <-- breadth.Dequeue()
                nodes.Add(front)

                         for each child in front.Children
                         if(child is not visited)
                  visited.Add(child)
                breadth.Enqueue(child)   
  
                return nodes;
- Depth First:  In a depth first traversal, we approach it a bit different than the way we do when working with a depth first traversal of a tree. 
 ##### Real World Uses of Graphs
  - Graphs are extremely popular when it comes to it’s uses. Here are just a few examples of graphs in use:

    - GPS and Mapping
    - Driving Directions
    -  Social Networks
    - Airline Traffic
    - Netflix uses graphs for suggestions of products