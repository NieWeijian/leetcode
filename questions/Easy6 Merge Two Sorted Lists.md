# 复盘

首先建立一个自己的result_list，后面通过依次比较两个以给链表的最小值，链接到自己的链表末尾。
但是有些细节问题，怎么找到自己的链表头，这个头怎么链接下去。
我的做法是自己新起了一个head的node，值初始化就是0,并把这个头的下一个节点直接就连下去了。
但是这样的话，如果两个给定链表都是空的，那返回的这个头不是空，因为我们初始化值成0了。

思路是都想到了，但是代码写出来有点不清晰。


# 提解
这里在新建自己的result_list的时候建的明确定义了一个头和一个尾，初始的时候头和尾定在一起。
在增长的时候，更新尾，保留头。

选两个列表小的元素，链接到tail，tail_nextptr链接为那个节点的地址，被选中的list节点也更新去下一个。
tail移动到tail_next上准备找下一个节点。直到找到list节点为空


最后在接上非空list的时候，用了一个正则表达式
return result_list = list1== null ? list2 : list1
清晰明了了

![[Pasted image 20250214173702.png]]



![[Pasted image 20250214174727.png]]

