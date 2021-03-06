# HTML

## 常用浏览器内核

| 浏览器       | 内核    |
| ------------ | ------- |
| IE           | Trident |
| firfox       | Gecko   |
| Safari       | Webkit  |
| chrome/Opera | Bink    |

## HTML常用标签

### 标题标签  < h1/> -< h6 >

```html
<h1>标题一共六级选,</h1> 
<h2>文字加粗一行显。</h2> 
<h3>由大到小依次减，</h3> 
<h4>从重到轻随之变。</h4> 
<h5>语法规范书写后，</h5> 
<h6>具体效果刷新见。</h6> 
```



### 段落和换行标签

```html
 <p> 我是一个段落标签 </p> //段落标签
```

```html
 <br /> //换行标签
```

### 文本格式化标签

| 语义   | 标签                              |
| ------ | --------------------------------- |
| 加粗   | < strong>< /strong>  or < b>< /b> |
| 倾斜   | < em>< /em> or < i>< /i>          |
| 删除线 | < del>< /del> or < s>< /s>        |
| 下划线 | < ins>< /ins> or < u>< /u>        |

这几个标签都更推荐使用前者 语义更为强烈

###   < div > 和< span >标签   

**特点：**

​	1.< div>标签用来布局，是块级元素一行只能放一个

​	2.< span>标签用来布局，一行可放多个

### 图像标签

```
<img src="图像URL" /> 
```

图像标签的其他属性：

| 属性   | 属性值 | 说明                                 |
| ------ | ------ | ------------------------------------ |
| src    | 路径   | 必须要的属性                         |
| alt    | 文本   | 替换文本，图片不能显示时候出现的文字 |
| title  | 文本   | 提示文本，鼠标放上面时候显示的文字   |
| width  | 像素   | 宽                                   |
| height | 像素   | 长                                   |
| border | 像素   | 边框                                 |

这些属性可以连起来写没有顺序属性和属性之间要用空格隔开，采用键值对的写法如下：

```
<img src="图片路径" alt="替换文本" title="提示文本" width="宽度" height="高度" border="1px">
```

**重点：**

alt和title的区别, 前者是替换文本，图片不能显示时候出现的文字，后者是提示文本，鼠标放上面时候显示的文字。

### 超链接标签< a >

```html
 <a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像 </a> 
```

跳转目标为空时可以用#代替

**href和target属性：**

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| href   | 用于指定目标的url地址，为空时可用#替代                       |
| target | 用于打开链接的方式，其中 _ __self为默认值， ___blank为在新窗口打开。 |

#### 锚点链接

点击锚点链接时快速定位到网页中的该位置

使用方法：

```html
<a href="#two"> 第2集 </a>  //设置锚点链接
<h3 id="two">第2集介绍</h3> //设置跳转的位置通过id=two
```

### 表格标签

表格的基本语法：

```html
 <table> //tabel定义表格的标签必须有
   <tr> //表示行 有几组tr就有几行
     <td>单元格内的文字</td> //表示单元格，有几组td就代表每一行中有几个格子(tabel data的缩写)
     ... 
   </tr> 
   ... 
 </table>
```

通常表格的第一行使用表头标签

```
<table> 
   <tr> 
     <th>姓名</th> 
     <th>性别</th>
     <th>电话</th>
   </tr> 
   ... 
 </table>
```

表头单元格也是单元格, 常用于表格第一行, 突出重要性, 表头单元格里面的文字会加粗居中显示. 

#### 合并单元格

跨行合并：rowspan="合并单元格的个数" 

跨列合并：colspan="合并单元格的个数"

**合并单元格的三个步骤：**

1.先确定是跨行还是跨列合并。 

2.找到目标单元格. 写上合并方式 = 合并的单元格数量。比如：< td colspan="2">< /td>。 

3.删除多余的单元格。 

### 列表标签

#### 无序列表

基本语法格式：

```
 <ul> 
   <li>列表项1</li> 
   <li>列表项2</li> 
   <li>列表项3</li> 
   ... 
 </ul>
```

#### 有序列表

基本语法格式：

```
 <ol> 
   <li>列表项1</li> 
   <li>列表项2</li> 
   <li>列表项3</li> 
   ... 
 </ol> 
```

#### 自定义列表

使用场景：

常用对术语或名字进行解释和描述如下图

关注我们下面有三个途径，相当于对上面的名词进行解释

![](H:\前端笔记\img\Snipaste_2020-07-10_13-46-58.png)

### 表单标签

#### 表单域

在 HTML 标签中， < form> 标签用于定义表单域，以实现用户信息的收集和传递。 

就是把网页中被< form> 标签包含的数据传递给后端的

```
 <form action=“url地址” method=“提交方式” name=“表单域名称"> 
   各种表单元素控件 
 </form> 
```

| 属性   | 属性值   | 作用                                        |
| ------ | -------- | ------------------------------------------- |
| action | url地址  | 用于接受处理表单数据的服务器程序的url地址。 |
| method | get/post | 用于设置表单数据的提交方式，get/post        |
| name   | 名称     | 用于表单的命名                              |

#### < input >表单元素

在英文单词中，input 是输入的意思，而在表单元素中 < input> 标签用于收集用户信息。 

```
 <input type="属性值"  /> 
```

**type中的属性值：**

| 属性值   | 描述                                  |
| -------- | ------------------------------------- |
| button   | 点击按钮，大多数通过js启动脚本        |
| checkbox | 定义复选框                            |
| file     | 文件上传                              |
| hidden   | 定义隐藏的输入字段                    |
| image    | 定义图像形式的提交按钮                |
| password | 定义密码字段，看不见的* * * *类似这样 |
| radio    | 定义单选按钮                          |
| reset    | 定义重置按钮，重置表单中所有数据      |
| submit   | 定义提交按钮，点击后把数据发给服务器  |
| text     | 定义单行输入字段，默认20个字符        |

除了type还有很多属性：

| 属性      | 属性值   | 描述                   |
| --------- | -------- | ---------------------- |
| name      | 用户定义 | input元素名称          |
| value     | 用户定义 | input元素的值          |
| maxlength | 正整数   | 输入字符最大长度       |
| checked   | checked  | 该元素首次加载时被选中 |

**注意：**

