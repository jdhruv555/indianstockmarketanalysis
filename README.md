# Network-Analysis-of-the-Indian-Stock-Market

We constructed a network for the Indian stock market in this study using the correlation between various stock returns. 
The created network was then subjected to community detection techniques. 
Additionally, we utilised Gephi, an open-source network research and visualisation software, to create visualisations of the return correlations between several publicly traded equities. 
The visualisation results provide a very straightforward approach to examine the overall correlation structure of various public equities and to identify major market segments, which could be quite valuable in real-world applications such as market monitoring.
One advantage of constructing a network that characterises several stocks within a market is that some critical global features of the stock within the network, such as degree centrality, average degree, and betweenness centrality, can be extracted. 
Additionally, we examined the stock market’s behaviour during times of crisis.

## Problem Statement

Based on the background information and literature review, the problem to be investigated in this work is defined as follows: <br>
* **Network Visualization:** The datasets we are using do not include stock graphs, so we use the accessible information to construct the graphs utilizing techniques discussed in the literature review.
* **Community Detection:** Following the construction of a stock graph, we investigate how different groups play distinct roles in the stock market. 
How powerful a stock is and how it affects the value of other stocks and communities. 
For each node, we compute multiple centrality measures. 
This network would be used for portfolio diversification and portfolio management.
* **Crisis Analysis:** Using a smaller dataset, we also look at the stock market’s behaviour before and during the COVID-19 pandemic. 
This enables us to visualise and examine the spread of market crisis behaviour.

## Dataset

For this study, we gathered two datasets. 
The NIFTY200 dataset is being used to analyse stock correlation, while the NIFTY top 30 dataset would be used to investigate the influence of Covid-19 on stock correlation.
Detailed description of the dataset can be seen in the report.

## Methodology

* **Defining Nodes and Edges:** The nodes represent stock firms, and the edges between them are constructed using cross-correlations of stock price changes. <br>
* **Detrending data and computing log returns:** Among the strategies discussed in literature, we chose Time-lag correlations of price movements (14) over a specified time period. Stock prices are highly moving time series data with intrinsic trends.
* 88Computing Correlation Matrix:** The Pearson correlation coefficient (12) was then calculated between the defined log returns.

Two different methods were used: 

1. **Winner Takes All Method**:
The Winner Take All method revolves around building a network from the correlation matrix if the value of the correlation coefficient is greater than a certain defined threshold.
2. **Minimum Spanning Tree Method**: The Minimum Spanning Tree method (13) used the distance matrix. The MST is the shortest spanning tree, which is a theoretical notion in graph theory.

## Conclusion

In this study, we have extensively analysed the NIFTY200 dataset and tried to decode the nature of the Indian Stock Market. We have also looked at the behavior of stock market during crisis in the NIFTY30 dataset. <br>

* Using the time series data we discovered several interesting features of both the datasets. We visualised stock splits and examined the influence of Covid on the stock market.
* Following that, we constructed the networks using the Winner Takes All and Minimum Spanning Tree approaches and comprehensively compared them. We divided the timeline into four windows to demonstrate the stock network’s dynamic character.
* We observed that the networks created by both the methods indeed exhibited the scale-free property with the MST method giving a better evidence. The average clustering coefficient calculated for Winner Takes All method and the small world property depicted by average shortest path length for MST method also agree with the real world graphs.
* By observing the degree of the nodes in the networks, we found that the Financial sector stocks have a major game-play in the stock market. We identified the main stocks to predict the movement of prices in the network using the betweenness centrality as a measure and yet again the Financial sector acted as a major pathway.
* We identified communities in networks using the Louvain technique for community detection, which is based on the modularity score. To visualise the discovered communities, we showed the stock networks for both approaches in appendix.
* From the Winner Takes All network as shown in Figure A1, we observe that few sectors like IT (pale green) and Metals (dark blue) have a dense cluster within their own sector.
* Finally we visualised the results of the stock market during crisis using the NIFTY30 dataset. <br>

By studying the evolution of these communities over time, we can conclude that some sectors essentially trade together as a group while others don’t. Detailed analysis of the results is provided in the report.

## Graphs

**1. Winner Takes All Method**
<p align="center">
<img src = /Results/wta.png width="720" />
</p>

**2. Minimum Spanning Tree Method**
<p align="center">
<img src = /Results/mst.png width="720" />
</p>

**3. Crisis Analysis**
<p align="center">
<img src = /Results/ca.png width="720" />
</p>
