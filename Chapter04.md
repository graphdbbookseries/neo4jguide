# 第四章 Neo4j 程序开发
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
