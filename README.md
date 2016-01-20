# zzz_lib
zzz's c++ lib  

<br/>

* sbtree_map.h
* sbtree_set.h
* bpptree_map.h
* bpptree_set.h
* chash_map.h
* chash_set.h
* segment_array.h

标准库风格容器<br/>
standard library style<br/>

* sbtree系列

基于二叉搜索树实现,使用size平衡<br/>
可以随机访问,随机访问迭代器<br/>
有multimap/multiset实现<br/>

* bpptree系列

基于B+树实现<br/>
可以随机访问,随机访问迭代器<br/>
内存管理使用相同大小内存块<br/>
相比标准库map,迭代器在插入/删除元素之后会失效<br/>
sizeof(key)非巨大的情况下,插入/删除/查找速度都超过标准库map<br/>
sizeof(key)巨大的情况下去,内存占用会偏大,并且性能下降<br/>
遍历速度任何条件下都很快!比标准库map快得多!<br/>
有map/set/multimap/multiset实现<br/>

* chash系列

基于哈希表实现<br/>
内存集中分配,尽可能利用缓存加速<br/>
插入元素可能导致扩容,产生搬运数据操作<br/>
遍历速度飞快!<br/>
在允许重复key时候,equal_range返回local_iterator,仅支持erase操作<br/>
有map/set/multimap/multiset实现<br/>

* segment_array系列

基于B+树的节点管理策略实现<br/>
内存管理使用相同大小内存块<br/>
任意位置插入/删除成本都很低<br/>

<br/>
<br/>

* sbtree.natvis
* bpptree.natvis
* chash.natvis
* segment_array.natvis

加入到工程,调试时候有更友好的视图<br/>
custom views of native<br/>

<br/>
<br/>
<br/>

* split_iterator

迭代器方式进行split<br/>
适配std::string<br/>
不需要额外的内存存储split后的数据<br/>
无法预知总共会split多少段<br/>
附带了**不完整**string_ref实现<br/>

<br/>

* sparse_array.h

稀松数组...不成熟的玩意...<br/>