# 第二章 Neo4j 基础入门

#### 2.3.3	属性  P42<br>
原文：<br>
<table border="0" cellspacing="0" cellpadding="0">
<thead>
<tr>
<td>
<p class="a">类型</p>
</td>
<td>
<p class="a">说明</p>
</td>
<td>
<p class="a">取值范围</p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p class="a">boolean</p>
</td>
<td>
<p class="a">布尔值</p>
</td>
<td>
<p class="a">&nbsp;true/false</p>
</td>
</tr>
<tr>
<td>
<p class="a">byte</p>
</td>
<td>
<p class="a">8位的整数</p>
</td>
<td>
<p class="a">-128 to 127, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">short</p>
</td>
<td>
<p class="a">16位的整数</p>
</td>
<td>
<p class="a">-32768 to 32767, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">int</p>
</td>
<td>
<p class="a">32位的整数</p>
</td>
<td>
<p class="a">-2147483648 to 2147483647, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">long</p>
</td>
<td>
<p class="a">64位的整数</p>
</td>
<td>
<p class="a">-9223372036854775808 to 9223372036854775807, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">float</p>
</td>
<td>
<p class="a">32位 IEEE 754 标准浮点数</p>
</td>
<td>
<p class="a">&nbsp;</p>
</td>
</tr>
<tr>
<td>
<p class="a">double</p>
</td>
<td>
<p class="a">64位 IEEE 754 标准浮点数</p>
</td>
<td>
<p class="a">&nbsp;</p>
</td>
</tr>
<tr>
<td>
<p class="a">char</p>
</td>
<td>
<p class="a">16位无符号整数代表的字符</p>
</td>
<td>
<p class="a">u0000 to uffff (0 to 65535)</p>
</td>
</tr>
<tr>
<td>
<p class="a">string</p>
</td>
<td>
<p class="a">Unicode 字符序列</p>
</td>
<td>
<p class="a">&nbsp;</p>
</td>
</tr>
</tbody>
</table>
更正：<br>
<table border="0" cellspacing="0" cellpadding="0">
<thead>
<tr>
<td>
<p class="a">类型</p>
</td>
<td>
<p class="a">说明</p>
</td>
<td>
<p class="a">取值范围</p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td>
<p class="a">boolean</p>
</td>
<td>
<p class="a">布尔值</p>
</td>
<td>
<p class="a">&nbsp;true或false</p>
</td>
</tr>
<tr>
<td>
<p class="a">byte</p>
</td>
<td>
<p class="a">8位的整数</p>
</td>
<td>
<p class="a">-128到127, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">short</p>
</td>
<td>
<p class="a">16位的整数</p>
</td>
<td>
<p class="a">-32768到32767, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">int</p>
</td>
<td>
<p class="a">32位的整数</p>
</td>
<td>
<p class="a">-2147483648到2147483647, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">long</p>
</td>
<td>
<p class="a">64位的整数</p>
</td>
<td>
<p class="a">-9223372036854775808到 9223372036854775807, inclusive</p>
</td>
</tr>
<tr>
<td>
<p class="a">float</p>
</td>
<td>
<p class="a">32位 IEEE 754 标准浮点数</p>
</td>
<td>
<p class="a">&nbsp;/</p>
</td>
</tr>
<tr>
<td>
<p class="a">double</p>
</td>
<td>
<p class="a">64位 IEEE 754 标准浮点数</p>
</td>
<td>
<p class="a">&nbsp;/</p>
</td>
</tr>
<tr>
<td>
<p class="a">char</p>
</td>
<td>
<p class="a">16位无符号整数代表的字符</p>
</td>
<td>
<p class="a">u0000 到 uffff (0 to 65535)</p>
</td>
</tr>
<tr>
<td>
<p class="a">string</p>
</td>
<td>
<p class="a">Unicode 字符序列</p>
</td>
<td>
<p class="a">&nbsp;/</p>
</td>
</tr>
</tbody>
</table>
说明：<br/>
单词to改为 到，去掉 inclusive，true/false 替换为 true或false，三个空单元用 /填充