radio (或者checkbox）如果是一组，我们必须给他们命名相同的名字   

使用radio单选按钮时必须设置相同的名字name 才能实现多选1。

```html
 <input type="radio" name="sex"  />男 
 <input type="radio" name="sex" />女 
```

**有些表单元素想刚打开页面就默认显示几个文字怎么做?** 

答: 可以给这些表单元素设置 value 属性=“值”

```html
 用户名: <input type="text"  value="请输入用户名" />  
```

**页面中的表单元素很多，如何区别不同的表单元素?**

答:  name 属性：当前 input 表单的名字，后台可以通过这个 name 属性找到这个表单。页面中的表单很多， name 的主要作用就是用于区别不同的表单。  

```html
 用户名: <input type="text"  value="请输入用户名" name="username" /> 
```

 **如果页面一打开就让某个单选按钮或者复选框是选中状态?** 

答: checked 属性：表示默认选中状态。用于单选按钮和复选按钮。 

```html
 性    别: 
 <input type="radio" name="sex" value="男" checked="checked" />男 //默认选择的就是男的
 <input type="radio" name="sex" value="女" />女 
```

```html
性    别: 
 <input type="radio" name="sex" value="男"/>男 
 <input type="radio" name="sex" value="女" checked="checked"/>女 //默认选择的就是女的的
```

**如何让input表单元素展示不同的形态? 比如单选按钮或者文本框** 

答: type属性：type属性可以让input表单元素设置不同的形态. 

#### < label>标签

< label> 标签为 input 元素定义标注（标签）。 
< label> 标签用于绑定一个表单元素, 当点击< label> 标签内的文本时，浏览器就会自动将焦点(光标)转到或者 选择对应的表单元素上,用来增加用户体验. 

比如以下场景可以使用：

![](H:\前端笔记\img\Snipaste_2020-07-10_14-18-24.png)

当我点击那个图片时候也能选中那个小圆圈，以免用户手抖点不到，增加用户体验

语法：

```html
 <label for="sex">男</label> 
 <input type="radio" name="sex"  id="sex" /> 
```

**核心： < label> 标签的 for 属性应当与相关元素的 id 属性相同。** 

里面可以时文字也可以时图片，就是< label>标签中间可以插入图片或者文字，一样可以实现该效果

####  < select> 表单元素 

使用场景: 在页面中，如果有多个选项让用户选择，并且想要节约页面空间时，我们可以使用< select>标签控件定义下 拉列表

语法：

```html
 <select> 
   <option>选项1</option> 
   <option>选项2</option> 
   <option>选项3</option> 
   ... 
 </select>
```

1.< select> 中至少包含一对< option> 。

2.在< option> 中定义 selected =“ selected " 时，当前项即为默认选中项 

```
 <select> 
   <option selected="selected">选项1</option> 
   <option>选项2</option> 
   <option>选项3</option> 
   ... 
 </select>
```

 <select> 
   <option selected="selected">选项1</option> 
   <option>选项2</option> 
   <option>选项3</option> 
   ... 
 </select>

就会有上面这个效果，默认选中了选项1

### < textarea> 表单元素 

使用场景: 当用户输入内容较多的情况下，我们就不能使用文本框表单了，此时我们可以使用 < textarea> 标签。 
在表单元素中，< textarea> 标签是用于定义多行文本输入的控件。 
使用多行文本输入控件，可以输入更多的文字，该控件常见于留言板，评论。 

语法：

```html
<textarea rows="3" cols="20"> 
   文本内容 
 </textarea> 
```

<textarea rows="3" cols="20"> 
   文本内容可以输入3行，每行字符数为20 
 </textarea> 

1. 通过 < textarea> 标签可以轻松地创建多行文本输入框。 
2. cols=“每行中的字符数” ，rows=“显示的行数”，我们在实际开发中不会使用，都是用 CSS 来改变大小。 

# HTML5

### H5新增语义化标签 

- `header`   ---  头部标签

- `nav`        ---  导航标签

- `article` ---   内容标签

- `section` ---   块级标签

- `aside`     ---   侧边栏标签

- `footer`   ---   尾部标签

  ![](H:\前端笔记\img\Snipaste_2020-07-19_12-04-31.png)

  使用语义化标签的注意

  - 语义化标签主要针对搜索引擎
  - 新标签可以使用一次或者多次
  - 在 `IE9` 浏览器中，需要把语义化标签都转换为块级元素
  - 语义化标签，在移动端支持比较友好，
  - 另外，`HTML5` 新增的了很多的语义化标签，随着课程深入，还会学习到其他的

### H5新增多媒体标签 

1.  多媒体标签有两个，分别是

    - 音频  -- `audio`
    - 视频  -- `video`

2.  `audio` 标签说明

    - 可以在不使用标签的情况下，也能够原生的支持音频格式文件的播放，
    - 但是：播放格式是有限的

3.  audio 支持的音频格式

    - audio 目前支持三种格式

audio 代码演示：

```html
 <audio src="文件地址" controls="controls"></audio> 
 < audio controls="controls"  > 
 <source src="happy.mp3" type="audio/mpeg" > 
 <source src="happy.ogg" type="audio/ogg" >  您的浏览器暂不支持audio标签。  
 </ audio> 
```



# CSS

## css引用方式

### 内部样式表

内部样式表（内嵌样式表）是写到html页面内部. 是将所有的 CSS 代码抽取出来，单独放到一个 <style> 标签中。 

语法：

```css
 <style> 
    div { 
      color: red; 
      font-size: 12px; 
    } 
 </style>
```

 1.< style> 标签理论上可以放在 HTML 文档的任何地方，但一般会放在文档的<head>标签中 
 2.通过此种方式，可以方便控制当前整个页面中的元素样式设置 
 3.代码结构清晰，但是并没有实现结构与样式完全分离 
 4.使用内部样式表设定 CSS，通常也被称为嵌入式引入，这种方式是我们练习时常用的方式 

### 行内样式表 

行内样式表（内联样式表）是在元素标签内部的 style 属性中设定 CSS 样式。适合于修改简单样式. 

语法：

```
<div style="color: red; font-size: 12px;">青春不常在，抓紧谈恋爱</div> 
```

 1.style 其实就是标签的属性 
 2.在双引号中间，写法要符合 CSS 规范 
 3.可以控制当前的标签设置样式 
 4.由于书写繁琐，并且没有体现出结构与样式相分离的思想，只有对当前元素添加简 单样式的时候，可以考虑使用 
 5.使用行内样式表设定 CSS，通常也被称为行内式引入 

### 外部样式表

实际开发都是外部样式表. 适合于样式比较多的情况. 核心是:样式单独写到CSS 文件中，之后把CSS文件引入 到 HTML 页面中使用. 

引入外部样式表分为两步： 

1.新建一个后缀名为 .css 的样式文件，把所有 CSS 代码都放入此文件中。 

2.在 HTML 页面中，使用<link> 标签引入这个文件

```
<link rel="stylesheet"  href="css文件路径"> 
```

| 属性 | 作用                                                         |
| ---- | ------------------------------------------------------------ |
| rel  | 定义当前文档于被链接文档之间的关系，在这里指定为‘’stylesheet‘，表示被链接的文档是一个样式表文件 |
| href | 定义链接外部样式表的文件的URL，也就是路径。                  |



## css基础选择器

基础选择器是由单个选择器组成的 

基础选择器又包括：`标签选择器`、`类选择器`、`id 选择器`和`通配符选择器` 

### 标签选择器

标签选择器（元素选择器）是指用 HTML 标签名称作为选择器，按标签名称分类，为页面中某一类标签指定 统一的 CSS 样式。 

语法：

```
 标签名{ 
    属性1: 属性值1;  
    属性2: 属性值2;  
    属性3: 属性值3;  
    ... 
 } 
```

### 类选择器 

语法：

```
.类名 {     属性1: 属性值1;   
    ... 
 } 
```

例如将所有的red类的背景全部填充为红色

```css
  .red {
        background-color: red;
    }
```

结构需要用class属性来调用

```html
 <div class=‘red’> 变红色 </div> 
```

**命名注意事项：**

① 类选择器使用“.”（英文点号）进行标识，后面紧跟类名（自定义，我们自己命名的）。 
② 可以理解为给这个标签起了一个名字，来表示。 
③ 长名称或词组可以使用中横线来为选择器命名。 
④ 不要使用纯数字、中文等命名，尽量使用英文字母来表示。 
⑤ 命名要有意义，尽量使别人一眼就知道这个类名的目的。 
⑥ 命名规范：见附件（ Web 前端开发规范手册.doc） 

**多类名的使用语法：**

```html
 <div class="red font20">亚瑟</div> 
```

(1) 在标签class 属性中写 多个类名 
(2) 多个类名中间必须用空格分开 
(3) 这个标签就可以分别具有这些类名的样式 

### id选择器

id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。 
HTML 元素以 id 属性来设置 id 选择器，CSS 中 id 选择器以“#" 来定义。 

语法：

```css
 #id名 {     属性1: 属性值1;   
    ... 
 } 
```

例如，将 id 为 nav 元素中的内容设置为红色。 

```css
 #nav { 
   color:red; 
 }
```

**id 选择器和类选择器的区别** 
① 类选择器（class）好比人的名字，一个人可以有多个名字，同时一个名字也可以被多个人使用。 
② id 选择器好比人的身份证号码，全中国是唯一的，不得重复。 
③ id 选择器和类选择器最大的不同在于使用次数上。 
④ 类选择器在修改样式中用的最多，id 选择器一般用于页面**唯一性**的元素上，经常和 JavaScript 搭配使用。 

### 通配符选择器

在 CSS 中，通配符选择器使用“*”定义，它表示选取页面中所有元素（标签）。 

语法：

```
 * {  
    属性1: 属性值1;       ...  
    }
```

例如清楚全局的内外边距：

```css
* {
        margin: 0;
        padding: 0;       
    } 
```

## css复合选择器

### 后代选择器

后代选择器又称为包含选择器，可以选择父元素里面子元素。其写法就是把外层标签写在前面，内层标签写在 后面，中间用空格分隔。当标签发生嵌套时，内层标签就成为外层标签的后代

语法：

```
元素1 元素2 { 样式声明 } 
```

上述语法表示选择元素 1 里面的所有元素 2 (后代元素)

```
ul li {
	样式声明 /*  选择 ul 里面所有的 li标签元素  */ 
}
```

### 子选择器

子元素选择器（子选择器）只能选择作为某元素的最近一级子元素。简单理解就是选亲儿子元素. 

语法：

```
元素1 > 元素2 { 样式声明 } 
```

上述语法表示选择元素1 里面的所有直接后代(子元素) 元素2。 

```
div > p { 样式声明 }  /*  选择 div 里面所有最近一级 p 标签元素  */  
```

**注意：**

子选择器选择的是他的直接的第一代后代也就是说

元素2 必须是**亲儿子**，其孙子、重孙之类都不归他管. 你也可以叫他 亲儿子选择器 

### 并集选择器

并集选择器可以选择多组标签, 同时为他们定义相同的样式。通常用于集体声明. 
并集选择器是各选择器通过英文逗号（,）连接而成，任何形式的选择器都可以作为并集选择器的一部分。 

```
元素1,元素2 { 样式声明 } 
```

上述语法表示选择元素1 和 元素2。 

###  链接伪类选择器 

语法：

```css
 /* a 是标签选择器  所有的链接 */  
  a {        
   color: gray; 
  } 
  /* :hover 是链接伪类选择器 鼠标经过 */ 
  a:hover {     
   color: red;  /* 鼠标经过的时候，由原来的 灰色 变成了红色 */ 
  }
```

```css
a:link /* 选择没有点击过的链接 */
a:visited /* 选择点击过或访问过的链接 */
a:hover	 /* 选择鼠标经过的链接 */
a:active /* 选择的是鼠标正在按下没弹起的链接 */
```

###  :focus 伪类选择器 

:focus 伪类选择器用于选取获得焦点的表单元素。 
焦点就是光标，一般情况 <input> 类表单元素才能获取，因此这个选择器也主要针对于表单元素来说。 

语法：

```css
input:focus {  
   background-color:yellow; /*选择的是获得光标的input表单元素 */
 }
```



## css字体属性

### 字体系列

CSS 使用 font-family 属性定义文本的字体系列。  

语法：

```css
 p { font-family:"微软雅黑";}      
 div {font-family: Arial,"Microsoft Yahei", "微软雅黑";} 
```

**注意事项：**

1.各种字体之间必须使用英文状态下的逗号隔开 

2.一般情况下,如果有空格隔开的多个单词组成的字体,加引号. 

3.尽量使用系统默认自带字体，保证在任何用户的浏览器中都能正确显示 

4.最常见的几个字体：body {font-family: 'Microsoft YaHei',tahoma,arial,'Hiragino Sans GB'; } 

### 字体大小

CSS 使用 font-size 属性定义字体大小。  

语法：

```css
 p {   
    font-size: 20px;  
 }
```

### 字体粗细

CSS 使用 font-weight 属性设置文本字体的粗细。

语法：

```
 p {   
    font-weight: 400;  //400为不加粗，700为加粗
 }
```

**注意：**

后面不加单位

### 文字样式

CSS 使用 font-style 属性设置文本的风格。 

语法：

```css
 p {   
    font-style: normal; 
 }
```

| 属性值 | 作用                 |
| ------ | -------------------- |
| normal | 默认值标准的字体样式 |
| italic | 斜体                 |

注意： 平时我们很少给文字加斜体，反而要给斜体标签（em，i）改为不倾斜字体

### 字体复合属性

语法：

```css
 body {  
  font: font-style  font-weight  font-size/line-height  font-family; 
}
```

**注意事项：**

1.使用 font 属性时，必须按上面语法格式中的顺序书写，不能更换顺序，并且各个属性间以空格隔开 

2.不需要设置的属性可以省略（取默认值），但必须保留 font-size 和 font-family 属性，否则 font 属性将不起作用 

复合写法比较麻烦个人感觉

## css文本属性

### 文本颜色

语法：

```
 div {  
   color: red; 
 } 
```

### 对齐文本

text-align 属性用于设置元素内文本内容的水平对齐方式

```
 div {  
   text-align: center; //center居中，left左对齐（默认），right右对齐。
 } 
```

### 装饰文本

text-decoration 属性规定添加到文本的修饰。可以给文本添加下划线、删除线、上划线等

语法：

```css
 div {  
   text-decoration：underline； 
 }
```

| 属性         | 描述                                    |
| ------------ | --------------------------------------- |
| none         | 默认，啥都没（常用于给a链接去掉下划线） |
| underline    | 下划线                                  |
| overline     | 上划线                                  |
| line-through | 删除线                                  |

### 文本缩进

text-indent 属性用来指定文本的第一行的缩进，通常是将段落的首行缩进。

语法：

```
 div {  
   text-indent: 10px; 
 } 
```

通过设置该属性，所有元素的第一行都可以缩进一个给定的长度，甚至该长度可以是负值

```
 p {  
   text-indent: 2em; //相当于首行缩进两个字符
 }
```

em 是一个相对单位，就是当前元素（font-size) 1 个文字的大小, 如果当前元素没有设置大小，则会按照父元 素的 1 个文字大小

