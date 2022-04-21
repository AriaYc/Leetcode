### 解题思路
本题主要问题也是由于输入字符串太长，如何在给定字符串中快速判断是否有重复substring，如果直接对比会需要大量重复计算。需要对
input进行预处理编码，即手动哈希。然后结合binary search来进行长度的猜测。本题最大的特点是需要进行双重哈希处理，题目作者
针对输入字符串进行针对处理，一组常见的字符串编码形式并不能通过。