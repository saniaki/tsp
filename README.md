# Travel Salesman Paath (TSP) 

### 1- Exact algorithm (tsp)
Two algorithms are presented:
* tsp_hashtable: hash table is used to constructr the array in the tsp algorithm
* tsp_bitset: a bitset labeling to construct the array in the tsp algorithm  

In the input files, the first line indicates the number of cities. Each city is a point in the plane, and each subsequent line indicates the x- and y-coordinates of a single city. The distance between two cities is defined as the Euclidean distance 


### 2- Heuristic algorithm (tsp_heuristic)
We are not gauranteed to get the optimal solution. Two versions of the algorithm are presented:
* tsp_heuristic
* tsp_heuristic_xtrick: an early_stop trick is used to minimize number of calculations to increase the efficiency. 

In this heuristic algorithm, we:
1.	Start the tour at the first city.
2.	Repeatedly visit the closest city that the tour hasn't visited yet. In case of a tie, go to the closest city with the lowest index. For example, if both the third and fifth cities have the same distance from the first city (and are closer than any other city), then the tour should begin by going from the first city to the third city.
3.	Once every city has been visited exactly once, return to the first city to complete the tour.


The first line indicates the number of cities. Each city is a point in the plane, and each subsequent line indicates the x- and y-coordinates of a single city. The distance between two cities is defined as the Euclidean distance .
