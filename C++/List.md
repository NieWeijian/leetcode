# 介绍

链表（list）数据结构包括两部分
	数据
	指向前后节点的指针

特性
	不能直接查找，只能循环遍历O（n）
	可以随意插入任意位置，O（1）
	内存空间不需要连续
	每个节点都需要额外的指针空间


# 列表的使用
在使用列表的时候实际上实在操作一个个节点。
每个节点包含两个元素，一是数据，二是下一个地址。
很多时候操作列表是在链接节点，操作节点链接的下一个地址。

## 链表末尾添加一个元素
typedef{
int data;
MyListNode * next_node;
}MyListNode ;

在后面操作列表的时候，为了能找到头节点，通常会定义一个头节点，保存地址。
MyListNode * HeadNode=new MyListNode();//C++初始化函数
MyListNode * list=new MyListNode();
HeadNode->next_node=list;//连上了下一个节点


在末尾连上一个节点：
MyListNode * node=MyListNode(val); //创建新节点
list->next_node=node;//链接上这个节点
list=node;//更新到链表的末尾


## 遍历链表
这里还可以用到那个迭代器的工具：
标准库里里面的数据结构都有一个it类型的迭代器，开头是it.begin()，结束是it.end()
![[Pasted image 20250214160331.png]]


如果不用迭代器遍历或者这是自己定义的链表没有迭代器的话
需要按照链表的原理进行遍历，
```
func(List * listHead)
{
	List * cur=listHead; 
	while(list!=nullptr)
	{
			cout << curr->val << " ";
			cur=cur.next;
	}

}


```

![[Pasted image 20250214160617.png]]


# 为什么这里ListNode* list 不用引用呢
1. 首先链表经常会出现空的情况，引用不能为空
2. 链表的nextptr是用指针，用引用会产生误解
3. 传递中间链表的灵活性

但是要修改链表的时候，可以用引用：
![[Pasted image 20250214162035.png]]
