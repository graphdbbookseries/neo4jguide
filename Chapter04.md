# 第四章 Neo4j 程序开发
#### 4 前述 P246<br>
原文：<br>
本章所有实例代码都可以从Neo4j的GitHub主页找到：https://github.com/neo4j-examples，建议读者结合实例代码学习以达到事半功倍的效果。
<br>

更正：<br>
本章所有实例代码都可以从Neo4j的GitHub主页找到：[https://github.com/neo4j/neo4j-documentation/tree/3.1/embedded-examples](https://github.com/neo4j/neo4j-documentation/tree/3.1/embedded-examples)和[https://github.com/neo4j-examples](https://github.com/neo4j-examples)，建议读者结合实例代码学习以达到事半功倍的效果。

<br/>
说明：<br/>
添加网址https://github.com/neo4j/neo4j-documentation/tree/3.1/embedded-examples

#### 4.2.2.2 将操作写进事务中 P249<br>
原文：程序4-7事务try、catch块<br>
 Try(Transaction tx = graphDb.beginTx())<br>
 {<br>
     // 本章所有操作放入到这个try、catch块中<br>
     tx.success();<br>
 }catch(Exception e){<br>
	Tx.failure()<br>
}<br>
finally<br>
 {<br>
     tx.finish();<br>
 }<br>
<br>
更正：<br>
Transaction tx = graphDb.beginTx();<br>
 try<br>
 {<br>
     //本章所有操作放入到这个try、catch块中<br>
     // ...<br>
     tx.success();<br>
 }<br>
 finally<br>
 {<br>
     tx.close();<br>
 }<br>

说明：原文中将Transaction tx = graphDb.beginTx()声明放入try后，导致作用域仅限于try程序块中,catch、finally程序块无法引用到tx对象，这将导致错误；另外在Neo4j3.1版本后Transaction类取消了finish方法并用close方法来关闭事务。<br>
####  4.2.2.4	为节点创建属性值 P255<br>
原文：<br>
<table border="1" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td width="111">
<p class="a" align="center">类型</p>
</td>
<td width="274">
<p class="a" align="center">描述</p>
</td>
<td width="241">
<p class="a" align="center">取值范围</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">boolean</p>
</td>
<td width="274">
<p class="a">布尔值</p>
</td>
<td width="241">
<p class="a">true/false</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">byte</p>
</td>
<td width="274">
<p class="a">8位的整数</p>
</td>
<td width="241">
<p class="a">-128到127</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">short</p>
</td>
<td width="274">
<p class="a">16位的整数</p>
</td>
<td width="241">
<p class="a">-32768到32767</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">int</p>
</td>
<td width="274">
<p class="a">32位的整数</p>
</td>
<td width="241">
<p class="a">-2147483648 到 2147483647</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">long</p>
</td>
<td width="274">
<p class="a">64位的整数</p>
</td>
<td width="241">
<p class="a">-9223372036854775808到9223372036854775807</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">float</p>
</td>
<td width="274">
<p class="a">IEEE754标准的32位浮点数</p>
</td>
<td width="241">
<p class="a"></p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">double</p>
</td>
<td width="274">
<p class="a">IEEE754标准的64位浮点数</p>
</td>
<td width="241">
<p class="a"></p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">char</p>
</td>
<td width="274">
<p class="a">16位无符号整数代表的Unicode字符</p>
</td>
<td width="241">
<p class="a">u0000 到 uffff (0 到 65535)</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">string</p>
</td>
<td width="274">
<p class="a">Unicode字符串</p>
</td>
<td width="241">
<p class="a"></p>
</td>
</tr>
</tbody>
</table>
</div>
更正：<br/>
<table border="1" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td width="111">
<p class="a" align="center">类型</p>
</td>
<td width="274">
<p class="a" align="center">描述</p>
</td>
<td width="241">
<p class="a" align="center">取值范围</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">boolean</p>
</td>
<td width="274">
<p class="a">布尔值</p>
</td>
<td width="241">
<p class="a">true或false</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">byte</p>
</td>
<td width="274">
<p class="a">8位的整数</p>
</td>
<td width="241">
<p class="a">-128到127</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">short</p>
</td>
<td width="274">
<p class="a">16位的整数</p>
</td>
<td width="241">
<p class="a">-32768到32767</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">int</p>
</td>
<td width="274">
<p class="a">32位的整数</p>
</td>
<td width="241">
<p class="a">-2147483648 到 2147483647</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">long</p>
</td>
<td width="274">
<p class="a">64位的整数</p>
</td>
<td width="241">
<p class="a">-9223372036854775808到9223372036854775807</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">float</p>
</td>
<td width="274">
<p class="a">IEEE754标准的32位浮点数</p>
</td>
<td width="241">
<p class="a">/</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">double</p>
</td>
<td width="274">
<p class="a">IEEE754标准的64位浮点数</p>
</td>
<td width="241">
<p class="a">/</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">char</p>
</td>
<td width="274">
<p class="a">16位无符号整数代表的Unicode字符</p>
</td>
<td width="241">
<p class="a">u0000 到 uffff (0 到 65535)</p>
</td>
</tr>
<tr>
<td width="111">
<p class="a">string</p>
</td>
<td width="274">
<p class="a">Unicode字符串</p>
</td>
<td width="241">
<p class="a">/</p>
</td>
</tr>
</tbody>
</table>
</div>
说明：<br/>
true/false 替换为 true或false，三个空单元用 /填充
