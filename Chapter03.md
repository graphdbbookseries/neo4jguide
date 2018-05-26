# 第三章 Neo4j之 Cypher
#### 3.2.3 变量 P73
原文：match(`μg`:food) return `μg`<br>
更正：MATCH (`μg`:food) RETURN `μg`
说明：将match和return由小写改为大写，字体不变。<br>

#### 3.2.6 变量 P78
因为是格式问题，所以不方便采用原文和更正，直接用描述。<br>
说明：框内的MATCH等的格式与其他的框内的格式不同，主要指字体的格式不对。<br>

#### 3.3.8.5 用MERGE的唯一性约束P136
原文<br>
ERGE (laurence:Person) {name: 'Laurence Fishburne'}<br>
更正：MERGE (laurence:Person) {name: 'Laurence Fishburne'}<br>
说明："ERGE"前面缺失字母"M"<br>


#### 3.4.2.13 properties()P176
原文：C CREATE (p:Person {name: 'Stefan', city: 'Berlin'})<br>
更正：CREATE (p:Person {name: 'Stefan', city: 'Berlin'})<br>
说明：去掉了CREATE 之前多余的'C'字符<br>

#### 3.4.2.14 properties()P177
原文：R RETURN toInt('42'), toInt('not a number')<br>
更正：RETURN toInt('42'), toInt('not a number')<br>
说明：去掉了RETURN之前多余的'R'字符<br>

#### 3.5.2.2 节点属性存在性约束 P205
原文：CREATE CONSTRAINT ON (book:Book) ASSERT book.isbn IS UNIQUE<br>
更正：CREATE CONSTRAINT ON (book:Book) ASSERT exists(book.isbn)<br>
说明：将"book.isbn IS UNIQUE"改为"exists(book.isbn)"<br>
