# Travel Salesman Path (TSP) 
The length shourtest tour and the order of vertices to visit for the shourtest tour in TSP problem is outputed. The shortest tour is also drawn as a figure.

<p align="center">
<img  align="center" src="https://github.com/saniaki/tsp/blob/main/images/TSP_Image.jpg" width="800"/>

### 1- Exact algorithm (tsp_exact)
The exact algorithm is very inefficent, O(n^2 2^n) time. Two algorithms are presented:
* tsp_hashtable: hash table is used to constructr the array in the tsp algorithm
* tsp_bitset: a bitset labeling to construct the array in the tsp algorithm  

In the input files, the first line indicates the number of cities. Each city is a point in the plane, and each subsequent line indicates the x- and y-coordinates of a single city. The distance between two cities is defined as the Euclidean distance.


### 2- Heuristic algorithm (tsp_heuristic)
We are not gauranteed to get the optimal solution. But, it is more effcient. Two versions of the algorithm are presented:
* tsp_heuristic
* tsp_heuristic_xtrick: an early_stop trick is used to minimize number of calculations to increase the efficiency. 

In this heuristic algorithm, we:
1.	Start the tour at the first city.
2.	Repeatedly visit the closest city that the tour hasn't visited yet. In case of a tie, go to the closest city with the lowest index. For example, if both the third and fifth cities have the same distance from the first city (and are closer than any other city), then the tour should begin by going from the first city to the third city.
3.	Once every city has been visited exactly once, return to the first city to complete the tour.


The first line indicates the number of cities. Each city is a point in the plane, and each subsequent line indicates the x- and y-coordinates of a single city. The distance between two cities is defined as the Euclidean distance .

### Comparisons (on tsp.txt file)
* tsp_hashtable and tsp_bitset: running time: hours, result= 26442.73
* tsp_heuristic and tsp_heuristic_xtrick: running time: less than 1 second, result= 32981.96

### Comparisons (on nn.txt file)
* tsp_hashtable and tsp_bitset: not feasible (on number vortecies more than ~25)
* tsp_heuristic: running time: 439 seconds, result= 1203406.50
* tsp_heuristic_xtrick: running time: 215 seconds, result= 1203406.50
