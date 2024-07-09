# Data Structures and Algorithms in OTT Platforms

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
> Data Structures and Algorithms in OTT Platforms

* * *

# Contents:
This page hosts:

1. Introduction
2. Objectives
3. OTT System Design
4. DSA in OTT Business cases
5. Conclusion
6. References

* * *

# Introduction
OTT platforms, short for Over-The-Top platforms, are online streaming services that deliver video and audio content directly to users over the internet. These platforms have fundamentally transformed the media and entertainment industry by offering a direct means of delivering content over the internet, bypassing traditional distribution channels. These platforms provide users with on-demand access to a vast array of movies, TV shows, music, and other media, catering to diverse preferences and viewing habits.

In the context of Algorithmic Problem Solving, OTT platforms present unique challenges and opportunities where the application of data structures and algorithms plays a crucial role in optimizing various aspects of platform operations. From enhancing user engagement through personalized recommendations to optimizing backend infrastructure for efficient content delivery, algorithmic solutions are integral to the success and scalability of OTT services.

![OTTs](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRMIVdKcYTnVsznWocI1k3TDTCGdSnsw21_cQ&s)

* * *

# Objectives
Objectives for this portfolio project are:
1. Outline the business scenarios applicable to OTT platforms.
2. Recommend appropriate data structures and algorithms for implementation.
3. Provide a sample code example for these algorithms or data structures in the given scenario.

* * *

# OTT System Design
![OTT System Design](/video-delivery.png)

* * *

# Database Management in OTTs