### 行高

line-height 属性用于设置行间的距离（行高）。可以控制文字行与行之间的距离

```
 p {  
   line-height: 26px; 
 } 
```

行间距

**CSS 没有给我们提供文字垂直居中的代码.  这里我们可以使用一个小技巧来实现.**  
解决方案:    让文字的行高等于盒子的高度  就可以让文字在当前盒子内垂直居中 

简单理解:  行高的上空隙和下空隙把文字挤到中间了.  是如果**行高小于盒子高度,文字会偏上,如果行高大于盒子高度,则文字偏下** 

如下图所示：

css<img src="H:\前端笔记\img\Snipaste_2020-07-10_20-50-19.png" style="zoom: 67%;" />



##  css 的元素显示模式 

### 什么是元素显示模式 

元素显示模式就是元素（标签）以什么方式进行显示，比如< div>自己占一行，比如一行可以放多个< span>。 

HTML 元素一般分为块元素和行内元素两种类型。

### 块元素

常见的块元素有< h1>~< h6>、< p>、< div>、< ul>、< ol>、< li>等，其中 < div> 标签是最典型的块元素

块级元素的特点： 
① 比较霸道，自己独占一行。 
② 高度，宽度、外边距以及内边距都可以控制。 
③ 宽度默认是容器（父级宽度）的100%。 
④ 是一个容器及盒子，里面可以放行内或者块级元素

