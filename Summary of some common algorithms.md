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
The core idea of heapsort is to let the biggest/smallest value into the top. We call these max heap/min heap.</br>
Two characters of heapsort</br>
**left child = his parents x 2 +1**</br>
**right child = his parents x 2+2**</br>
There are three main steps to finish this algorithm. We use max heap as an example.</br>
### 1.Build a max heap.</br>
Find the last non-leaf node, and find and move the biggest one to this node from this node, its left child, and its right child. Repeat this until the biggest one in the top root. </br>
![Moving the biggest value to top node](/img/heapsort1.png)
Another is after you move the biggest one to the top, you need to clean up every changed non-leaf node to confirm that all the node is bigger than their child.</br>
![Adapting the changed node after moving](/img/heapsort3.png)
The time complexity of step 1 should be O(n)
### 2.Adapting the heap and keeping the biggest one in the tail node. 
In this step, what you need to do is swapping the top node and the tail node, and keep the biggest element in the tail node. And then adapt the heap like step1 and find the second biggest element and move it to current tail node. Continue to repeat these until all the nodes ordered.
Example
#### a.Swapping the top element 9 with tail node 4
![](/img/heapsortstep21.png)
#### b.Readjust the structure so that it continues to meet the heap definition
![](/img/heapsortstep22.png)
#### c.Swapping the top element 8 with the bottom element 5 to get the second largest element 8
![](/img/heapsortstep23.png)
#### final
![](/img/heapsortfinal.png)</br>
The total time complexity is O(nlogn)
