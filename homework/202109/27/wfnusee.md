# Chapter 2 Data Models and Query Languages

## Query Languages for Data
SQL 是一种 声明式 的语言。 IMS 和 CODASYL 则式一种指令式的语言。
```
function getSharks() { 
    var sharks = [];
    for (var i = 0; i < animals.length; i++) { 
        if (animals[i].family === "Sharks") {
            sharks.push(animals[i]); }
        }
        return sharks; 
    }
```
这是一种指令式的例子

写成 SQL
```
SELECT * FROM animals WHERE family = 'Sharks';
```

SQL放弃了许多能力也给了系统更多自动优化的空间。
大多数时候声明式的代码的执行都是并行的，而指令式的则很难自动并行。

## 网页上也支持声明式语法
一般通过xml定义... 老前端了，不解释了

## MapReduce Querying
Map Reduce 是 google 提出的一种大规模并行计算的变成模型。 许多 NoSQL 会用该模型进行数据查询。

```
db.observations.mapReduce( 
    function map() {
        var year = this.observationTimestamp.getFullYear(); 
        var month = this.observationTimestamp.getMonth() + 1; emit(year + "-" + month, this.numAnimals);
    },
    function reduce(key, values) {
        return Array.sum(values); 
    },
    {
            query: { family: "Sharks" },
            out: "monthlySharkReport"
    } 
);
```
mongodb查询的例子。
map和reduce必须是纯函数。相比于SQL而言仍然是比较低层的语言。