**注意：** 

1.文字类的元素内不能使用块级元素 

2.< p> 标签主要用于存放文字，因此 < p> 里面不能放块级元素，特别是不能放< div>

3.同理， < h1>~< h6>等都是文字类块级标签，里面也不能放其他块级元素 

### 行内元素

常见的行内元素有 < a>、< strong>、< b>、< em>、< i>、< del>、< s>、< ins>、< u>、< span>等，其中 < span> 标签是最典型的行内元素。有的地方也将行内元素称为内联元素。 

**行内元素的特点：** 
① 相邻行内元素在一行上，一行可以显示多个。 
② 高、宽直接设置是无效的。 
③ 默认宽度就是它本身内容的宽度。 
④ 行内元素只能容纳文本或其他行内元素。 

**注意：**

1. 链接里面不能再放链接 
2. 特殊情况链接 < a> 里面可以放块级元素，但是给 < a> 转换一下块级模式最安全 

### 行内块元素

在行内元素中有几个特殊的标签 —— <img />、<input />、<td>，它们同时具有块元素和行内元素的特点。 有些资料称它们为行内块元素。 

**行内块元素的特点：** 
① 和相邻行内元素（行内块）在一行上，但是他们之间会有空白缝隙。一行可以显示多个（行内元素特点）。 
② 默认宽度就是它本身内容的宽度（行内元素特点）。 
③ 高度，行高、外边距以及内边距都可以控制（块级元素特点）。 

### 元素显示模式的总结

| 元素模式   | 元素排列       | 设置样式   | 默认宽度       | 包含                                       |
| ---------- | -------------- | ---------- | -------------- | ------------------------------------------ |
| 块级元素   | 一行只能有一个 | 可设置宽高 | 容器的100%     | 容器级的可包含任何标签（文字类元素不能放） |
| 行内元素   | 一行可以多个   | 不可设置宽 | 它本身内容宽高 | 容纳文本或其他行内元素                     |
| 行内块元素 | 一行可以多个   | 可设置宽   | 它本身内容宽高 |                                            |

### 元素模式的转换

特殊情况下，我们需要元素模式的转换，简单理解: 一个模式的元素需要另外一种模式的特性 
比如想要增加链接 <a> 的触发范围。 

```css
display:block; /*转换为块元素：*/
display:inline/*转换为行内元素*/
display: inline-block; /*转换为行内块*/
```

## css背景

### 背景颜色

background-color 属性定义了元素的背景颜色

```css
background-color:颜色值; 
```

 一般情况下元素背景颜色默认值是 transparent（透明），我们也可以手动指定背景颜色为透明色。 

###  背景图片 

background-image 属性描述了元素的背景图像。实际开发常见于 logo 或者一些装饰性的小图片或者是超 大的背景图片, 优点是非常便于控制位置. (精灵图也是一种运用场景) 

```css
background-image : none | url (url) 
```

 

| 参数值 | 作用             |
| ------ | ---------------- |
| none   | 无背景图（默认） |
| url    | 写背景图像的地址 |

注意：背景图片后面的地址，千万不要忘记加 URL， 同时里面的路径不要加引号。 

### 背景平铺

如果需要在 HTML 页面上对背景图像进行平铺，可以使用 background-repeat 属性。 

```
 background-repeat: repeat | no-repeat | repeat-x | repeat-y   
```

| 参数值    | 作用                         |
| --------- | ---------------------------- |
| repeat    | （默认的）在纵向和横向上平铺 |
| no-repeat | 不平铺                       |
| repeat-x  | 横向平铺                     |
| repeat-y  | 纵向平铺                     |

###  背景图片位置 

 利用 background-position 属性可以改变图片在背景中的位置。 

```css
 background-position: x  y; 
```

参数代表的意思是：x 坐标和 y 坐标。 可以使用 方位名词 或者 精确单位 

| 参数值   | 说明                                      |
| -------- | ----------------------------------------- |
| 精确单位 | 百分数\| 由浮点数和单位标识符组成的长度值 |
| 方位名词 | top\|center\|bottom\|left\|center\|right  |

1.参数是方位名词 

​	如果指定的两个值都是方位名词，则两个值前后顺序无关，比如 left  top 和 top  left 效果一致 

​	如果只指定了一个方位名词，另一个值省略，则第二个值默认居中对齐 

 2.参数是精确单位

​	如果参数值是精确坐标，那么第一个肯定是 x 坐标，第二个一定是 y 坐标 

​	如果只指定一个数值，那该数值一定是 x 坐标，另一个默认垂直居中 

3.参数是混合单位

​	如果指定的两个值是精确单位和方位名词混合使用，则第一个值是 x 坐标，第二个值是 y 坐标 

###  背景图像固定（背景附着） 

background-attachment 属性设置背景图像是否固定或者随着页面的其余部分滚动

background-attachment 后期可以制作视差滚动的效果。 

```css
 background-attachment : scroll | fixed 
```

| 参数   | 作用                           |
| ------ | ------------------------------ |
| scroll | 背景图像随对象内容滚动（默认） |
| fixed  | 背景图像固定                   |

