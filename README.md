# Social Network Analysis of Murder on the Orient Express: A Graph-Based Exploration of Character Relationships

## Project Goals
- Character Network Creation
  
The core of the project involves creating a social graph where nodes represent the characters, and edges represent interactions or relationships between them. The strength and frequency of these relationships will drive the analysis.

- Network Analysis
  
The graph will then undergo various analyses to measure important network properties such as centrality (which characters are most important), clustering (how tightly connected characters are), community detection (grouping characters), and other network metrics.

- Comparison with Generative Models
  
By comparing the extracted social graph with theoretical network models, the project aims to explore how well the structure of the story matches typical patterns found in real-world or simulated social networks.

## Approach 

1. Make a List of Characters in the Novel
   
  Manually identify and extract a list of all characters in the novel. These will form the nodes of the social graph. 

2. Extract a Social Graph of the Manually Identified Characters in the Text
   
  After identifying the characters, the next step is to extract their interactions from the text. In a social graph:
  - Nodes: Represent the characters.
  - Edges: Represent interactions or relationships between characters (e.g., dialogues, mentions, or encounters in the book).
  - Edge Weights: Could be added to represent the strength of interactions (e.g., frequency of communication, intensity of the relationship).
  - The resulting social graph can be represented as an adjacency matrix or an edge list.

3. Calculate the Four Types of Centrality of Main Protagonists
   
  Once the social graph is built, use centrality measures to determine which characters are most "central" or influential within the network:

  - Degree Centrality: Measures the number of direct connections a character has. Characters with high degree centrality are involved with many others.
  - Betweenness Centrality: Measures the extent to which a character lies on the shortest paths between others. Characters with high betweenness centrality act as “bridges” in the network.
  - Closeness Centrality: Measures how close a character is to all other characters in terms of shortest paths. Characters with high closeness centrality can reach others in fewer steps.
  - PageRank: Based on the Google PageRank algorithm, this centrality takes into account not just the number of connections a character has but also the importance of the characters they are connected to.
  
4. Detect Communities
   
  Community detection involves finding clusters of characters that are more densely connected to each other than to the rest of the network.
  Algorithms like Louvain or Girvan-Newman can be used to automatically detect these communities.

5. Create Equivalent Generative Models to Compare Against the Social Graph
   
  To understand whether the social graph extracted from the novel reflects typical social patterns or is unique to the story, models like Erdős-Rényi (Random Graph), Barabási-Albert (Scale-Free Network), and Watts-Strogatz (Small-World Network) can be used.
