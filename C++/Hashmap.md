# 1 基本用法

1. unordered_map<string,int> map;   键是string类型，值是int类型
2. map.insert("apple",1); 或者，map[apple]=1
3. 访问元素，
	1. int value=map["apple"]，如果这个键值不存在会自动创建，并初始化为0
	2. int value=map.count("apple")，检查键值是否存在，返回1,否则0
4. 删除元素：map.erase()
5. 返回迭代器：auto it = map.find("apple")，找到这个键值对应的键，但是是一个迭代器

# 实现twosum

利用hashmap查找只需要O(1)复杂度的优点，只要遍历一边目标数组就能找到答案。
用空间换时间。

![[Pasted image 20250209195115.png]]
hashmap的键是vector里的数字，键值是对应的vector的下标