### 背景复合写法 

为了简化背景属性的代码，我们可以将这些属性合并简写在同一个属性 background 中。从而节约代码量. 
当使用简写属性时，**没有特定的书写顺序**,一般习惯约定顺序为： 
background: 背景颜色 背景图片地址 背景平铺 背景图像滚动 背景图片位置; 

```css
background: transparent url(image.jpg) repeat-y  fixed  top ; 
```

###  背景色半透明 

```css
background: rgba(0, 0, 0, 0.3); 
```

最后一个参数是 alpha 透明度，取值范围在 0~1之间 

## css三大特性

### 层叠性

层叠性原则：

1.样式冲突，遵循就近原则，哪个样式离结构近就执行哪个

2.样式不冲突就不层叠

### 继承性

字标签会继承父标签的某些样式，如文字颜色，字号

可以继承的有（text- ，font- ，line-这些元素开头的可以继承，以及color属性）

行高的继承：

行高可以不加单位，就是子元素的x倍

```css
body{
font:12px/1.5/*文字大小的1.5倍*/
}
```

### 优先级

选择器相同执行层叠性

选择器不同按权重执行

| 选择器               | 选择器权重 |
| -------------------- | ---------- |
| 继承或者*            | 0，0，0，0 |
| 元素选择器           | 0，0，0，1 |
| 类选择器，伪类选择器 | 0，0，1，0 |
| ID选择器             | 0，1，0，0 |
| 行内样式“style”      | 1，0，0，0 |
| ！important重要的    | 无穷打     |

优先级注意点：

1.权重由4组数据组成，但**不会进位**

2.可理解为类选择器永远大于元素选择器，以此类推

3.等级判断从左向右

**权重叠加：**如果是复合选择器有权重叠加问题，需要计算

## css盒子模型

### 边框（border） 

border可以设置元素的边框。边框有三部分组成:边框宽度(粗细) 边框样式  边框颜色 

语法：

```css
 border : border-width || border-style || border-color
```

| 属性         | 作用     |
| ------------ | -------- |
| border-width | 边框粗细 |
| border-style | 边框样式 |
| border-color | 边框颜色 |

**边框样式 border-style 可以设置如下值：** 

1.none：没有边框即忽略所有边框的宽度（默认值）

2.solid：边框为单实线(最为常用的) 

3.dashed：边框为虚线   

4.dotted：边框为点线 

CSS 边框属性允许你指定一个元素边框的样式和颜色。

语法：

```css
 border-top: 1px solid red;  /* 只设定上边框， 其余同理,  属性没有顺序 */ 
```

### 表格合并边框

border-collapse 属性控制浏览器绘制表格边框的方式。它控制相邻单元格的边框。 

```css
 border-collapse:collapse;  
```

collapse 单词是合并的意思 

### 边框会影响盒子实际大小 

边框会额外增加盒子的实际大小。因此我们有三种方案解决: 

1.测量盒子大小的时候,不量边框. 

2.如果测量的时候包含了边框,则需要 width/height 减去边框宽度 

**3.采用css中的box-sizing来指定和模型box- sizing:border-box**（常用）

## 内边距（padding） 

语法：

```css
pading-left|ringht|top|bottom/*左内边距|右内边距|上内边距|下内边距*/
```

padding 属性（简写属性）可以有一到四个值

| 值得个数                    | 表达意思                                    |
| --------------------------- | ------------------------------------------- |
| padding:5px;                | 上下左右5像素内边距                         |
| padding:5px 10px;           | 上下5像素，左右10像素内边距                 |
| padding:5px 10px 20px;      | 上5像素，左右10像素，下20像素内边距         |
| padding:5px 10px 20px 30px; | 上5像素，右10像素，下20像素，左30像素内边距 |

顺时针得正方形

**当我们给盒子指定 padding 值之后，发生了 2 件事情：** 

1.内容和边框有了距离，添加了内边距。 

2.padding影响了盒子实际大小。 也就是说，如果盒子已经有了宽度和高度，此时再指定内边框，会撑大盒子

**解决方案：** 

如果保证盒子跟效果图大小保持一致，则让 width/height 减去多出来的内边距大小即可。 

**padding影响盒子也有好处**

padding内边距可以撑开盒子,我们可以做非常巧妙的运用. 因为每个导航栏里面的字数不一样多,我们可以不用给每个盒子宽度了,直接给padding最合适. 

![](H:\前端笔记\img\Snipaste_2020-07-12_10-18-13.png)

## 外边距（margin） 

margin 属性用于设置外边距，即控制盒子和盒子之间的距离。 写法和padding类似

外边距可以让块级盒子水平居中，但是必须满足两个条件： 

① 盒子必须指定了宽度（width）。 
② 盒子左右的外边距都设置为 auto 

语法：

```css
 .header{ 
 		width:960px;
 		margin:0 auto;
 			} 
```

**注意：以上方法是让块级元素水平居中，行内元素或者行内块元素水平居中给其父元素添加 text-align:center 即可**

### 外边距合并

使用 margin 定义块元素的垂直外边距时，可能会出现外边距的合并。 
主要有两种情况: 

**1.相邻块元素垂直外边距的合并** 

当上下相邻的两个块元素（兄弟关系）相遇时，如果上面的元素有下外边距 margin-bottom，下面的元素有 上外边距 margin-top ，则他们之间的垂直间距不是 margin-bottom 与 margin-top 之和。**取两个值中的 较大者**这种现象被称为相邻块元素垂直外边距的合并。 

**解决方案：** 
尽量只给一个盒子添加 margin 值。 

**2.嵌套块元素垂直外边距的塌陷** 

对于两个嵌套关系（父子关系）的块元素，父元素有上外边距同时子元素也有上外边距，此时父元素会塌陷较大的外边距值。 

就是父元素有一个30px的上外边距，子元素也有一个40px的上外边距，就会发生父元素的上外边距变为40px，而子元素的上外边距为0px没变化

**解决方案：**

① 可以为父元素定义上边框。 
② 可以为父元素定义上内边距。 
③ 可以为父元素添加 overflow:hidden

还有其他方法，比如浮动、固定，绝对定位的盒子不会有塌陷问题。

### 清除内外边距 

网页元素很多都带有默认的内外边距，而且不同浏览器默认的也不一致。因此我们在布局前，首先要清除下网 页元素的内外边距。 

语法：

```css
 * { 
    padding:0;   /* 清除内边距 */ 
    margin:0;    /* 清除外边距 */ 
   list-style: none; /*去掉 li 前面的 项目符号(小圆点) */
  }
```

注意：行内元素为了照顾兼容性，尽量只设置左右内外边距，不要设置上下内外边距。但是转换为块级和行内 块元素就可以了 

###  圆角边框 

在 CSS3 中，新增了圆角边框样式，这样我们的盒子就可以变圆角了。 border-radius 属性用于设置元素的外边框圆角。 

```css
 border-radius:length;   
```

