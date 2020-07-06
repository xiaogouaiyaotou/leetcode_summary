Sliding window:Q1176





Q929 

实际上是用正则表达式进行匹配 

Set()是建立一个无重复的列表 

Xxx.spllit(‘+’)[0]去除掉‘+’之后所有的字符 

Xxx.replace(‘x’,’y’)将其中的x替换为y 

Local, domain=xxx.split(‘@’)  将@前后分别给到local和domain 

 

Q163, Single Number 

主要运动异或^（遇到相同的变为0，其他情况保持不变） 

For I in range(len(xx)): 

           Num^=nums[i] 

只循环一次，把所有的都放在一起，其相同的变为0，最后只留下一个单独的 

 

Q226 Invert binary tree 

注意一点，可以对两边节点直接进行交换，和交换两个数一样，找个中间数过度就行了 

 

Q169 

有人用随机算法是最骚的，随机算法，简而言之,就是每轮循环用randint设置一个随机数，然后从头到尾与这个随机数进行对比，讲重复的进行记录，此情况分好坏，因为不能控制哪次能遇到这种。时间复杂度是从O（N）-O（N^2） 

Q141. 寻找是否有循环链表 

通过设置快慢指针来实现，快指针每次走两步，慢指针每次走一步，如果快慢指针相遇就说明存在循环。 

            temp2.sort() 

            temp=temp+temp2 

            temp2.clear() 

 

Q287 

1.先对函数进行排序，这样如果有相等的两个数一定相邻。 

2. 利用数组的下标，将检索过的数字对应下标位置的内容存储为原数字的负数。这样既能保存原数字的大小，又能存储到该数字是否存在的信息。（其之所以能实现的原因是题目中限定了值的大小一定小于数组最大下标） 

 

Q49, 

对每个字符进行排序后，再整合成一个字符，就能整体查找而避免对每个字符的单个搜索 

Q459. 

这题看了个答案是在是高 https://blog.csdn.net/chip_wan/article/details/82156522 

其余方法， 

Q53 

 本质上是一个动态规划 

设置一个指针在列表中移动，每个对这个指针之前的结果做出最有解，随着指针向后移动更新每次加上新东西和之前最优解的对比即可得到最终最优解 

Q3. 
method1
Setting two pointers to present the two boundary of the longest substring.
Using a non repeat list to store all the data.
The right bondary move from left to right one by one, and if the right boundary didn't in the list, add it into the list.
Else, if the right pointer in the lists, delete left pointer one by one until the right pointer didn't appears in the list.
Attention, you should operate the list and the left pointer in the meanwhile.

## Transfer from issue part
I will continue to read the summary from here. I wrote the summary in issue before, but I suddently found that it will not show your operation in the contirbution if you just modify in the issue part. So I plan to continue my summary from here

### Q143. Reorder List
Two methods, onw way is I found from Internet before long time ago, and it's not a routine operation, but it can be done this problem. You can copy the link node to a list, and it's very easy for you to do anything in the list. There solution should not be the acknowledge point that they want you to do. </br>
Second, there are a a lot of skills you need to use for this problem. The general idea is divided into 3 points. </br>
1. Dividing the linked list into two, one for first half, another for last half. Here, you should use the fast/slow pointer to achieve this operation. </br>
2. Reversing the Second linked list. Here is examining the operation of reversing list. </br>
3. Combining these two linked list. </br>
### Q148. Sort List
We can find from the description that the time complexity should be O(n log n), this is going to be a sort problem. Based on the sort algorithm we know, the sort algorithm an O(n log n) time complexity has quicksort, merge sort, and heapsort. For there, we can use mergesort. First, we use fast/slow pointer to divide the link into two linked lists. Second, we sorted these two linked lists and then sort these two linked lists.
### Q75. Sort Colors
Because there is only three numbers, so we can set two pointers to do a record. One is for 0 another is for 2.
### q19. Remove Nth Node From End of List
Very intersting problem, another types of double pointers. We can let the fast pointer run K-1 times at first, and then let the fast and slow pointer run togerther. When the fast pointer arrives the end, the slow pointer arrives the n-th node from the end o f list.
### Interview problem 62,The last number left in the circle
No algorithmic skills,it's just a math problem. it can generalize the rules of the subject to a funtion :</br>
f(n, m) = 0         (n = 1)</br>
f(n, m) = [f(n-1, m) +m] % n  (n > 1)  </br>
### Q16. 3Sum Closest
Two pointers. First we need to do a sort for the list. And let left pointer(L)=i+1, right pointer(R)=n-1. and do doop when L<R, there are cases to consider: 1. let sum=nums[i]+nums[L]+nums[R], if sum=target, return target. 2. If abs(sum-target)<abs(res-target), it shows sum is closer to the target, then update res. 3. if sum-target>0, it presents nums[R] is too big, we need to move R to leff. 4. if sum-target<0, it presents nums[L] is too small, move L to right.
### Q343 Integer Break
Good question. We can sovle it by math method or DP. And I don't really understand the mathematical derivation. So I just represent DP method here.
The function should be dp[i]=max(dp[i],dp[i-j]*j,(i-j)*j). Here, about dp[i-j] and (i-j), dp[i-1] includes the case that cut at least once in i-j, and i-j means only cut once at i-j. Because we need to know the optimal solution at each length then we can get the results by dp.
