# 前端开发

## 前端开发语言

* HTML 超文本标记语言 --- 结构

* CSS 层叠样式表 ------------ 样式

* JS(JavaScript) --------------- 行为

| 标准 | 说明                                                         |
| ---- | ------------------------------------------------------------ |
| 结构 | 结构用于对网页元素进行整理的分类，主要是HTML                 |
| 表现 | 表现用于设置网页元素的版式、颜色、大小等外观样式，主要指的是CSS |
| 行为 | 行为是指网页模型的定义及交互的编写，主要是Javascript         |

Web标准提出的最佳体验方案：结构、样式、行为相分离。

结构写到HTML文件中，表现写到CSS文件中，行为写到JavaScript文件中。

----

## HTML超文本标记语言

`<` 标记      `<html>` 标签     `<html> </html>` 标签对 

大多数为双标签，极少数为单标签，如换行标签`<br />` 。

标签的关系：<u>包含关系</u>和<u>并列关系</u> 



### HTML基本结构标签

```html
<html>
    <head>
        <title>第一个页面</title>
    </head>
    <body>
        这是我的第一个页面
    </body>
</html>
```

| 标签名            | 定义       | 说明                                                   |
| ----------------- | ---------- | ------------------------------------------------------ |
| `<html></html>`   | HTML标签   | 页面中最大的标签，根标签                               |
| `<head></head>`   | 文档的头部 | 在head标签中我们必须设置的标签是title                  |
| `<title></title>` | 文档的标题 | 让页面拥有一个属于自己的网页标题                       |
| `<body></body>`   | 文档的主体 | 元素包含文档的所有内容，页面内容基本都是放到body里面的 |

在vscode里可采用输入!或者tab键生成大体框架。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我用vscode创建的第一个页面</title>
</head>
<body>
    我的页面创建出来啦
</body>
</html>
```

`<!DOCTYPE>` 文档类型的声明标签，用来告诉浏览器使用哪种HTML版本显示网页。（要写在最前面）。

`<html lang="en">` 用来定义当前文档的显示语言，`en` 定义为英语，`zh-CH` 定义为中文。

`<meta charset="UTF-8">`UTF-8为万国码，防止乱码情况，一定要写。



### HTML常用标签

#### 标题标签`<h1>`-`<h6>`

```html
<h1>我是一级标题</h1>
```

h是单词head的缩写，意为头部、标题。

<u>标签语义</u>:作为标题使用，并且依据重要性递减。

<u>特点</u>:标题文字会较大较粗，独占一行。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>标题一共六级选</h1>
    <h2>文字加粗一行选</h2>
    <h3>由大到小依次减</h3>
    <h4>从重到轻随之变</h4>
    <h5>语法规范书写后</h5>
    <h6>具体效果刷新见</h6>
</body>
</html>
```



#### 段落和换行标签

 ```html
<p>我是一个段落标签</p>
 ```

<u>标签语义</u>：可以把HTML文档分割为若干段落。

<u>特点</u>：文本在一个段落会根据浏览器窗口大小自行换行。段落与段落之间有空隙。

```html
<br />
```

单词break的缩写，意为打断、换行。

<u>标签语义</u>：强制换行。

<u>特点</u>：`<br />` 是个单标签。`<br />` 只是简单的开始新的一行，跟段落不一样，不会有间隙。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>这是第一段的第一句，<br />这是第一段的第二句。</p>
    <p>这是第二段。</p>>
</body>
</html>
```



 #### 文本格式化标签

文本文字中 **粗体** , *斜体* ，<u>下划线</u>  等效果。

<u>标签语义</u>：突出重要性，比普通文字更重要。

| 语义   | 标签                             |
| ------ | -------------------------------- |
| 加粗   | `<strong></strong>`或者`<b></b>` |
| 倾斜   | `<em></em>`或者`<i></i>`         |
| 删除线 | `<del></del>`或者`<s></s>`       |
| 下划线 | `<ins></ins>`或者`<u></u>`       |

tips:更推荐`<strong>`,`<em>`,`<del>`,`<ins>`语义更强烈。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    我是<strong>加粗</strong>的文字<br />
    我是<em>倾斜</em>的文字<br />
    我是<del>删除线</del>的文字<br />
    我是<ins>下划线</ins>的文字<br />
</body>
</html>
```



