## 第九章 一致性和共识算法，P303 - P307，1001
- 保证服务随时可用，容错
- 隐藏系统细节，支持原子性，没有奔溃操作
- 支持隔离性和并发操作
- 支持持久性，数据完全可靠
- 所有节点能达成某些一致
- 在主从复制系统中，某个时刻有且只能由一个主节点，否则就发生脑裂

## 保证一致性
- 在主从，多主，无主复制系统中，如何避免复制
- 最终一致性，停止数据更新后，所有节点在一段时间后数据都会相同
- 所有副本最终都会收敛到相同值
- 弱保证的系统有局限性，本章讨论强一致性模型，比如线性化

## 可线性化
- 模拟单个副本，可线性化，原子一致性，强一致性
- TODO-分布式语义

## 图9-1 非线性化系统
- 裁判把比赛结果写入主节点
- 主节点复制结果到从节点1
- 客户端a从从节点1读取到比赛的最终结果
- 客户端b从从节点2读取到比赛的中间结果

## 图9-2 使用全局时钟来线性化并发操作

## 图9-3 如果某个客户端读到新值，其他的客户端也必须返回新值

## 线性化，P308 - P312, 1002