参数值可以为数值或百分比的形式 

1.如果是正方形，想要设置为一个圆，把数值修改为高度或者宽度的一半即可，或者直接写为 50% 
2.该属性是一个简写属性，可以跟四个值，分别代表左上角、右上角、右下角、左下角 

3.分开写：border-top-left-radius、border-top-right-radius、border-bottom-right-radius 和 border-bottom-left-radius 

4.兼容性 ie9+ 浏览器支持, 但是不会影响页面布局,可以放心使用.

### 盒子阴影 

CSS3 中新增了盒子阴影，我们可以使用 box-shadow 属性为盒子添加阴影。 

语法：

```css
 box-shadow: h-shadow v-shadow blur spread color inset; 
```

| 值       | 描述                         |
| -------- | ---------------------------- |
| h-shadow | 必须，水平阴影位置，可为负   |
| v-shadow | 必须，垂直平阴影位置，可为负 |
| blur     | 可选，模糊距离               |
| spread   | 可选，阴影的尺寸             |
| color    | 可选，阴影颜色               |
| inset    | 可选，外部阴影和内部阴影     |

注意： 

1.默认的是外阴影(outset), 但是不可以写这个单词,否则造成阴影无效 

2.盒子阴影不占用空间，不会影响其他盒子排列。 

### 文字阴影 

在 CSS3 中，我们可以使用 text-shadow 属性将阴影应用于文本

语法：

```css
 text-shadow: h-shadow v-shadow blur color; 
```

里面属性意思参考盒子阴影的

## css浮动

### 传统网页布局的三种方式 

CSS 提供了三种传统布局方式(简单说,就是盒子如何进行排列顺序)： 

1. 普通流（标准流） 
2.  浮动 
3. 定位 

### 标准流（普通流/文档流） 

所谓的标准流:  就是标签按照规定好默认方式排列

1. 块级元素会独占一行，从上向下顺序排列。 
2.  行内元素会按照顺序，从左到右顺序排列，碰到父元素边缘则自动换行。

**注意：实际开发中，一个页面基本都包含了这三种布局方式（后面移动端学习新的布局方式）** 

### **什么是浮动？ **

float 属性用于创建浮动框，将其移动到一边，直到左边缘或右边缘触及包含块或另一个浮动框的边缘。 

语法：

```css
选择器 { float: 属性值; } 
```

| 属性值 | 描述           |
| ------ | -------------- |
| none   | 不浮动（默认） |
| left   | 左浮           |
| right  | 右浮           |

###  浮动特性（重难点） 

设置了浮动（float）的元素最重要特性： 
1. 脱离标准普通流的控制（浮）  移动到指定位置（动）, （俗称脱标） 
2. 浮动的盒子不再保留原先的位置 

设置了浮动的元素就相当于飘起来了，不保留原来的位置

![](H:\前端笔记\img\Snipaste_2020-07-12_10-58-29.png)

**如果多个盒子都设置了浮动，则它们会按照属性值一行内显示并且顶端对齐排列**

![](H:\前端笔记\img\Snipaste_2020-07-12_10-59-25.png)

**注意： 浮动的元素是互相贴靠在一起的（不会有缝隙），如果父级宽度装不下这些浮动的盒子， 多出的盒子 会另起一行对齐。** 

3. 浮动元素会具有行内块元素特性

任何元素都可以浮动。不管原先是什么模式的元素，添加浮动之后具有行内块元素相似的特性。 
1 如果块级盒子没有设置宽度，默认宽度和父级一样宽，但是添加浮动后，它的大小根据内容来决定 
2 浮动的盒子中间是没有缝隙的，是紧挨着一起的 
3 行内元素同理 

**为了约束浮动元素位置, 我们网页布局一般采取的策略是:**
**先用标准流的父元素排列上下位置, 之后内部子元素采取浮动排列左右位置.  符合网页布局第一准侧.**

![](\img\Snipaste_2020-07-12_11-02-05.png)

**注意事项：**

**浮动的盒子只会影响浮动盒子后面的标准流,不会影响前面的标准流.** 

**浮动的盒子只会影响浮动盒子后面的标准流,不会影响前面的标准流.** 

**浮动的盒子只会影响浮动盒子后面的标准流,不会影响前面的标准流.** 

重要事情说三遍

### 清除浮动 

##### 为什么需要清除浮动？

由于父级盒子很多情况下，不方便给高度，但是子盒子浮动又不占有位置，最后父级盒子高度为 0 时，就会 影响下面的标准流盒子。 

![](H:\前端笔记\img\Snipaste_2020-07-12_11-12-15.png)

#####  清除浮动本质 

1. 清除浮动的本质是清除浮动元素造成的影响 
2.  如果父盒子本身有高度，则不需要清除浮动 
3. 清除浮动之后，父级就会根据浮动的子盒子自动检测高度。父级有了高度，就不会影响下面的标准流了 

语法：

```css
选择器{
	clear:both|right|left;
} 
```



##### 清除浮动 —— 额外标签法 

额外标签法也称为隔墙法，是 W3C 推荐的做法。 
额外标签法会在**最后一个浮动的盒子**添加一个空的标签。例如 < div style="clear:both">< /div>，或者其他标签 （如< br />等）。 

注意： 要求这个新的空标签必须是**块级元素**

优点： 通俗易懂，书写方便 

缺点： 添加许多无意义的标签，结构化较差 

##### 清除浮动 —— 父级添加 overflow 

可以给父级添加 overflow 属性，将其属性值设置为 hidden、 auto 或 scroll 。 
子不教,父之过,注意是给父元素添加代码 

优点：代码简洁 

缺点：无法显示溢出的部分 

##### 清除浮动 —— :after 伪元素法 

:after 方式是额外标签法的升级版。也是给父元素添加 

语法：

```css
 .clearfix:after {   
   content: "";  //伪元素必须写对的属性
   display: block;  //插入的伪元素必须为块级元素，但是生成的伪元素是行内元素所以转化下
   height: 0;  //不要看见这元素
   clear: both;  //核心代码清除浮动
   visibility: hidden;   //不要看见这个元素
 }  
 .clearfix {   专有为了兼容性 */  
   *zoom: 1; 
 }
```

优点：没有增加标签，结构更简单 

##### 清除浮动 —— 双伪元素清除浮动 

也是给父元素添加 

语法：

```css
 .clearfix:before,.clearfix:after { 
   content:""; 
   display:table;  
 } 
 .clearfix:after { 
   clear:both; 
 } 
 .clearfix { 
    *zoom:1; 
 } 
```

## CSS定位

### 定位组成 

定位：将盒子定在某一个位置，所以定位也是在摆放盒子， 按照定位的方式移动盒子。  
定位 = 定位模式 + 边偏移 。  
定位模式用于指定一个元素在文档中的定位方式。边偏移则决定了该元素的最终位置。 

定位模式决定元素的定位方式 ，它通过 CSS 的 position 属性来设置，其值可以分为四个： 

