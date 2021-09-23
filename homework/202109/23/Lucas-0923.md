## 分区，P199 - P204, 0923
- 分区，partition，分片，sharding，区别于副本
- shard：MongoDB，Elasticsearch，Solr Cloud
- Region：HBase
- tablet：Bigtable
- vnode：Cassandra，Riak
- vBucket：Couchbase
- 分区为了扩展性，如何分割数据，索引怎么配合
- 如何再平衡，路由请求
- 分区和复制是独立的

## 键值数据的分区
- 分区不公平，偏斜，skew
- 负载重的分区
- 可以把连续的键放在一起，比如Bigtable
- 主键是时间戳，方便按时间查询
- 但是同一段时间内，有可能写入过载
- 时间戳前加设备ID，均匀写入各个分区

## 按照键的哈希分区
- 避免热点，使用哈希来确定分区
- TODO-一致性哈希
- 确定，不支持主键的范围查询，如Couchbase，Voldemort
- Cassandra 只有第一列用来哈希，其他列作为SStables中排序数据的连接所有
- 组合索引方法，社交（user_id, update_timestamp) 是否用来哈希？
