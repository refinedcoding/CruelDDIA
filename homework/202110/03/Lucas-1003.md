## 线性化，P308 - P312, 1003
- Linearizability 可线性化，保证单个对象在读写寄存器保存最新值
- 不要求事务，无法避免写倾斜，需要实现实体冲突化
- Serializability 可串行化，隔离事务，每个事物可能读写多个对象

## 如何实现线性化
- 加锁和选举主节点
- 约束和保证唯一性
- TODO：跨通道的时间依赖

## 线性化系统的实现，P313 - P317, 1005

## TODO