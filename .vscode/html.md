# HTML 常见元素和理解
前端三大件：HTML结构，CSS样式，JS行为
HTML常见元素和理解，版本，元素分类，嵌套关系，默认样式和定制化
常见元素：
meta title style link script base相关信息
div(框框）/section/article/aside/header/footer(标题h+数字)(区域）
p(段落）
span/em(默认斜体）/strong（粗体）(行)
table/thead/tbody/tr(单元行）/td（单元格）(表格）
列表ul（无序）/ol(有序）li
dl/dt（内容）/dd（标题0（定义列表）
a(链接）
表单form/input（输入框）/select（下拉框）/textarea（输入区）/buton（按钮）
charset(字符集）viewpoint(适配移动端）
元素[属性]
a[href(链接地址）,target（默认当前窗口)(-blank新窗口）]
img(图片）[scr（地址）,alt（替换资源)(文字）]
table td（表格）[colspan（行）,rowspan（列）]
form（表单）[target（提交到哪里）,method（get用何方式提交）,enctype（何编码提交）]
input（输入框)[type,value]
button(按钮）[type]
select>option[value]（下拉框）
lable（与表单项关联）[for]（用于单选框和复选框，文字和框同效果）
# 如何理解HTML
'文档'，结构，有区块和大纲
文档：大纲（注意HTML的结构）
版本：HTML4基于标记语言（SGML）
XHTML(XML)(所有的属性必须小写，规则复杂)
HTML5(规范)（标签允许不结束,属性不用带引号，标签的属性可大写可以不带属性)
新增：新区块标签section，article(区域块，可带标题内容)(出现在大纲)
nav（导航）(出现在大纲）  aside(不出现在大纲）
如何更语义化的页面
表达增强：日期，时间，搜索
表单验证（通过属性控制范围）
placehoder自动聚焦（当页面自动加载的时候，光标自动再输入框）
header/footer(头尾)
section包含的内容琐碎,简单/article包含的项目多（区域）
em(默认斜体）/strong（粗体）/取代样式的加粗
i icon(图标)
# HTML元素的分类
按默认样式分类：
块级block（默认占据整行,可指定宽高)[div section article aside p h+数字 ol ul dl table address form blockquote]
行内inline（没有规则的形状，在一行的某个地方，宽高由内容决定）[和文本相关的元素a span i em strong lable var cide code]
inline—block（内联块级元素）（对内表现为有形状，有尺寸。对外表现为额可以和其他元素在同以行）[主要是表单元素：下拉框，输入框img input]
按内容分
flow在文档流中有影响的元素大部分可见的元素
heading标题h+数字（1-6）
sectioning主要是分区的元素和导航元素[section article aside header footer][nav]
interactive有互动的元素（与用户有交互，用户点击链接跳走）[a audio button embed iframe img input keygen label object select textarea video]
phrasing短语[ em]一般是inline元素
embedded嵌入的其它的资源
metadata表示信息的元素[ base link meta script style title]
# HTML元素嵌套关系
1.块级元素可以包含行内元素
2.块级元素不一定能包含块级元素[ 例如p段落不能包含div元素]
3.“行内元素一般不能包含块级元素”
4.不一般情况：为什么a包含div是合法的？实际是不合法的，对分类经行了重新界定
判断嵌套是否合法：一是使用工具验证 二是查文档，看该元素属于什么类型，它的content model是什么，看被嵌套的元素是否属于它的content model，如果属于就可以嵌套，反之不可。
补充：能否嵌套看content model，它的content model属于哪一个内容分类，去该内容分类找相应的元素
# HTML元素的默认样式
1.默认样式的意义（简单便捷)
2.默认样式带来的问题（例如：表单的美化）
3.CSS Reset(重置)
HTML是有样式的，默认的样式不需要，引入CSS Reset，经行重置