Database management involves the efficient handling, storage, and retrieval of vast amounts of data, including user information, content metadata, streaming data, and analytics. Various data structures and algorithms are employed to ensure that these tasks are performed efficiently. The research [paper](https://www.researchgate.net/publication/352081148_Proposed_DBMS_for_OTT_platforms_in_line_with_new_age_requirements) gives insights on enhancing user experience on OTT platforms through efficient data management.

### Data Structures Used
#### B+ Tree
B-Trees and B+ Trees are commonly used in database indexing to provide efficient search, insertion, and deletion operations. B-Trees and B+ Trees ensure that the database can quickly locate records even in very large datasets.
B trees have time complexity of O(logn) for insertion, deletion and search and space complexity of O(n)

View [B+ tree code](https://github.com/Manasa54321/aps-portfolio/blob/main/Bplus.cpp)

#### Hash Tables
Hash Tables are used for fast lookups, especially in key-value stores and caching mechanisms. Hash tables are essential for quick access to frequently used data.
Time complexity: Insert/Delete/Search O(n)
Space Complexity: O(n)

View [Hash Table code](https://github.com/Manasa54321/aps-portfolio/blob/main/hash_table.cpp)

#### Trie
Trie is very efficient for alphabetical data storage and retrieval. It is also used implementing autocomplete and prefix search features. Tries can be used to index and search for video titles and other metadata.
Time complexity: Insert/Search O(n)
Space Complexity: O(n)

View [Trie code](https://github.com/Manasa54321/aps-portfolio/blob/main/trie.cpp)

#### Knowledge Graphs
Knowledge Graphs (Graph Database) are specifically developed and used for modelling relationships between entities, such as user interactions, social connections, and content recommendations.

* * *

# Data Search

### Inverted Index

An Inverted Index is a data structure used in information retrieval systems to efficiently retrieve documents or web pages containing a specific term or set of terms. In an inverted index, the index is organized by terms (words), and each term points to a list of documents or web pages that contain that term. It is widely used in databases for efficient search. In OTTs, it finds content based on keywords and phrases.

View [Inverted Index code](https://github.com/Manasa54321/aps-portfolio/blob/main/inverted_index.cpp)

#### Usage in OTTs

Keyword Search: When a user enters a search query, the platform tokenizes and normalizes the query.

Query Processing: The platform looks up the terms in the inverted index and retrieves the corresponding postings lists.

Result Ranking: The results are ranked based on relevance, often using factors like term frequency, document frequency, and other relevance metrics.

Display Results: The platform displays the ranked list of content items matching the search query.

#### Construction
An inverted index is constructed by tokenizing the words of a document, stemming the root word, and then recording Document IDs.

* * *

# Autocompletion

![KMP Algorithm](https://media.geeksforgeeks.org/wp-content/uploads/20221125004358/image-660x398.png)

One more feature found in OTT platform searches is Autocompletion. This uses the Trie data structure for content handling and storage. Autocomplete search can be of simple implementation using Knuth-Morris-Pratt (KMP) Algorithm (prefix matching) which has O(n + m) time complexity, where ‘m’ is the length of the pattern and ‘n’ is the length of the text. But complexity is when they have to be ranked which is achieved by PageRank algorithm.
Time complexity: O(n + m) time complexity, where ‘m’ is the length of the pattern and ‘n’ is the length of the text.

View [KMP Algorithm Code](https://github.com/Manasa54321/aps-portfolio/blob/main/KMP.cpp)


#### PageRank

PageRank is an algorithm originally developed by Google to rank web pages in their search engine results. It can be adapted to rank nodes in a graph based on their importance or influence. It uses Graph data structure to model its entities.

View [Pagerank algorithm](https://github.com/Manasa54321/aps-portfolio/assets/105267382/08e9f040-7de5-40e7-8121-bb2d9df04619)  implementation

* * *

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

DFS and BFS are used to explore nodes and relationships in the graph. They are useful for finding related entities or paths between nodes.
The time complexity for both DFS and BFS is O(V + E), where V is the number of vertices and E is the number of edges in the graph.

View [DFS code](https://github.com/Manasa54321/aps-portfolio/blob/main/dfs.cpp)

View [BFS code](https://github.com/Manasa54321/aps-portfolio/blob/main/bfs.cpp)

#### Similarity Scores

Similarity scores are generally determined by the cosine similarity algorithm.

### Pathfinding Algorithms

OTT platforms utilize algorithms like Dijkstra’s Algorithm and A* to calculate the shortest path between nodes in the knowledge graph. For instance, if a user has shown a preference for action movies directed by a specific director, Dijkstra’s Algorithm or A* can efficiently navigate the knowledge graph to recommend other action movies directed by the same director or featuring similar actors.

Dijkstra’s Algorithm :

![Dijkstra's Algorithm](https://upload.wikimedia.org/wikipedia/commons/5/57/Dijkstra_Animation.gif)

Both Dijkstra's Algorithm and A* Algorithm have a time complexity of O((V + E) log V) with a binary heap, where V is the number of vertices and E is the number of edges in the graph.

View [Dijkstra’s Algorithm](https://github.com/Manasa54321/aps-portfolio/blob/main/dijkstra_algorithm.cpp)

View [A* code](https://github.com/Manasa54321/aps-portfolio/blob/main/A_star.cpp)

* * *

# Real-time Adapatations - Adaptive Bitrate Streaming (ABR)

Adaptive Bitrate Streaming (ABR) is a technology used in modern video streaming applications that can dynamically adapt in real-time, in order to provide the best quality for each individual viewer. ABR streams take into account network conditions, screen size, and device capabilities and can adjust on the fly to changes in available bandwidth and device resources. It is used to dynamically adjust video quality based on network conditions, improving the quality-of-service of the OTT platform.

The ABR process has three main steps:
#### 1. Transcoding
The original video is transcoded into multiple versions, each with a different bitrate and resolution.
#### 2. Packaging
The transcoded videos are then packaged into small segments, usually a few seconds each.
#### 3. Delivery
When a user streams the video, the player dynamically switches between different bitrate segments based on real-time network conditions for smooth playback.

### Segment Trees in Transcoding

Segment Trees can be mainly used in the transcoding step. A Segment Tree is a data structure that stores data about a range of elements in nodes as a tree. It is mostly used to handle range queries with updates efficiently, with a time complexity of O(log n).
Time complexity: O(log n).

#### Usage in ABR

Each video segment can be represented as an interval or range, where each range corresponds to a specific bitrate or resolution. The tree can be built and queried whenever required and is particularly useful for Dynamic Switching. As network conditions change, the segment tree can quickly adjust and provide the suitable segment. We can re-query the segment tree whenever there is a significant change in network conditions and dynamically switch to the new segment that matches the updated network condition.

This structure improves the quality of usage even in fluctuating network conditions.

View [segment tree code](https://github.com/Manasa54321/aps-portfolio/blob/main/segment_tree.cpp)

* * *

# User Experience 

In OTT platforms, efficient content delivery and distribution are critical to providing a seamless user experience. Two key techniques used in this context are content caching and CDN (Content Delivery Network) management.

### Content Caching

Content caching involves storing copies of frequently accessed content closer to the user to reduce latency and bandwidth usage. This is essential for OTT platforms to deliver high-quality video streams without buffering. Commonly, LRU (Least Recently Used) cache is used for this purpose. LRU is a scheduling algorithm that evicts the least recently accessed items first when the cache reaches its capacity.

View [LRU cache implementation](https://github.com/Manasa54321/aps-portfolio/blob/main/LRu_cache.cpp)

* * *

# CDN

A CDN is a network of distributed servers that deliver content to users based on their geographic location.

**CDN in Netflix**
Netflix knows very well that if a video takes five more seconds than usual, and this happens a few too many times, they will lose subscribers. With the help of an intelligent CDN, when we hit the play button, the video can be fetched from multiple locations. They migrated to AWS for cloud storage and computing to achieve scalability and flexibility. They implemented their own CDN, OpenConnect, to optimize content delivery and reduce buffering by caching content locally at ISPs. This architecture ensures rapid, reliable video streaming and minimizes downtime. Netflix also contributes to the tech community by open-sourcing their AWS tools.

#### Consistent Hashing in CDNs
Generally, in CDNs, Consistent Hashing technique is used to distribute data across a distributed system in a way that minimizes reorganization when nodes are added or removed. It uses data structures like:

- **Hash Ring**: Represents the circular space where both content and servers are mapped.
- **Sorted Map**: Stores the positions of servers on the hash ring, allowing efficient look-up of the nearest server for any given content.

View [Consistent hashing](https://github.com/phaistos-networks/ConsistentHashing/blob/master/consistent_hashing.h) implementation

* * *

# Content Delivery - Data Compression

Compressed video and audio files are significantly smaller than their uncompressed counterparts. This reduction in size means less data needs to be transferred over the network, making efficient use of available bandwidth. There are many video formats, which are used on multiple occasions. But, OTT Platforms usually use certain specific video formats, MKV, MP4, AVI, AVCHD. Any video file that we have is defined by the type of containers and codecs present in it.

**Video Formats**
- MKV
- MP4
- AVI
- AVCHD
Any video file is defined by the type of containers and codecs present in it.

### Huffman Coding

Huffman coding is a widely used data compression algorithm that can be particularly useful in OTTs. OTT platforms manage extensive metadata for each piece of content, including titles, descriptions, actors, genres, etc. Compressing this metadata can save storage space and reduce retrieval times. Although Huffman coding is not typically used for the final compression of video and audio streams (which often rely on more complex algorithms like H.264, H.265, or VP9 for video, and AAC or MP3 for audio), it can be part of the initial steps in these algorithms.

The time complexity of the Huffman coding algorithm is O(n log n), where n is the number of unique characters or symbols in the input data

View [Huffman Coding code](https://github.com/Manasa54321/aps-portfolio/blob/main/huffman_coding.cpp)

* * *

# Subscription Management

For User Account Management Hash Tables and linked lists can be used.
Hash Tables: Efficient for storing user information such as username, email, password hashes, and subscription details. Allows for quick lookup and retrieval.
Linked Lists: Useful for maintaining a history of user transactions, including subscription upgrades, downgrades, and cancellations.

View [Hash Tables code](https://github.com/Manasa54321/aps-portfolio/blob/main/hash_table.cpp)
Time Complexity: Insert/Delete/Search: O(n)
Space Complexity: O(n)

View [LInked List code](https://github.com/Manasa54321/aps-portfolio/blob/main/linked_list.cpp)
Time Complexity: Insert/Delete/Search: O(n)
Space Complexity: O(1)

For the Subscription Plans, Binary Search Trees are suitable for organizing subscription plans based on features, pricing tiers, and duration. They allow for efficient searching and updating of plans.

Time Complexity: Insert/Delete/Search: O(n)
Space Complexity: O(n)

View [BST code](https://github.com/Manasa54321/aps-portfolio/blob/main/BST.cpp)

![BST Traversal](https://upload.wikimedia.org/wikipedia/commons/4/48/Inorder-traversal.gif)

# Load Balancing

The **Assignment Problem**, traditionally used in operations research to optimize resource allocation, can be applied to load balancing and fault tolerance in OTT platforms. It involves assigning a set of tasks (e.g., user requests) to a set of agents (e.g., servers) in a way that minimizes the total cost or maximizes efficiency. 
The task is each server is an agent, and each incoming request is a task. The goal is to assign requests to servers to balance the load while minimizing latency or maximizing resource utilization. We should continuously update the cost matrix based on real-time metrics like current server load, latency, and network conditions. The **Hungarian algorithm** can be used to solve the assignment problem efficiently.

Time Complexity: O(N^3)

View [Hungarian algorithm code](https://github.com/Manasa54321/aps-portfolio/blob/main/assignment_problem.cpp)

# Conclusion
Algorithmic Problem Solving in OTT platforms focuses on using data structures and algorithms to address specific business challenges such as enhancing user experience, optimizing content delivery, and improving backend operations. By applying these techniques, OTT platforms can streamline their operations, deliver high-quality content efficiently, and ultimately provide a seamless and satisfying user experience.

# References

[1] Wikipedia contributors, "Over-the-top media service," Wikipedia, The Free Encyclopedia. Available: https://en.wikipedia.org/wiki/Over-the-top_media_service.

[2] Medium, "Smart Recommendation System for OTT Platforms," Mobiotics. Available: https://medium.com/mobiotics/smart-recommendation-system-for-ott-platforms-f0e79b8e520.

[3] DLSU, "Utilizing the Cosine Similarity Algorithm for Recommendation Systems," Animo Repository. Available: https://animorepository.dlsu.edu.ph/cgi/viewcontent.cgi?article=1801&context=conf_shsrescon#:~:text=By%20utilizing%20the%20cosine%20similarity,using%20the%20cosine%20similarity%20algorithm.

[4] IBM, "Knowledge Graph," IBM. Available: https://www.ibm.com/topics/knowledge-graph.

[5] Bitmovin, "Adaptive Streaming," Bitmovin. Available: https://bitmovin.com/adaptive-streaming.

[6] GeeksforGeeks, "Segment Tree Data Structure," GeeksforGeeks. Available: https://www.geeksforgeeks.org/segment-tree-data-structure/.

[7] ResearchGate, "Proposed DBMS for OTT Platforms in Line with New Age Requirements," ResearchGate. Available: https://www.researchgate.net/publication/352081148_Proposed_DBMS_for_OTT_platforms_in_line_with_new_age_requirements#pf9.

[8] GeeksforGeeks, "Inverted Index," GeeksforGeeks. Available: https://www.geeksforgeeks.org/inverted-index/.

[9] PrepBytes, "String Matching Algorithm," PrepBytes. Available: https://www.prepbytes.com/blog/strings/string-matching-algorithm/.

[10] Medium, "How the Cloud and CDN Architecture Works for Netflix," ResellerClub. Available: https://teamresellerclub.medium.com/how-the-cloud-and-cdn-architecture-works-for-netflix-8f3d17906782.

[11] Muvi, "The Best Video Format for OTT Platforms Decoded," Muvi. Available: https://www.muvi.com/blogs/the-best-video-format-for-ott-platforms-decoded/.

[12] GitHub, "PageRank," GitHub. Available: https://github.com/louridas/pagerank.

[13] GitHub, "Consistent Hashing," GitHub. Available: https://github.com/phaistos-networks/ConsistentHashing/blob/master/consistent_hashing.h.

[14] GitHub, "OTT Media Video Delivery," GitHub. Available: https://github.com/kanmaytacker/system-design/blob/master/OTT/media/video-delivery.png.
