# Emmet常用快捷语法

###  HTML文档初始结构快捷语法
- html:5 或者 ! 生成 HTML5 结构
- html:xt 生成 HTML4 过渡型
- html:4s 生成 HTML4 严格型

###  标签属性生成快捷语法（# 、.）
- ul#page 生成带id的标签
- ul.name 一个class为name的ul标签
- ul#navigation.nav 同时指定标签的id和class，如生成id为navigation，class为nav的ul标签

###  兄弟标签生成快捷语法（+）
- div+ul+bq 生成标签的兄弟标签，即平级元素，使用指令+

###  后代标签生成快捷语法（>）
- div>ul>li >表示后面要生成的内容是当前标签的后代

###  上级标签生成快捷语法
- div>ul>li^span  编写一个跟ul平级的span标签，那么我需要先用“^”提升一下层次

###  重复多份快捷语法（*）
- ul>li*5 在ul下生成5个li标签

###  分组快捷语法（"()"）
- div>(header>ul>li*2)+footer>p 用括号进行分组，表示一个代码块，分组内部的嵌套和层级关系和分组外部无关

###  添加属性快捷语法（[attr]）
- a[href= "www.baidu.com" title = "百度"]  生成的a标签含有href和title标签也可以添加自定义属性

###  添加编号快捷语法（$）
- ul>li.item$*5 在ul下的li标签添加class属性值item依次递增从1-5
- ul>li.item$$$*5 $表示一位数字，只出现一个的话，就从1开始，如果出现多个，就从0开始
- ul>li.item$@-*5 在$后面增加 @- 来实现倒序排列
- ul>li.item$@3*5 使用 @N 指定开始的序号
- ul>li.item$@-3*5 生成以 3 为底倒序列表

###  添加文本内容快捷语法（{}）
- a[href="www.baidu.com" title="It is a blog"]{猛击这里} 生成有可点击内容“猛击这里”的标签

###  隐式标签
- 隐式标签表示 Emmet 可以省略某些标签名，例如，声明一个带类的div，只需输入.item，就会生成<div class="item"></div>。另外，Emmet 还会根据父标签进行判定，例如，在中输入ul>.item$*5

- li：用于 ul 和 ol 中
- tr：用于 table、tbody、thead 和 tfoot 中
- td：用于 tr 中
- option：用于 select 和 optgroup 中

### 书写时不要有空格

### HTML 简写规则简单总结
1. E 代表HTML标签。
2. E#id 代表id属性。
3. E.class 代表class属性。
4. E[attr=foo] 代表某一个特定属性。
5. E{foo} 代表标签包含的内容是foo。
6. E>N 代表N是E的子元素。
7. E+N 代表N是E的同级元素。
8. E^N 代表N是E的上级元素。
