### 解题思路：
因为array中只有0和1，所以我们不妨用count的方法来表示subarray中01的个数，即0的时候-1 1的时候+1。我们只需要记录第一次出现
sum的idx位置，当第二次出现相同sum的时候，我们只需要检查当前idx和第一次出现此sum的idx的距离。  
需要注意的是将(0, -1)记录进去可以处理sum=0时的情况。