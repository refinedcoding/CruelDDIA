# CHAPTER2

p27- 42

应用软件的数据模型具有分层的特点，每一层需要关注的关键问题是该层数据模型会如何被下一层表示

不同层之间存在 transalation layer，比如应用层代码和DB之间 --- impedance mismatch，可以类比于电路中的阻抗，会导致层级之间的数据进行转换时需要额外的开销

## Relation Model VS Document Model

本章的讲述重点主要是数据模型的不同表示，这两种数据模型还涉及容错、并发性等，会在之后的章节覆盖

### Relation Model

1. 能更好地表示 Many to One, Many to Many 等实体关系，更好地支持跨表的 join 操作
2. Schema on write

### Document Model

1. 更适合表示 One to Many 的实体关系
2. schema on read 更加灵活的 schema 避免了引入多个表带来的膨胀现象
3. storage locality，数据没有被拆分到多个表中，但在进行更新时可能需要对整个文本对象进行不必要的重写或复制等操作

### Convergence

Realtion Model 与 Document Model 之间的界限不断在模糊，比如传统的 DB 也逐渐支持 XML、JSON 等文本的解析， NoSQL 也支持 join 操作(在客户端实现，尽管性能不佳)
