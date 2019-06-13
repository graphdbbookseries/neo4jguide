# 第九章 Neo4j 简体中文版

## 本章全部替换部分
**[1] 本章全部替换部分（共5处）<br>**
原文：标签 A<br>
更正：标签A<br>
说明：去掉标签与A之间的英文空格<br>
<br>
**[2] 本章全部替换部分（共4处）<br>**
原文：名称 A<br>
更正：名称A<br>
说明：去掉名称与A之间的英文空格<br>

## 9.4 指定节点图片P499<br>
**原文：**<br>
节点属性：image<br>
属 性 值：图片的相对路径或绝对路径，如 "image/公司/微云数聚.jpg"<br>
功    能：将节点显示为指定圆形图片<br>
要将节点显示为图片，需要做两件事：<br>
1.	将图片存放到服务器。本章所用图片均已事先准备好，并存放在下述文件夹：<br>
C:\neo4j-chs\neo4j-web-cn\webapps\ROOT<br>
2.	在节点中设置属性 image，用其指定图片的相对路径（也可以是绝对路径）。<br>
CREATE <br>
  (张老师:写作成员 {名称:"张老师", image:"image/作者/张老师.jpg"}), <br>
  (苏博士:写作成员 {名称:"苏博士", image:"image/作者/苏博士.jpg"}), <br>
  (庞砖家:写作成员 {名称:"庞砖家", image:"image/作者/庞砖家.jpg"}), <br>
  (陈博士:写作成员 {名称:"陈博士", image:"image/作者/陈博士.jpg"}),<br>
  (高博士:写作成员 {名称:"高博士", image:"image/作者/高博士.jpg"}), <br>
  (李博士:写作成员 {名称:"李博士", image:"image/作者/李博士.jpg"}), <br>
  (薛大侠:写作成员 {名称:"薛大侠", image:"image/作者/薛大侠.jpg"}), <br>
  (赵大侠:写作成员 {名称:"赵大侠", image:"image/作者/赵大侠.jpg"}),<br>
  (琴琴:写作成员 {名称:"琴琴", image:"image/作者/琴琴.jpg"}),<br>
  (家辉:写作成员 {名称:"家辉", image:"image/作者/家辉.jpg"}),<br>
  (国防科大:大学 {名称:"国防科大", image:"image/大学/国防科大.jpg"}),<br> 
  (枣庄学院:大学 {名称:"枣庄学院", image:"image/大学/枣庄学院.jpg"}), <br>
  (中科院:大学 {名称:"中科院", image:"image/大学/中科院.jpg"}), <br>
  (西安交大:大学 {名称:"西安交大", image:"image/大学/西安交大.jpg"}),<br> 
  (北京邮大:大学 {名称:"北京邮大", image:"image/大学/北京邮大.jpg"}), <br>
  (北体大:大学 {名称:"北体大", image:"image/大学/北体大.jpg"}), <br>
  (西南交大:大学 {名称:"西南交大", image:"image/大学/西南交大.jpg"}),<br> 
  (权威指南:著作 {名称:"Neo4j 权威指南", image:"image/著作/著作.jpg"}),<br>

**更正：**<br>
节点属性：image<br>
属 性 值：图片的URL，如 "http://we-yun.com/image/公司/微云数聚.jpg"<br>
功    能：将节点显示为指定圆形图片<br>
要将节点显示为图片，需要做两件事：<br>
1.	将图片存放到服务器。本章所用图片均已事先准备好，并存放在下述文件夹：<br>
http://we-yun.com/image/<br>
2.	在节点中设置属性 image，用其指定图片的URL。<br>
CREATE <br>
  (张老师:写作成员 {名称:"张老师", image:"http://we-yun.com/image/作者/张老师.jpg"}), <br>
  (苏博士:写作成员 {名称:"苏博士", image:"http://we-yun.com/image/作者/苏博士.jpg"}), <br>
  (庞砖家:写作成员 {名称:"庞砖家", image:"http://we-yun.com/image/作者/庞砖家.jpg"}), <br>
  (陈博士:写作成员 {名称:"陈博士", image:"http://we-yun.com/image/作者/陈博士.jpg"}),<br>
  (高博士:写作成员 {名称:"高博士", image:"http://we-yun.com/image/作者/高博士.jpg"}), <br>
  (李博士:写作成员 {名称:"李博士", image:"http://we-yun.com/image/作者/李博士.jpg"}), <br>
  (薛大侠:写作成员 {名称:"薛大侠", image:"http://we-yun.com/image/作者/薛大侠.jpg"}), <br>
  (赵大侠:写作成员 {名称:"赵大侠", image:"http://we-yun.com/image/作者/赵大侠.jpg"}),<br>
  (琴琴:写作成员 {名称:"琴琴", image:"http://we-yun.com/image/作者/琴琴.jpg"}),<br>
  (家辉:写作成员 {名称:"家辉", image:"http://we-yun.com/image/作者/家辉.jpg"}),<br>
  (国防科大:大学 {名称:"国防科大", image:"http://we-yun.com/image/大学/国防科大.jpg"}),<br> 
  (枣庄学院:大学 {名称:"枣庄学院", image:"http://we-yun.com/image/大学/枣庄学院.jpg"}), <br>
  (中科院:大学 {名称:"中科院", image:"http://we-yun.com/image/大学/中科院.jpg"}), <br>
  (西安交大:大学 {名称:"西安交大", image:"http://we-yun.com/image/大学/西安交大.jpg"}),<br> 
  (北京邮大:大学 {名称:"北京邮大", image:"http://we-yun.com/image/大学/北京邮大.jpg"}), <br>
  (北体大:大学 {名称:"北体大", image:"http://we-yun.com/image/大学/北体大.jpg"}), <br>
  (西南交大:大学 {名称:"西南交大", image:"http://we-yun.com/image/大学/西南交大.jpg"}),<br> 
  (权威指南:著作 {名称:"Neo4j 权威指南", image:"http://we-yun.com/image/著作/著作.jpg"}),<br>

**说明：修改了以下6点：**<br>
[1] "图片的相对路径或绝对路径"-->"图片的URL";<br>
[2] "image/公司/微云数聚.jpg"-->"http://we-yun.com/image/公司/微云数聚.jpg"; <br>
[3] "下述文件夹"-->"下述URL"; <br>
[4] "C:\neo4j-chs\neo4j-web-cn\webapps\ROOT"-->"http://we-yun.com/image/"; <br>
[5] "用其指定图片的相对路径（也可以是绝对路径）"-->"用其指定图片的URL"; <br>
[6] 所有以".jpg"结尾的这个图片路径中的"image"都改为"http://we-yun.com/image";<br>