| 值       | 语义                         |
| -------- | ---------------------------- |
| static   | 静态定位(默认的就是没有定位) |
| absolute | 绝对定位                     |
| relative | 相对定位                     |
| fixed    | 固定定位                     |

### 相对定位 relative

相对定位是元素在移动位置的时候，是相对于它原来的位置来说的（自恋型）

语法：

```css
选择器 { position: relative; } 
```

相对定位的特点：（务必记住） 
1. 它是相对于自己原来的位置来移动的（移动位置的时候参照点是自己原来的位置）。 
2. 原来在标准流的位置继续占有，后面的盒子仍然以标准流的方式对待它。 
因此，相对定位并没有脱标。它最典型的应用是给绝对定位当爹的。。。 

###  绝对定位 absolute

绝对定位是元素在移动位置的时候，是相对于它祖先元素来说的（拼爹型）。 

语法：

```css
选择器 { position: absolute; } 
```

绝对定位的特点：（务必记住） 
1. 如果没有祖先元素或者祖先元素没有定位，则以浏览器为准定位（Document 文档）。 
2. 如果祖先元素有定位（相对、绝对、固定定位），则以最近一级的有定位祖先元素为参考点移动位置。 
3. **绝对定位不再占有原先的位置。（脱标）** 
所以绝对定位是脱离标准流的。

##### 绝对定位的盒子居中 

加了绝对定位的盒子不能通过 margin:0 auto 水平居中，但是可以通过以下计算方法实现水平和垂直居中。 
① left: 50%;：让盒子的左侧移动到父级元素的水平中心位置。 
② margin-left: -100px;：让盒子向左移动自身宽度的一半。 

#### 子绝父相的由来 

这个“子绝父相”太重要了，是我们学习定位的口诀，是定位中最常用的一种方式这句话的意思是：子级是**绝 对定位**的话，父级要用**相对定位**。 

① 子级绝对定位，不会占有位置，可以放到父盒子里面的任何一个地方，不会影响其他的兄弟盒子。 
② 父盒子需要加定位限制子盒子在父盒子内显示。 
③ 父盒子布局时，需要占有位置，因此父亲只能是相对定位。 
这就是子绝父相的由来，所以相对定位经常用来作为绝对定位的父级。 
总结： 因为父级需要占有位置，因此是相对定位， 子盒子不需要占有位置，则是绝对定位 
当然，子绝父相不是永远不变的，如果父元素不需要占有位置，子绝父绝也会遇到。 

### 固定定位 fixed 

固定定位是元素固定于浏览器可视区的位置。主要使用场景： 可以在浏览器页面滚动时元素的位置不会改变。 
语法：

```css
选择器 { position: fixed; } 
```

固定定位的特点：（务必记住） 
1. 以浏览器的可视窗口为参照点移动元素。 
跟父元素没有任何关系 
**不随滚动条滚动**。 
2. 固定定位不在占有原先的位置。 
固定定位也是**脱标**的，其实固定定位也可以看做是一种特殊的绝对定位。 

**固定定位小技巧：  固定在版心右侧位置。** 

小算法： 
1. 让固定定位的盒子 left: 50%.  走到浏览器可视区（也可以看做版心） 的一半位置。 
2. 让固定定位的盒子 margin-left: 版心宽度的一半距离。  多走 版心宽度的一半位置 
就可以让固定定位的盒子贴着版心右侧对齐了。 

### 粘性定位 sticky（了解） 

粘性定位可以被认为是相对定位和固定定位的混合。 Sticky  粘性的  
语法： 

```css
选择器 { position: sticky; top: 10px; } 
```

粘性定位的特点： 
1. 以浏览器的可视窗口为参照点移动元素（固定定位特点） 
2. 粘性定位占有原先的位置（相对定位特点） 
3. 必须添加 top 、left、right、bottom 其中一个才有效 
跟页面滚动搭配使用。 兼容性较差，IE 不支持。

###  定位叠放次序 z-index 

在使用定位布局时，可能会出现盒子重叠的情况。此时，可以使用 z-index 来控制盒子的前后次序 (z轴) 

语法：

```css
选择器 { z-index: 1; } 
```

1 数值可以是正整数、负整数或 0, 默认是 auto，**数值越大，盒子越靠上** 
2 如果属性值相同，则按照书写顺序，后来居上 
3 数字后面不能加单位 
4 只有定位的盒子才有 z-index 属性 

###  定位的拓展 

**1.定位特殊特性** 
	绝对定位和固定定位也和浮动类似。 

1.行内元素添加绝对或者固定定位，可以直接设置高度和宽度。 

2.块级元素添加绝对或者固定定位，如果不给宽度或者高度，默认大小是内容的大小