#### `<div>`和`<span>`标签

`<div>`和`<span>`是没有语义的，它们是一个盒子，用来装内容。

```html
<div>这是头部</div>
<span>今日价格</span>
```

div是division的缩写，表示分割、分区。span意为跨度、跨距。

div独占一行（大盒子），span一行可以放多个（小盒子）。



#### 图像标签和路径

在HTML标签中，`<img>`标签用于定义HTML页面中的图像。

```html
<img src="图像URL"/>
```

`<img>`是<u>单标签</u>，是单词image的缩写，意为图像。

**src**是`<img>` 标签的必须属性，用于指定图像文件的路径和文件名。

图像标签的其他属性：

| 属性   | 属性值   | 说明                                 |
| ------ | -------- | ------------------------------------ |
| src    | 图片路径 | 必须属性                             |
| alt    | 文本     | 替换文本，图片不能显示的文字         |
| title  | 文本     | 提示文本，鼠标放到图像上，显示的文字 |
| width  | 像素     | 设置图像的宽度                       |
| height | 像素     | 设置图像的高度                       |
| border | 像素     | 设置图像的边框粗细                   |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h4>图像标签的使用：</h4>
    <img src="img.jpg">
    <h4>alt替换文本 图像显示不出来的时候用文字替换</h4>
    <img src="img1.jpg" alt="图片加载失败"/>
    <h4>title提示文本，鼠标放到图像上面会提示文字</h4>
    <img src="img.jpg" title="这里是图像上提示文字"/>
    <h4>width给图片设定宽度</h4>
    <img src="img.jpg" title="这里是图像上提示文字" width="500"/>
    <h4>height给图片设定高度</h4>
    <img src="img.jpg" title="这里是图像上提示文字" height="200"/>
    <h4>border给图片设定边框</h4>
    <img src="img.jpg" title="这里是图像上提示文字" width="500" border="5"/>
</body>
</html>
```

* 宽度、高度设定一般仅修改一个。

* 图像标签可以拥有多个属性，必须写在标签名后面。

* 属性之间部分先后顺序，用空格隔开，属性=“属性值”。

<u>相对路径</u>：以引用文件所在位置为参考基础，而建立出的目录路径。简单来说，图片相对于HTML页面的位置。

| 相对路径分类 | 符号 | 说明                                                         |
| ------------ | ---- | ------------------------------------------------------------ |
| 同一级路径   |      | 图片文件位于HTML文件同一级                                   |
| 下一级路径   | /    | 图片文件位于HTML文件下一级                                   |
| 上一级路径   | ../  | 图片文件位于HTML文件上一级，如`<img src="../img.jpg">`，需要先通过`../`返回到上一级 |

<u>绝对路径</u>:是指目录下的绝对位置，直接到达目标位置，通常是从盘符开始的路径。

<u>相对路径`/`，绝对路径`\`。</u> 



#### 超链接标签

`<a>`标签用于定义超链接，作用是从一个页面连接到另一个页面。

```html
<a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像</a>
```

| 属性   | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| href   | 用于指定连接目标的url地址，（必须属性）当为标签应用href属性时，它就具有了超链接的功能。 |
| target | 用于指定链接页面的打开方式，其中`_self`为默认值，`_blank`为在新窗口中打开方式。 |

**链接的分类**：

1. 外部链接，例如：

   ```html
   <a href="http://www.baidu.com">百度</a>
   ```

2. 内部链接：网站内部页面之间的相互链接，直接链接内部页面名称即可，例如：

   ```html
   <a href="index.html">首页</a>
   ```

3. 空链接：如果当时没有确定链接目标时，

   ```html
   <a href="#">首页</a>
   ```

4. 下载链接：如果href里面地址是一个`.exe`文件或者`.zip`压缩包，会下载这个文件。

   ```html
   <a href="ysb.zip">下载文件</a>
   ```

5. 网页元素链接：在网页中的各种网页元素，如文本、图像、表格、音频、视频都可以添加超链接。

   ```html
   <a href="http://www.baidu.com"><img src="img.jpg"></a>
   ```

6. 锚点链接：点击链接，可以快速定位到页面中的某个位置。

   ```html
   <a href="#two">第2集</a>
   <h3 id="two">第2集介绍</h3>
   ```



### HTML中注释和特殊字符

#### 注释

HTML中的注释以`<!--`开头，以`-->`结束。快捷键：`ctrl + /`。

#### 特殊字符

| 特殊字符 | 描述   | 字符的代码 |
| -------- | ------ | ---------- |
|          | 空格符 | `&nbsp;`   |
| &lt;     | 小于号 | `&lt;`     |
| &gt;     | 大于号 | `&gt;`     |
| &amp;    | 和号   | `&amp;`    |



### HTML其他标签

#### 表格标签

表格主要用于显示，展示数据。

```html
<table>
    <tr>
        <td>单元格内的文字</td>
    </tr>
