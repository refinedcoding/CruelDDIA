# 1002

p1 - p26

## Overview

看书前大致翻了一下目录，全书分为三部分

1. Fundation， 总览，一些概念，如分布式场景下系统的可靠性、容灾、可扩展性，数据的序列化等
2. Distributed Data， 讲分布式存储的，如数据一致性协议，数据分区，分布式事务等
3. Derived Data，我觉得也可以叫 Distributed Computing，讲分布式计算，批处理、流处理等

## Reliable, Scalable an Matainable Application

### Reliability

可靠性指系统能承受某些类型的 fault, 这些类型包含了: HW fault, SW fault, Human fault

### Scalability

本书将可扩展性归结为系统在负载增加的情况下依然能维持一定的性能。

## Maintainability

可维护性有两方面，一方面是开发人员对的视角，如系统代码的可维护性、可方便地进行系统的迭代等；另一方面是运维人员的视角，一个好的系统能最大程度简化运维人员的手动配置作用

## 没有银弹

没有一个通用的分布式系统架构，使其可靠、可扩展、可维护，不同的业务场景会对架构提出不同的要求