**2.脱标的盒子不会触发外边距塌陷** 
浮动元素、绝对定位(固定定位）元素的都不会触发外边距合并的问题。 

**3.绝对定位（固定定位）会完全压住盒子** 

浮动元素不同，只会压住它下面标准流的盒子，但是不会压住下面标准流盒子里面的文字（图片） 
但是绝对定位（固定定位） 会压住下面标准流所有的内容。 
浮动之所以不会压住文字，因为浮动产生的目的最初是为了做文字环绕效果的。 文字会围绕浮动元素 

####  定位的总结 

![](H:\前端笔记\img\Snipaste_2020-07-12_16-30-12.png)

## CSS元素的显示与隐藏 

###  display 属性 

display 属性用于设置一个元素应如何显示。 
 **1.display: none ；隐藏对象** 
 **2.display：block ；除了转换为块级元素之外，同时还有显示元素的意思** 

重点：

**display 隐藏元素后，不再占有原来的位置。** 
后面应用及其广泛，搭配 JS 可以做很多的网页特效。 

###  visibility 可见性 

visibility 属性用于指定一个元素应可见还是隐藏。 

语法：

```
 visibility：visible ;  /*元素可视*/
 visibility：hidden ;  /*元素不可视*/
```

**visibility 隐藏元素后，继续占有原来的位置。** 

如果隐藏元素想要原来位置， 就用 visibility：hidden 
如果隐藏元素不想要原来位置， 就用 display：none  (用处更多 重点） 

###  overflow 溢出 

overflow 属性指定了如果内容溢出一个元素的框（超过其指定高度及宽度） 时，会发生什么。 

| 属性值  | 描述                                   |
| ------- | -------------------------------------- |
| visible | 不剪切内容也不添加滚动条               |
| hidden  | 不显示超出对象尺寸的内容，超出部分隐藏 |
| scroll  | 不管超出内容否，总显示滚动条           |
| auto    | 超出自动显示滚动条，不超出不显示滚动条 |

一般情况下，我们都不想让溢出的内容显示出来，因为溢出的部分会影响布局。 
但是如果有定位的盒子， 请慎用overflow:hidden  因为它会隐藏多余的部分。 

## css高级技巧

### 精灵图

#####  为什么需要精灵图 

一个网页中往往会应用很多小的背景图像作为修饰，当网页中的图像过多时，服务器就会频繁地接收和发送 请求图片，造成服务器请求压力过大，这将大大降低页面的加载速度。 
因此，为了有效地减少服务器接收和发送请求的次数，提高页面的加载速度，出现了 CSS 精灵技术（也称 CSS Sprites、CSS 雪碧）。 
核心原理：将网页中的一些小背景图像整合到一张大图中 ，这样服务器只需要一次请求就可以了。 

##### 精灵图（sprites）的使用 

使用精灵图核心： 
1. 精灵技术主要针对于背景图片使用。就是把多个小背景图片整合到一张大图片中。 
2. 这个大图片也称为 sprites  精灵图  或者 雪碧图 
3. 移动背景图片位置， 此时可以使用 background-position 。 
4. 移动的距离就是这个目标图片的 x 和 y 坐标。注意网页中的坐标有所不同 
5. 因为一般情况下都是往上往左移动，所以数值是负值。 
6. 使用精灵图的时候需要精确测量，每个小背景图片的大小和位置。 

使用精灵图核心总结： 
1. 精灵图主要针对于小的背景图片使用。 
2. 主要借助于背景位置来实现---background-position 。 
3. 一般情况下精灵图都是负值。（千万注意网页中的坐标： **x轴右边走是正值，左边走是负值， y轴同理**。） 

```css
.sprite {
	background: url('imgs/sprite.png') no-repeat -120px -307px;
	width: 32px;
	height: 32px;
}
```

### 字体图标

####  字体图标的产生 

字体图标使用场景：  主要用于显示网页中通用、常用的一些小图标。 

精灵图是有诸多优点的，但是缺点很明显。 
1. 图片文件还是比较大的。 
2. 图片本身放大和缩小会失真。 
3. 一旦图片制作完毕想要更换非常复杂。 

此时，有一种技术的出现很好的解决了以上问题，就是**字体图标 iconfont**。 
字体图标可以为前端工程师提供一种方便高效的图标使用方式，展示的是图标，本质属于字体。 

####  字体图标的优点 

 1.轻量级：一个图标字体要比一系列的图像要小。一旦字体加载了，图标就会马上渲染出来，减少了服务器请求 
 2.灵活性：本质其实是文字，可以很随意的改变颜色、产生阴影、透明效果、旋转等 
 3.兼容性：几乎支持所有的浏览器，请放心使用 
注意： 字体图标不能替代精灵技术，只是对工作中图标部分技术的提升和优化。 

#### 字体图标的下载 

1. icomoon 字库  http://icomoon.io 
2. 阿里 iconfont 字库   http://www.iconfont.cn/ 

###  CSS 三角 

```css
  div {
            width: 0;
            height: 0;
            border: 10px solid ;
            border-top-color: royalblue;
            border-bottom-color: red;
            border-left-color: pink;
            border-right-color: green;

        }
```

![](H:\前端笔记\img\Snipaste_2020-07-19_10-25-01.png)

想要哪个方向的三角形就把另外三条边框颜色设置为透明

#### 直角三角形的做法

```css
width: 0; 
height: 0; 
border-color: transparent red transparent transparent; 
border-style: solid; 
border-width: 22px 8px 0 0; 
```



###  CSS 用户界面样式 

#### 什么是界面样式 

所谓的界面样式，就是更改一些用户操作样式，以便提高更好的用户体验。 

1. 更改用户的鼠标样式  
2.  表单轮廓 
3. 防止表单域拖拽

#### 鼠标样式 cursor 

```css
 li {cursor: pointer; } 
```

设置或检索在对象上移动的鼠标指针采用何种系统预定义的光标形状。 

| 属性值      | 描述          |
| ----------- | ------------- |
| default     | 小白箭头 默认 |
| pointer     | 小手          |
| move        | 移动          |
| text        | 文本          |
| not-allpwed | 禁止          |

#### 表单轮廓线outline 

 给表单添加 outline: 0;   或者  outline: none; 样式之后，就可以去掉默认的蓝色边框。 

```css
 input {outline: none; } 
```

### vertical-align 属性应用 

CSS 的 vertical-align 属性使用场景： 经常用于设置图片或者表单(行内块元素）和文字垂直对齐。 
官方解释： 用于设置一个元素的垂直对齐方式，但是它只针对于**行内元素**或者**行内块元素**有效。 

```css
 vertical-align : baseline | top | middle | bottom 
```

| 值       | 描述                                               |
| -------- | -------------------------------------------------- |
| baseline | 默认，元素放置在父元素的基线上（基线对齐）         |
| top      | 把元素的顶端与行中最高元素的顶端对齐（顶线对齐）   |
| middle   | 把此元素放置在父元素的中部（中线对齐）             |
| bottom   | 把元素的顶端与行中最低的元素的顶端对齐（底线对齐） |

![](H:\前端笔记\img\Snipaste_2020-07-19_10-46-16.png)

####  解决图片底部默认空白缝隙问题 

图片底侧会有一个空白缝隙，原因是行内块元素会和文字的基线对齐

主要解决方法有两种： 
1. 给图片添加 vertical-align:middle | top| bottom 等只要不是基线对齐就不会出现这个情况。 （提倡使用的） 
2. 把图片转换为块级元素  display: block

#### 溢出的文字省略号显示 

##### 1. 单行文本溢出显示省略号--必须满足三个条件 

```css
/*1. 先强制一行内显示文本*/    
white-space: nowrap;  （ 默认 normal 自动换行）   
/*2. 超出的部分隐藏*/    
overflow: hidden;   
/*3. 文字用省略号替代超出的部分*/    
text-overflow: ellipsis;
```

##### 2. 多行文本溢出显示省略号 

多行文本溢出显示省略号，有较大兼容性问题， 适合于webKit浏览器或移动端（移动端大部分是webkit内 核） 

```css
overflow: hidden; 
text-overflow: ellipsis; 
/* 弹性伸缩盒子模型显示 */ 
display: -webkit-box; 
/* 限制在一个块元素显示的文本的行数 */ 
-webkit-line-clamp: 2; 
/* 设置或检索伸缩盒对象的子元素的排列方式 */ 
-webkit-box-orient: vertical; 
```

### 常见布局技巧

#### 1. margin负值运用 

![](H:\前端笔记\img\Snipaste_2020-07-19_10-57-48.png)

1.让每个盒子margin 往左侧移动 -1px 正好压住相邻盒子边框 

2.鼠标经过某个盒子的时候，提高当前盒子的层级即可（如果没有有定位，则加相对定位（保留位置），如 果有定位，则加z-index） 

#### 2. 文字围绕浮动元素 

![](H:\前端笔记\img\Snipaste_2020-07-19_11-01-04.png)

**巧妙运用浮动元素不会压住文字的 特性** 

#### 3.行内块巧妙运用 

![](H:\前端笔记\img\Snipaste_2020-07-19_11-02-00.png)

页码在页面中间显示: 

1. 把这些链接盒子转换为行内块， 之后给父级指定  text-align:center; 
2. 利用行内块元素中间有缝隙，并且给父级添加 text-align:center; 行内块元素会水平会居中 