</table>
```

`<table></table>`用于定义表格的标签。

`<tr></tr>`用于定义表格中的行，必须嵌套在`<table></table>` 标签中。

`<td></td>`用于定义表格中的单元格，必须嵌套在`<tr></tr>`标签中。



##### 表头单元格标签

`<th>`标签表示HTML表格的表头部分。

`<th>`与`<td>`不同于，表头单元格内的文本内容会加粗居中显示。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <table>
        <tr>   <th>学号</th>  <th>姓名</th>  <th>性别</th></tr>
        <tr>   <td>001</td>    <td>方灿</td>  <td>男</td></tr>
    </table>
</body>
</html>
```



##### 表格属性 

表格标签这部分属性我们实际开发并不常用，后面通过CSS来设置。

| 属性名      | 属性值              | 描述                                             |
| ----------- | ------------------- | ------------------------------------------------ |
| align       | left、center、right | 规定表格相对周围元素的对齐方式                   |
| border      | 1或“”               | 规定表格单元是否拥有边框，默认为“”，表示没有边框 |
| cellpadding | 像素值              | 规定单元边沿与其内容之间的空白，默认1像素        |
| cellspacing | 像素值              | 规定单元格之间的空白，默认2像素                  |
| width       | 像素值或百分比      | 规定表格的宽度                                   |

```html
<table align="center" border="1" cellpadding="10" cellspacing="0">
        <tr>   <th>学号</th>  <th>姓名</th>  <th>性别</th></tr>
        <tr>   <td>001</td>   <td>方灿</td>  <td>男</td></tr>
    </table>
```



#####表格结构标签

`<thead>`标签：表格的头部区域，`<tbody>`标签：表格的主体区域。



#####合并单元格

合并单元格方式：

* 跨行合并：rowspan="合并单元格的个数"。上侧单元格为目标单元格，写合并代码。
* 跨列合并：colspan="合并单元格的个数"。左侧单元格为目标单元格，写合并代码。



#### 列表标签

列表是用来布局的。

列表分为三大类：无序列表、有序列表和自定义列表。



##### 无序列表

`<ul>`标签表示HTML页面中项目的无序列表，一般会以项目符号呈现列表项，而列表项使用`<li>`标签定义。

```html
<ul>
    <li>列表项1</li>
    <li>列表项2</li>
    <li>列表项3</li>
</ul>
```



##### 有序列表

`<ol>`标签表示HTML页面中项目的有序列表，列表排序以数字来显示，而列表项使用`<li>`标签定义。



##### 自定义列表

自定义列表经常用于对术语或名词进行解释和描述，定义列表的列表项前没有任何项目符号。

`<dl>`标签用于定义描述列表，该标签会与`<dt>`（定义项目/名字）和`<dd>`（描述每一个项目/名字）一起使用。

```html
<dl>
    <dt>关注我们</dt>
    <dd>新浪微博</dd>
    <dd>官方微信</dd>
</dl>
```



