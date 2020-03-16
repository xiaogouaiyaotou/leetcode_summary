-Greedy</br>
-DP</br>
     1.Knapsack Problem</br>
     2.longest comman subsequence</br>
     3.Longest common substring</br>
     4.</br>
-Backtracking</br>
-Divide-and-conquer</br>
-Branch-and-bound</br>
</br>
</br>
Waiting for study:</br>
merge sort</br>
count sorting</br>
Dijkstra algorithm               -------shortest path</br>
Kruskal algorithm                -------Minimum Spanning Tree</br>
</br>
## HeapSort
The core idea of heapsort is let the biggest/smallest value into the top. We call these max heap/min heap.</br>
Two characters of heapsort</br>
**left child = his parents x 2 +1**</br>
**right child = his parents x 2+2**</br>
There are three main steps to finish this algorithm. We use max heap as a example.</br>
### 1.Build a max heap.</br>
Find the last non-leaf node, and find and move the biggest one to this node from this node, its left child ,and its right child. Repeat this until the biggest one in the top root. </br>
Another is, after you move the biggest one to the top, you need to clean up every changed non-leaf node to confirm that all the node is bigger than their child.
