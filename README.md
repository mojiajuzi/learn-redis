### 基础概念

#### 数据库(databases)
Ｒedis数据库的概念与关系型数据的概念是一样的，不过在Redis中我们使用数据库是为了用于不同应用的分组
使得不同应用的数据得以分离，Ｒedis中数据库以简单的数字进行命名

#### 命令(Commands)，键(Keys)和值(Values)
键是对数据进行标识的ID,而值则代表与键关联的真实数据，从整体上来看，Redis中的所有数据都可以标识为
键值对的关系，不过对于值来说，可以有多种数据类型

#### 查询(Query)
在Ｒedis中，key是一切，而value则什么都不是，因为在Ｒedis只会对key进行操作，而不会对值进行任何的操作

#### 内存(Memory)和持久化(Persistence)
默认情况下Redis会基于keys的变化数量，将数据库的快照保存到硬盘，一般来说如果变化的key超过1000个
则每分钟保存一次快照，如果小于９个，将15分钟保存一次快照

除快照外，Ｒedis可以以追加模式运行，任何时候一个key的变化，将会被追加到保存在硬盘的文件中。
在某些情况下，可以忍受60秒数据的丢失，有的时候，为了换取性能，可以忍受赢家或者软件方面的失败
但是有些情况下，是不允许数据的丢失的，因此Redis给了一个设置的选项

Redis将所有的数据存储在内存中，因此这方面的开销依旧是费用最高的一部分

####总结
- key是数据的标识
- 数据值是任意结构的二进制数组并且Redis并不关心值
-　Redis包含五种特殊的数据值结构