#### 表单标签

使用表单是为了收集用户信息。

在HTML中，一个完整的表单是由<u>表单域</u>、<u>表单控件（表单元素）</u>和<u>提示信息</u>组成。



##### 表单域

表单域是一个包含表单元素的区域。

在HTML标签中，`<form>`标签用于定义表单域，实现用户信息的收集和传递。

<u>`<form>`会把它范围内的表单元素信息提交给服务器。</u>

```html
<form action="url地址" method="提交方式" name="表单域名称">
    各种表单元素控件
</form>
```

常用属性：

| 属性   | 属性值   | 作用                                               |
| ------ | -------- | -------------------------------------------------- |
| action | url地址  | 用于指定接收并处理表单数据的服务器程序的url地址    |
| method | get/post | 用于设置表单数据的提交方式，其取值为get或者post    |
| name   | 名称     | 用于指定表单的名称，以区分同一个页面中的多个表单域 |



##### 表单控件（表单元素）

`<input>`<u>单标签</u>用于收集用户信息。

```html
<input type="属性值" />
```

在`<input>`标签中，包含一个type属性，根据不同的type属性值，输入字段拥有很多形式。

| 属性值   | 描述                                                 |
| -------- | ---------------------------------------------------- |
| button   | 可点击按钮（多数情况下，用于通过JavaScript启动脚本） |
| checkbox | 复选框                                               |
| file     | 输入字段和浏览按钮，供文件上传                       |
| hidden   | 隐藏的输入字段                                       |
| image    | 图像形式的提交按钮                                   |
| password | 密码字段                                             |
| radio    | 单选按钮                                             |
| reset    | 重置按钮                                             |
| submit   | 提交按钮，会把表单数据发送到服务器                   |
| text     | 输入字段，默认宽度20                                 |

`<input>`除了type属性外还有很多其他属性：

| 属性      | 属性值     | 描述                                |
| --------- | ---------- | ----------------------------------- |
| name      | 用户自定义 | 定义input元素名称                   |
| value     | 用户自定义 | 规定input元素的值                   |
| checked   | checked    | 规定此input元素首次加载时应当被选中 |
| maxlength | 正整数     | 规定输入字段中字符的最大长度        |

name和value是每个表单元素都有的属性值，主要给后台人员使用。

name是每个表单元素的名字，<u>要求单选按钮和复选按钮要有相同的name值</u>，用于区分不同的表单元素。

value可以使某些表单元素刚打开就默认显示几个文字。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Input 表单元素</title>
</head>
<body>
    <form>
        <!-- text 文本框 -->
        用户名：<input type="text" name="username" value="请输入用户名" maxlength="6"> <br>
        
        <!-- password 密码框 -->
        密码：<input type="password" name="pwd"> <br>
        
        <!-- radio 单选按钮 可以实现多选一 -->
        <!-- name 是表单元素名字 这里性别单选按钮必须有相同的名字name 才可以实现多选一 -->
        <!-- 单选框和复选框可以设置checked属性，当页面打开的时候就可以默认选中这个按钮 -->
        性别：男<input type="radio" name="sex" value="男" checked="checked"> 女<input type="radio" name="sex" value="女"> <br>
        
        <!-- checkbox 复选框 可以多选 -->
        爱好：吃饭<input type="checkbox"> 睡觉<input type="checkbox"> 打豆豆<input type="checkbox"> <br>
        
        <input type="submit" value="免费注册">
        <input type="reset" value="重新输入">
        
        <!-- button 普通按钮 后期搭配js使用 -->
        <input type="button" value="获取短信验证码"><br>
        
        <!-- 文件域 使用场景 上传文件使用的 -->
        上传头像：<input type="file">
        
    </form>
</body>
```


##### `<label>`标签 

`<label>`标签为input元素定义标注（标签）。

`<label>`标签用于绑定一个表单元素，当点击`<label>`标签的文本时，浏览器会自动将焦点（光标）转到或者选择对应的表单元素上，用来增加用户体验。

```html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex" />
```


-----

## CSS
