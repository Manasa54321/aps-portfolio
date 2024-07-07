# APS Portfolio

<dl>
<dt>Course Name</dt>
<dd>Algorithmic Problem Solving</dd>
<dt>Course Code</dt>
<dd>23ECSE309</dd>
<dt>Name</dt>
<dd>Manasa S Hullatti</dd>
<dt>University</dt>
<dd>KLE Technological University, Hubballi-31</dd>
</dl>

* * *

> APS Portfolio
>
> Manasa

#### Note:
This page hosts:

1. Introduction
2. Why Portfolio
3. Objectives
4. Design
5. Challenges
6. To-Do


# Adaptive Bitrate Streaming (ABR)

Adaptive Bitrate Streaming (ABR) is a technology used in modern video streaming applications that can dynamically adapt in real-time, in order to provide the best quality for each individual viewer. ABR streams take into account network conditions, screen size, and device capabilities and can adjust on the fly to changes in available bandwidth and device resources. It is used to dynamically adjust video quality based on network conditions, improving the quality-of-service of the OTT platform.

## Process

The ABR process has three main steps:

### 1. Transcoding
The original video is transcoded into multiple versions, each with a different bitrate and resolution.

### 2. Packaging
The transcoded videos are then packaged into small segments, usually a few seconds each.

### 3. Delivery
When a user streams the video, the player dynamically switches between different bitrate segments based on real-time network conditions for smooth playback.

## Segment Trees in Transcoding

Segment Trees can be mainly used in the transcoding step. A Segment Tree is a data structure that stores data about a range of elements in nodes as a tree. It is mostly used to handle range queries with updates efficiently, with a time complexity of O(log n).

### Usage in ABR

Each video segment can be represented as an interval or range, where each range corresponds to a specific bitrate or resolution. The tree can be built and queried whenever required and is particularly useful for Dynamic Switching. As network conditions change, the segment tree can quickly adjust and provide the suitable segment. We can re-query the segment tree whenever there is a significant change in network conditions and dynamically switch to the new segment that matches the updated network condition.

### Benefits

This structure improves the quality of usage even in fluctuating network conditions.



# Database Management in OTTs

Database management involves the efficient handling, storage, and retrieval of vast amounts of data, including user information, content metadata, streaming data, and analytics. Various data structures and algorithms are employed to ensure that these tasks are performed efficiently. The research paper [1] focuses on enhancing user experience on OTT platforms through efficient data management.

## Data Structures Used

### B+ Tree
B-Trees and B+ Trees are commonly used in database indexing to provide efficient search, insertion, and deletion operations. B-Trees and B+ Trees ensure that the database can quickly locate records even in very large datasets. B trees have time complexity of O(logn) for insertion, deletion and search.

### Hash Tables
Hash Tables are used for fast lookups, especially in key-value stores and caching mechanisms. Hash tables are essential for quick access to frequently used data.

### Trie
Trie is very efficient for alphabetical data storage and retrieval. It is also used implementing autocomplete and prefix search features. Tries can be used to index and search for video titles and other metadata.

### Knowledge Graphs
Knowledge Graphs (Graph Database) are specifically developed and used for modelling relationships between entities, such as user interactions, social connections, and content recommendations.


---

# Recommendation Systems

A Recommendation engine or recommendation system is an information filtering tool that provides the most relevant suggestions regarding products or services to various customers. A recommendation engine generally uses machine learning algorithms to collect and analyze user activities such as their preferences, search history, and others. Knowledge graphs also play an important role in such systems in an OTT.

## Knowledge Graphs

A knowledge graph, also known as a semantic network, represents a network of real-world entities—such as objects, events, situations, or concepts—and illustrates the relationships between them. This information is usually stored in a graph database and visualized as a graph structure, prompting the term "knowledge graph."

### Graph Representation

Knowledge graphs can be represented in various forms, including:
- Adjacency lists
- Adjacency matrices
- Triple stores
- Edge lists

### Graph Traversal Algorithms

#### Depth-First Search (DFS) and Breadth-First Search (BFS)

DFS and BFS are used to explore nodes and relationships in the graph. They are useful for finding related entities or paths between nodes. The time complexity for both DFS and BFS is O(V + E), where V is the number of vertices and E is the number of edges in the graph.

### Similarity Scores

Similarity scores are generally determined by the cosine similarity algorithm.

### Pathfinding Algorithms

OTT platforms utilize algorithms like Dijkstra’s Algorithm and A* to calculate the shortest path between nodes in the knowledge graph. For instance, if a user has shown a preference for action movies directed by a specific director, Dijkstra’s Algorithm or A* can efficiently navigate the knowledge graph to recommend other action movies directed by the same director or featuring similar actors.

#### Dijkstra’s Algorithm and A*

Both Dijkstra's Algorithm and A* Algorithm have a time complexity of O((V + E) log V) with a binary heap, where V is the number of vertices and E is the number of edges in the graph.

## Conclusion

Knowledge graphs and graph traversal algorithms are essential components of recommendation systems in OTT platforms. They enable efficient exploration of relationships between entities and facilitate accurate and personalized recommendations for users.

* * *

### Prerequisites
* Code List 1 [Union-Find](https://github.com/prakashbh/day-today-codes/blob/master/10-union-find-basic.c) concepts.
