## ACCESSING THE INTERACTIVE MAPS:
-> K-means Clustering: [https://goofyboga.github.io/clustering_weighted_addresses/kmeans_clusters_map.html]  
-> DBSCAN Clustering: [https://goofyboga.github.io/clustering_weighted_addresses/dbscan_clusters_map.html]  
-> Weighted Addresses: [https://goofyboga.github.io/clustering_weighted_addresses/CSESoc_weighted_map.html]  

If the above links fail to work, a static image has been provided below of it's use case:  
-> K-means Clustering:  
![image](https://github.com/user-attachments/assets/596dcd62-f4df-48aa-bf3d-6a7d8ef509e6)  
-> DBSCAN Clustering:  
![image](https://github.com/user-attachments/assets/ab0386b7-1c0c-4dfc-b40d-8755841a7379)  
-> Weighted Addresses:  
![image](https://github.com/user-attachments/assets/6c594ab4-eaf3-4cf7-810e-31b7eb88a00f)  

## Technical Summary
Given the potential variability of member locations, both K-means and DBSCAN clustering have been utilised to deal 
with both uniform and non-uniform density clustering respectively. For K-means, Silhouette Score method has been used 
to obtain the optimal number of clusters which came out as 4 to 6. I ended up selecting 6 clusters to prioritise smaller
groups. DBSCAN was more effective in providing localised clusters that was more geographically efficient as it accounted 
for irregularly shaped clusters of Sydney's population centres (non spherical). HOWEVER even in the best case selection of 
eps = 0.03 and min_samples = 3 -> DBSCAN still classifies ~15% of its data points as noise or outliers. This is highly unideal 
as the use case of a Runclub values minimal data point loss (inclusiveness of all members) over geographical optimisation. 
For this reason, K-means with a selection of 6 clusters has been deemed the most suitable clustering model selection.

## Specification 
Takes in input consisting of name, address and an attendance weight scale (1-5). Optionally, future improvements can be made 
to this script which differentiates between the organization's portfolios and divisions using different symbols.  


