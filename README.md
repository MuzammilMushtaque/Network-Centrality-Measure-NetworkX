# Centrality Measure of Graph

### Interpretation of Results

- Subgraph Sizes: The experiment considered ten different subgraph sizes, ranging from 10 to 300 nodes, distributed reasonably given the total number of nodes in the graph (146 nodes). The sizes were sampled multiple times, resulting in 50 measurements for each centrality metric.

- Degree Centrality:

        Mean runtime: 0.0034 seconds.
        
        The runtimes are relatively low and consistent, with a standard deviation of 0.0023 seconds.
        
        The maximum runtime observed was 0.0079 seconds, indicating that degree centrality is computationally inexpensive even for larger subgraphs.
        
- Closeness Centrality:

        Mean runtime: 0.4071 seconds.
        
        This measure shows a higher runtime variability, with a standard deviation of 0.4462 seconds.
        
        The maximum runtime was 1.6316 seconds, reflecting the increased computational complexity compared to degree centrality.
        
- Betweenness Centrality:

        Mean runtime: 0.5351 seconds.
        
        Betweenness centrality also exhibits significant variability, with a standard deviation of 0.5977 seconds.
        
        The maximum runtime observed was 2.2434 seconds, the highest among the three metrics, indicating that betweenness centrality is the most computationally expensive to calculate.
        

The procedure randomly selects nodes for each subgraph, can influence the results. Variability in the connectivity and structure of the sampled subgraphs might lead to fluctuations in centrality runtimes. To mitigate this, multiple samples were taken for each subgraph size, providing a more robust measure of average runtime.

#### Summary:

The results show how the runtime for each centrality measure scales with the size of the subgraph.
Degree centrality generally runs faster than closeness and betweenness centrality because it involves fewer calculations.

The results are in line with expectations. Degree centrality has the least computational complexity, followed by closeness centrality, with betweenness centrality being the most computationally expensive due to its reliance on shortest path calculations.


These runtime measurements help the organization understand the computational cost associated with analyzing different aspects of their network.
This can guide decisions on resource allocation and the feasibility of real-time analysis for different network sizes.

----------

**Recommendations**:

For large-scale real-time analysis, focus on degree and closeness centrality as they are computationally less intensive.
Use betweenness centrality selectively or in smaller subgraphs where its insights are most valuable.

---------

**Limitations and Future Work**:


*Graph Size:* The total graph size (146 nodes) is relatively small. Future work could explore larger graphs to observe how centrality measure runtimes scale with graph size.

*Sampling Method:* Different sampling methods (e.g., stratified sampling) could be employed to ensure a more representative selection of subgraphs.

*Algorithm Optimization:* Investigate optimized algorithms or parallel computing techniques to improve the efficiency of centrality computations, particularly for betweenness centrality.

By understanding the runtime characteristics of these centrality measures, organizations can make informed decisions about which metrics to use based on their computational resources and the size of their networks.
