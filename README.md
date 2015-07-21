# 需要了解的算法
##排序
- [x] Insertion Sort
- [x] Bubble Sort
- [x] Selection Sort
- [x] Shell Sort
- [x] Quick Sort
- [x] Merge Sort
- [x] Count Sort
- [x] Radix Sort
- [x] Bucket Sort

## 图算法
- [x] Dijkstra (Single Source Shortest Path)
- [ ] Bellman-Ford (Single Source Shortest Path)
- [x] Prim (Minimum Generated Tree)
- [x] Kruskal (Minimum Generated Tree)
- [x] Topological Order
- [x] DFS
- [x] BFS
- [ ] Floyd-Warshall (All Shortest Path)
- [ ] Ford-Fulkerson Method (Maximum Flow)

## 字符串算法
- [x] KMP
- [x] Rabin-Karp 
    * [白话分析字符串匹配算法——Rabin-Karp算法](http://blog.chinaunix.net/uid-23629988-id-2983531.html)
- [x] BM
    * [BM模式匹配算法-原理](http://www.iteye.com/topic/352954)
    * [字符串匹配的Boyer-Moore算法](http://www.ruanyifeng.com/blog/2013/05/boyer-moore_string_search_algorithm.html)

## 线性规划
- [ ] Simplex Method


## 几何学
- [ ] Graham's scan
- [ ] Jarvis March
# 常用的数据结构
- [x] Stack
- [x] Heap
- [x] Queue
- [x] Linked List
- [ ] Priority Queue
- [ ] Dequeue
- [x] Binary Tree
- [x] Binary Search Tree
- [ ] AVL Tree
- [ ] Red-Black Tree
# 常用的算法设计方法
## Divide Conquer(分治) 
分治法是先将问题规模为n的问题分解为两个规模为n/2的子问题，然后将两个子问题的
解合并为原问题的解。其实现的框架为
```
    f(input):
        res1 = f(one half of input);
        res2 = f(another half of input);
        res = merge(res1, res2);
        return res;
```    

其代表算法为mergesort和quicksort.

## Backtracing(回溯)
回溯算法是递归+恢复状态。其算法框架为
```
    f(input) 
        fetch one element x from input
        mark(x);
        f(input/{x})
        unmark(x);
```
## Dynamic Programming(动态规划)

## Greedy(贪心)
局部最优解为全局最优解。
- [ ] Huffman
- [x] Prim
- [x] Kruskal

## 分支限界法
分支限界法是回溯法求解设计寻找某个目标函数最小（或最大值）问题的一种变形方法。


## Binary Search(二分查找)
利用数据结构（如数组、有分查找树等）中元素已经排好序的这个性质。

## Two Pointer(从两头压缩问题)

## DFS(深度优先搜索)

## BFS(广度优先搜索)

# 算法比较
* Single Source Shortest Path
    * Dijkstra
        * 局限于边的权值非负的情况，若图中出现权值为负的边，该算法就是失效。 
           <pre> 
                  1 
           O----------->O
           |            ^ 
           | 2       -1 |
           ------>O------
           </pre>
    * Bellman Ford
        * O(V*E)
