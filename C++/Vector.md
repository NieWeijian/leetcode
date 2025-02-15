# 1 基本用法
Vector是一个动态数组，能自动管理内存和大小
	初始化：`vector<int> vec; // 创建空的整型vector`
	末尾添加元素：`vec.push_back(1);`
	末尾删除元素：`vec.pop_back()`
	在指定位置添加元素：vec.insert(vec.begin()+2,5)
	删除指定位置元素：vec.erase(vec.begin()+1)
	快速清空：vec.clear(); // 清空所有元素
	释放内存：vec.clear();
	访问指定元素：
		下标访问：vec[i]
		访问首位：vec.front()
		访问末尾：vec.back()
		访问元素个数：vec.size()
		访问容器容量：vec.capacity()
		检查为空：vec.empty()
		调整大小为：vec.resize(10)
		预留位：vec.reserve(10)
		

vec.begin和vec.front的区别在于begin是返回迭代一个迭代器并指向第一个元素。
vec.front是指向第一个元素的值。


# 2 Vector的遍历
## 2.1 迭代器
![[Pasted image 20250208160802.png]]
遍历vector的方法，其中有一种是迭代器。这种方法之前在c中没见过，但是这种思想很好，不管什么类型的数据，都可以用这个迭代器进行遍历。
其中it就是这个迭代器（iterator）。* it 可以获得实际值，++it移动到下一个迭代值，&(* it)获得迭代器地址。



## 2.2