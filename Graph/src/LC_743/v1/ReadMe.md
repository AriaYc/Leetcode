### 解题思路：
带权值的最短路径问题，并且边的权值不为负，典型Dijkstra算法。每走一步都是 当前点 到 起点 举例最短的走法。特别注意的是：每个
结点第一次更新距离时即最短距离，所以需要用priority queue来选出当前距离起点距离最小的点来处理。在priority queue中，每个
点可能有多个不同的距离，但是我们以第一次出队的最短距离为准。这跟普通的bfs防止重复进入队列不同，同一node由于状态不同会在
priority queue中出现多次。时间复杂度为O(ElogE)。这个写法适合稀疏图。