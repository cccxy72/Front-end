# 前端开发

[TOC]



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

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200725223003265.png" alt="image-20200725223003265" style="zoom:67%;" />



##### `<label>`标签 

`<label>`标签为input元素定义标注（标签）。

`<label>`标签用于绑定一个表单元素，当点击`<label>`标签的文本时，浏览器会自动将焦点（光标）转到或者选择对应的表单元素上，用来增加用户体验。

```html
<label for="sex">男</label>
<input type="radio" name="sex" id="sex" />
```

`<label>`标签的for属性应当与相关元素的id属性相同。



##### `<select>`表单元素

我们可以用`<select>`标签控件定义下拉列表。

```html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
</select>
```

`<select>`中至少包含一对`<option>`。

在`<select>`中定义 selected=“selected” 时，当前项即为默认选中项。



##### `<textarea>`表单元素

当输入内容较多时，可以用`<textarea>`文本域标签，可以定义多行文本输入。

```html
<textarea rows="3" cols="20">
    文本内容
</textarea>
```



#### 综合案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>综合案例注册页面</title>
</head>
<body>
    <h4>青春不常在，抓紧学编程</h4>
    <table width="600">
        <!--第一行-->
        <tr>
            <td>性别：</td>
            <td>
                <input type="radio" name="sex" id="man"><label for="man">男</label>&nbsp;
                <input type="radio" name="sex" id="woman"><label for="woman">女</label>
            </td>
        </tr>
        <!--第二行-->
        <tr>
            <td>生日：</td>
            <td>
                <select>
                    <option>--请选择年份--</option>
                    <option>2000</option>
                    <option>2001</option>
                    <option>2002</option>
                    <option>2003</option>
                    <option>2004</option>
                    <option>2005</option>
                </select>
                <select>
                    <option>--请选择月份--</option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                    <option>4</option>
                    <option>5</option>
                    <option>6</option>
                </select>
                <select>
                    <option>--请选择日期--</option>
                    <option>1</option>
                    <option>2</option>
                    <option>3</option>
                    <option>4</option>
                    <option>5</option>
                    <option>6</option>
                </select>
            </td>
        </tr>
        <!--第三行-->
        <tr>
            <td>所在学校</td>
            <td>
                <input type="text" value="请输入在读学校">
            </td>
        </tr>
        <!--第四行-->
        <tr>
            <td>专业：</td>
            <td><input type="radio" name="major" checked="checked" id="jk"><label for="jk">计科</label> 
                <input type="radio" name="major" id="rg"><label for="rg">软工</label> 
                <input type="radio" name="major" id="dsj"><label for="dsj">大数据 </label>
                <input type="radio" name="major" id="wlw"><label for="wlw">物联网</label>
            </td>
        </tr>
        <!--第五行-->
        <tr>
            <td>在读年级:</td>
            <td>
                <input type="text" value="请输入在读年级">
            </td>
        </tr>
        <!--第六行-->
        <tr>
            <td>学习方向：</td>
            <td>
                <input type="checkbox" name="direction" checked="checked">前端开发
                <input type="checkbox" name="direction">人工智能
                <input type="checkbox" name="direction">游戏设计
            </td>
        </tr>
        <!--第七行-->
        <tr>
            <td>个人介绍</td>
            <td>
                <textarea>个人简介</textarea>
            </td>
        </tr>
        <!--第八行-->
        <tr>
            <td></td>
            <td>
                <input type="submit" value="注册">
            </td>
        </tr>
        <!--第九行-->
        <tr>
            <td></td>
            <td>
                <input type="checkbox" checked="checked">我同意注册条款和会员加入标准
            </td>
        </tr>
        <!--第十行-->
        <tr>
            <td></td>
            <td>
                <a href="#">我是会员，立即登录</a>
            </td>
        </tr>
        <!--第十一行-->
        <tr>
            <td></td>
            <td>
                <h5>我承诺</h5>
                <ul>
                    <li>信息属实</li>
                    <li>认真学习</li>
                </ul>
            </td>
        </tr>
    </table>
</body>
</html>
```



-----

## CSS

CSS是层叠样式表的简称。

CSS也是一种标记语言。主要用于设置HTML页面中的文本内容（字体、大小、对齐）、图片的外形（宽高、边框样式、边距等）以及版面的布局和外观显示样式。

由HTML专注去做结构呈现，样式交给CSS，结构（HTML）与样式（CSS）相分离。

<u>CSS规则由两个主要的部分构成：选择器以及一条或多条声明。</u>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS语法规范</title>
    <style>
        /* 选择器{样式} */
        /* 给谁改样式{改什么样式} */
        p {
            color: red;
            /* 修改了文字大小为12像素 */
            font-size: 12px;
        }
    </style>
</head>
<body>
    <p>有点意思</p>
</body>
</html>
```

* 属性和属性值以“键值对”的形式出现
* 属性是对指定的对象设置的样式属性，如字体大小、文本颜色
* 属性和属性值之间用英文“:”分开
* 多个键值对之间用“;”进行区分



### CSS代码风格

样式格式书写：

紧凑格式

```html
h3 { color: deeppink;font-size: 20px;}
```

展开格式

```html
h3 { 
   color: deeppink;
   font-size: 20px;
}
```

样式大小写风格：

选择小写。

样式空格风格：

```html
h3 {
   color: pink;
}
```

* 属性值前面，冒号后面保留一个空格
* 选择器（标签）和大括号中间保留空格



### CSS基础选择器

选择器就是根据不同需求把不同的标签选出来，简单来说就是选择标签用的。

选择器分为<u>基础选择器</u>和<u>复合选择器</u>两个大类。

* 基础选择器是由单个选择器组成的
* 基础选择器又包括：标签选择器、类选择器、id选择器和通配符选择器



#### 标签选择器

标签选择器（元素选择器）是指用HTML标签作为选择器，按标签名称分类，为页面中某一类标签指定统一的CSS样式。

```html
标签名 {
     属性1: 属性值1;
     属性2: 属性值2;
     属性3: 属性值3;
     ···
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>基础选择器之标签选择器</title>
    <style>
        /* 标签选择器 ： 写上标签名 */
        p {
            color: green;
        }
        div {
            color: pink;
        }
    </style>
</head>
<body>
    <p>男生</p>
    <p>男生</p>
    <p>男生</p>
    <div>女生</div>
    <div>女生</div>
    <div>女生</div>
</body>
</html>
```

标签选择器可以把某一类标签全部选择出来，比如所有的`<div>`标签和所有的`<span>`标签。



#### 类选择器

单独选一个或者几个标签，可以使用类选择器。

```html
.类名 {
     属性1: 属性值1;
     ···
}
```

例如，将所有拥有red类的HTML元素均为红色：

```html
.red {
    color: red;
}
```

结构需要用**class属性**来调用class类对的意思。

```html
<div class="red">变红色</div>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>基础选择器之类选择器</title>
    <style>
        /* 类选择器口诀：样式点定义 结构类调用 一个或多个 开发最常用 */
        .red {
            color: red;
        }
    </style>
</head>
<body>
    <ul>
        <li class="red">陈</li>
        <li class="red">写</li>
        <li>意</li>
    </ul>
</body>
</html>
```

* 类选择器使用“.”（英文点号）进行标识，后面紧跟类名（自定义，我们自己命名）
* 长名称或者词组可以使用横线来为选择器命名
* 不要使用纯数字、中文等命名，尽量使用英文字母表示
* 命名要有意义，尽量使别人一眼就知道这个类名的目的

用类选择器设置盒子背景颜色：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>类选择器画三个盒子</title>
    <style>
        .red {
            width: 100px;
            height: 100px;
            background-color: red;
        }
        .green {
            width: 100px;
            height: 100px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div class="red"></div>
    <div class="green"></div>
    <div class="red"></div>
</body>
</html>
```



**类命名规范：**

 头：header 

 内容：content/container

 尾：footer

 导航：nav  

 侧栏：sidebar

 栏目：column

 页面外围控制整体布局宽度：wrapper

 左右中：left right center

 登录条：loginbar

 标志：logo

 广告：banner

 页面主体：main

 热点：hot

 新闻：news

 下载：download

 子导航：subnav

 菜单：menu

 子菜单：submenu

 搜索：search

 友情链接：friendlink

 页脚：footer

 版权：copyright

 滚动：scroll

 内容：content

 标签页：tab

 文章列表：list

 提示信息：msg

 小技巧：tips

 栏目标题：title

 加入：joinus

 指南：guild

 服务：service

 注册：regsiter

 状态：status

 投票：vote

 合作伙伴：partner

**(二)注释的写法:**

 /* Footer */

 内容区

 /* End Footer */

**(三)id的命名:**

 **(1)页面结构**

 容器: container

 页头：header

 内容：content/container

 页面主体：main

 页尾：footer

 导航：nav

 侧栏：sidebar

 栏目：column

 页面外围控制整体布局宽度：wrapper

 左右中：left right center

 **(2)导航**

 导航：nav

 主导航：mainbav

 子导航：subnav

 顶导航：topnav

 边导航：sidebar

 左导航：leftsidebar

 右导航：rightsidebar

 菜单：menu

 子菜单：submenu

 标题: title

 摘要: summary

 **(3)功能**

 标志：logo

 广告：banner

 登陆：login

 登录条：loginbar

 注册：regsiter

 搜索：search

 功能区：shop

 标题：title

 加入：joinus

 状态：status

 按钮：btn

 滚动：scroll

 标签页：tab

 文章列表：list

 提示信息：msg

 当前的: current

 小技巧：tips

 图标: icon

 注释：note

 指南：guild

 服务：service

 热点：hot

 新闻：news

 下载：download

 投票：vote

 合作伙伴：partner

 友情链接：link

 版权：copyright\



**多类名的使用方式：**

```html
<div class="red font20">亚瑟</div>
```

* 在标签class属性中写多个类名
* 多个类名中间必须用空格分开

```html
<html>
    <head>
    <title>多类名的使用方式</title>
    <style>
        .red {
            color: red;
        }
        .font35 {
            font-size: 35px;
        }
    </style>
</head>
<body>
    <div class="red font35">123456</div>
</body>
</html>
```



#### id选择器

id选择器可以为特定id的HTML元素指定特定的样式。

HTML元素以id属性来设置id选择器，CSS中id选择器以`#`来定义。

```tml
#id名 {
    属性1： 属性值1；
    ···
}
```

<u>id选择器口诀：样式#定义，结构id调用，只能调用一次，别人切勿使用</u>

```txt
类选择器好比人的名字昵称，id选择器好比人的身份证号码无重复。
```



#### 通配符选择器

在CSS中，通配符选择器使用`*`定义，它表示选取页面中所有元素（标签）。

```html
* {
  属性1： 属性值1；
  ···
}
```



#### 四种选择器总结

| 基础选择器   | 作用                   | 特点                               | 使用情况     | 用法                 |
| :----------- | ---------------------- | ---------------------------------- | ------------ | -------------------- |
| 标签选择器   | 可以选出所有相同的标签 | 不能差异化选择                     | 较多         | p {color: red;}      |
| 类选择器     | 可以选出1个或多个标签  | 可以根据需求选择                   | 非常多       | .nav {color: red;}   |
| id选择器     | 一次只能选择一个标签   | ID属性只能在每个HTML文档中出现一次 | 一般与JS搭配 | `#`nav {color: red;} |
| 通配符选择器 | 选择所有标签           | 选择的太多，有部分不需要           | 特殊情况使用 | *{color: red;}       |



### CSS字体属性

CSS Fonts（字体）属性用于定义字体系列、大小、粗细、和文字样式（如斜体）。



#### 字体系列

CSS使用font-family属性定义文本的字体系列。

```html
p {
  font-family: "微软雅黑";
}
div {
  font-family: Arial,"Microsoft Yahei","微软雅黑"；
}
```

* 各种字体之间必须用英文状态下的逗号隔开
* 一般情况下，如果有空格隔开的多个但系组成的字体，加引号



#### 字体大小

CSS使用font-size属性定义文字大小。

```html
p {
  font-size: 20px;
}
```

* px（像素）大小是网页常用的单位
* 谷歌浏览器默认的文字大小是16px
* 不同浏览器可能默认显示的字号大小不一致，我们尽量给一个明确值的大小，不要默认大小
* 可以给body指定整个页面文字的大小
* 标题标签比较特殊，需要单独指定文字大小



#### 字体粗细

CSS使用font-weight属性设置文本字体的粗细。

```html
.bold {
     /* font-size:bold */
     /* 700后面不要跟单位 等价于bold 都是加粗的效果 */
     /* 实际开发中更体长用number表示加粗或变细 */
     font-weight： 700;
}
h2 {
     /* 变细可用以下两种 */
     font-weight: 400;
     font-weight: normal;
}
```

| 属性值  | 描述                                         |
| ------- | -------------------------------------------- |
| normal  | 默认值（不加粗的）                           |
| bold    | 定义粗体（加粗的）                           |
| 100-900 | 400等同于normal，700等同于bold，后面不跟单位 |



#### 文字样式

CSS使用font-style属性设置文本的风格。

```html
p {
  font-style: normal;
}
```

| 属性值 | 作用                                                  |
| ------ | ----------------------------------------------------- |
| normal | 默认值，浏览器会显示标准的字体样式font-style: normal; |
| italic | 浏览器会显示*斜体*的字体样式                          |

* 平时很少给文字加斜体，反而要给斜体标签（em,i）改为不倾斜字体



#### 字体复合属性

字体属性可以把以上文字样式综合来写，这样可以更节约代码。

```html
body {
    font: font-style font-weight font-size/line-height font-family;
}
```

```html
<style>
    div {
        font: italic 700 16px 'Microsoft Yahei';
        /* 下面两个不能省略 */
        font:16px 'Microsoft Yahei';
    }
</style>
```

* 使用font属性时，必须按上面语法格式中的顺序书写，不能更换顺序，并且各个属性间以空格隔开
* 不需要设置的属性可以忽略（取默认值），但必须保留font-size和font_family属性，否则font属性将不起作用



### CSS文本属性

CSS Text（文本）属性可以定义文本的外观，比如文本的颜色、对齐文本、装饰文本、文本缩进、行间距等。



#### 文本颜色

color属性用于定义文本的颜色。

```html
div {
   color: red;
}
```

| 表示           | 属性值                 |
| -------------- | ---------------------- |
| 预定义的颜色值 | red，green，blue，pink |
| 十六进制       | `#`FF0000              |
| RGB代码        | rgb(255,0,0)           |



#### 对齐文本

text-align属性用于设置元素内文本内容的水平对齐方式。

```html
div {
   text-align: center;
}
```

| 属性值 | 解释             |
| ------ | ---------------- |
| left   | 左对齐（默认值） |
| right  | 右对齐           |
| center | 居中对齐         |



#### 装饰文本

text-decoration属性规定添加到文本的修饰，可以给文本添加下划线、删除线、上划线等。

```html
div {
    text-decoration: underline;
}
```

| 属性值       | 描述                            |
| ------------ | ------------------------------- |
| none         | 默认。没有装饰线                |
| underline    | 下划线。链接a自带下划线（常用） |
| overline     | 上划线。（几乎不用）            |
| line-through | 删除线。（不常用）              |

链接a去掉下划线：

```html
<html>
    <head>
        <style>
            a {
                text-decoration: none;
            }
        </style>
    </head>
    <body>
        <a href="#">没有下划线的链接</a>
    </body>
</html>
```



#### 文本缩进

text-indent属性用来指定文本的第一行缩进，通常是将段落的首行缩进。

```html
div {
    text-indent: 20px;
}
```

通过设置该属性，所有元素的第一行都可以缩进一个给定的长度，甚至该长度可以是负值。

```html
p {
    text-indent: 2em;
}
```

em是一个相对单位，就是当前元素（font-size）1个文字的大小，如果当前元素没有设置大小，则会按照父元素1个文字大小。



#### 行间距

line-height属性用于设置行间的距离（行高）。可以控制文字行与行之间的距离。

```html
p {
  line-height: 26px;
}
```

![image-20200805230859732](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200805230859732.png)

文本高度已定不变，改变行间距会改变上间距和下间距。

上间距和下间距会一样高。



#### 文本属性总结

| 属性            | 表示     | 注意点                                        |
| --------------- | -------- | --------------------------------------------- |
| color           | 文本颜色 | 通常用 十六进制                               |
| text-align      | 文本对齐 | 可以设定文字水平的对齐方式                    |
| text-indent     | 文本缩进 | 通常用于首航缩进2个字的距离 text-indent: 2em; |
| text-decoration | 文本修饰 | 添加下划线underline，取消下划线none           |
| line-height     | 行高     | 控制行与行之间的距离                          |



### CSS的引入方式

按照CSS样式书写的位置（或者引入的方式），CSS眼视光hi表可以分为三大类：

* 行内样式表（行内式）
* 内部样式表（嵌入式）
* 外部样式表（链接式）



#### CSS内部样式表

内部样式表（内嵌样式表）是写到html页面内部，是将所有的CSS代码抽取出来，单独放到一个`<style>`标签中。

```html
<style>
    div {
        color: red;
        font-size: 12px;
    }
</style>
```

* `<style>`标签理论上可以放在html文档的任何地方，但一般放在文档的`<head>`标签中
* 通过此种方式，可以方便控制当前整个页面中的元素样式设置
* 代码结构清晰，但并没有实现结构与样式完全分离



#### 行内样式表

行内样式表（内联样式表）是元素标签内部的style属性中设定CSS样式。适合于修改简单样式。

```html
<div style="color: red; font-size: 12px;">行列样式表</div>
```

* style其实是标签的属性
* 在双引号中间，写法要符合CSS规范
* 可以控制当前的标签设置样式
* 由于书写繁琐，没有体现出结构与样式分离



#### 外部样式表

实际开发都是外部样式表，适合于样式比较多的情况，核心是：样式单独写到CSS文件中，之后把CSS文件引入到HTML页面中使用。

**引入外部样式表分两步：**

1. 新建一个后缀名为.css的样式文件，把所有CSS代码都放入此文件中。
2. 在HTML页面中，使用`<link>`标签引入这个文件。

```html
<link rel="stylesheet" href="css文件路径">
```

![image-20200806160850409](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806160850409.png)



#### CSS引入方式总结

| 样式表     | 优点                   | 缺点         | 使用情况 | 控制范围     |
| ---------- | ---------------------- | ------------ | -------- | ------------ |
| 行内样式表 | 书写方便，权重高       | 结构样式混写 | 较少     | 控制一个标签 |
| 内部样式表 | 部分结构和样式分离     | 没有彻底分离 | 较多     | 控制一个页面 |
| 外部样式表 | 完全实现结构和样式分离 | 需要引入     | 最多     | 控制多个页面 |



### 综合案例

html文件：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>北方高温明日达鼎盛 京津冀多地地表温度将超60℃</h1>
    <div class="gray">2019-07-03 16:31:47 来源: <a href="#">中国天气网　</a>  
    <input type="text" value="请输入查询条件" class="search">  <button class="btn">搜索</button>
</div>
    <hr>

    <p>中国天气网讯 今天（3日），华北、黄淮多地出现高温天气，截至下午2点，北京、天津、郑州等地气温突破35℃。
    预报显示，今后三天（3-5日），这一带的高温天气将继续发酵，
    高温范围以及强度将在4日达到鼎盛，预计北京、天津、石家庄、济南等地明天的最高气温有望突破38℃，
    其中北京和石家庄的最高气温还有望创今年以来的新高。</p>
    
    <h4>气温41.4℃！地温66.5！北京强势迎七月首个高温日</h4>
    
    <p><img src="image/pic.jpeg" alt=""></p>

    <p>今天，华北、黄淮一带的高温持续发酵，截至今天下午2点，陕西北部、山西西南部、河北南部、北京、天津、
    山东西部、河南北部最高气温已普遍超过35℃。大城市中，北京、天津、郑州均迎来高温日。</p>
    
    <p>在阳光暴晒下，地表温度也逐渐走高。今天下午2点，
    华北黄淮大部地区的地表温度都在50℃以上，部分地区地表温度甚至超过60℃。其中，河北衡水地表温度高达68.3℃，天津站和北京站附近的地表温度分别高达66.6℃和66.5℃。在阳光暴晒下，
    地表温度也逐渐走高。今天下午2点，华北黄淮大部地区的地表温度都在50℃以上，
    部分地区地表温度甚至超过60℃。其中，河北衡水地表温度高达68.3℃，天津站和北京站附近的地表温度分别高达66.6℃和66.5℃。</p>
    
    <h4>明日热度再升级！京津冀携手冲击38℃+</h4>
    
    <p>中国天气网气象分析师王伟跃介绍，明天（4日），华北、黄淮地区35℃以上的高温天气还将继续升级，
    并进入鼎盛阶段，高温强度和范围都将发展到最强。 明天，北京南部、天津大部、河北中部和南部、山东中部和西部、
    山西南部局地、河南北部、东北部分地区的最高气温都将达到或超过35℃。</p>
    
    <p>不过，专家提醒，济南被雨水天气完美绕开，因此未来一周，当地的高温还会天天上岗。
    在此提醒当地居民注意防暑降温，防范持续高温带来的各种不利影响。（文/张慧 数据支持/王伟跃 胡啸 审核/刘文静 张方丽）</p>

    <p class="footer">本文来源：中国天气网 责任编辑：刘京_NO5631</p>
</body>
</html>
```

CSS文件：

```css
body {
    font: 16px/28px 'Microsoft YaHei';

}
h1 {
    font-weight: 400;
    text-align: center;
}
.gray {
    color: #888888;
    font-size: 12px;
    text-align: center;
}
a {
    text-decoration: none;
}
.search {
    color: #666;
    width: 170px;
}
.btn {
    font-weight: 700;
}
p {
    text-indent: 2em;
}
.footer {
    color: #888;
}
```

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806162522602.png" alt="image-20200806162522602" style="zoom:67%;" />



### Chrome调试工具

![image-20200806163118173](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806163118173.png)



### Emmet语法

#### 快速生成HTML结构语法

1. 生成标签 直接输入标签名 按tab键。比如div然后按tab键，就可以生成`<div></div>`
2. 如果想要生成多个相同标签 加上`*`就可以了。比如 div`*`3就可以快速生成3个div
3. 如果有服自己关系的标签，可以用`>`。比如ul`>`li就可以了
4. 如果有兄弟关系的标签，用`+`就可以。比如div+p
5. 如果生成带有类名或者id名字的，直接写`.demo`或者`#two`tab键就可以了
6. 如果生成的div类名是由顺序的，可以用自增符号`$`
7. 如果下能要在生成的标签内部写内容可以用`{}`表示



#### 快速生成CSS样式语法

CSS基本采取简写形式即可

1. 比如`w200 `按tab键，可以生成`width: 200px;`
2. 比如`lh26`按tab键，可以生成`line-height: 26px;`



#### 快速格式化代码

`shift + alt + F`

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806174746557.png" alt="image-20200806174746557"  />



### CSS的复合选择器

常用的复合选择器包括：后代选择器、子选择器、并集选择器、伪类选择器等等。



#### 后代选择器（重要）

后代选择器又称包含选择器，可以选择父元素里面的子元素。其写法就是把外层标签写在前面，内层标签写在后面，中间用空格分割。当标签发生嵌套时，内层标签就成为外层标签的后代。

语法：

```txt
元素1 元素2 { 样式声明 }
```

上述语法表示选择元素1里面的所有元素2（后代元素）。

例如：

```txt
ul li { 样式声明 } /* 选择ul里面所有的li标签元素 */
```

* 元素1和元素2中间**一定要用空格隔开**
* 元素1是父级，元素2是子级，**最终选择是元素2**
* 只要包含在元素1里不管是子级，孙级都可以
* 元素1和元素2可以是任意基础选择器

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806202850766.png" alt="image-20200806202850766" style="zoom:67%;" />

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806202923803.png" alt="image-20200806202923803" style="zoom:67%;" />

![image-20200806202953676](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806202953676.png)



#### 子选择器（重要）

子元素选择器（子选择器）只能选择作为某元素的最近一级子元素。简单理解是选亲儿子元素。

```html
<html>
    <head>
        <title>子元素选择器</title>
        <style>
            .nav>a {
                color: red;
            }
        </style>
    </head>
    <body>
        <div class="nav">
            <a href="#">我是儿子</a>
            <p>
                <a href="#">我是孙子</a>
            </p>
        </div>
    </body>
</html>
```

语法：

```txt
元素1>元素2 { 样式声明 }
```

上述语法表示选择元素1里面的所有直接后代（子元素）元素2。

例如：

```txt
div > p { 样式声明 } /* 选择div里面所有最近一级p标签元素 */
```

* 元素1和元素2中间用**大于号**隔开
* 元素1是父级，元素2是子级，**最终选择的是元素2**
* **只能选择亲儿子**



#### 并集选择器（重要）

并集选择器可以选择多组标签，同时为他们定义相同的样式。通常用于集体声明。

并集选择器是各选择器通过应为逗号`,`连接而成，任何形式的选择器都可以作为并集选择器的一部分。

语法：

```txt
元素1,元素2{ 样式声明 }
```

上述语法表示选择元素1和元素2。

例如：

```html
ul,
div { 样式声明 } 
/* 选择ul 和 div标签元素 */
```

* 元素1和元素2中间用逗号隔开
* 逗号可以理解为和的意思
* **并集选择器竖着写**



#### 伪类选择器

味蕾选择器用于向某些选择器添加特殊的效果，比如给链接添加特殊效果，或者选择第1个，第n个元素。

伪类选择器书写最大的特点是用冒号`:`表示，比如`:hover`。

伪类选择器由很多：链接伪类、结构伪类等，这里讲的是链接伪类选择器。



##### 链接伪类选择器

```html
a:link     /*选择所有未被访问的链接*/
a:visited  /*选择所有已被访问的链接*/
a:hover    /*选择鼠标指针位于其上的链接*/
a:active   /*选择活动链接（鼠标按下未弹起的链接）*/
```

```html
<html>
    <head>
        <title>链接伪类选择器</title>
        <style>
           /* 未访问的链接 a:link */
            a:link {
                color: #333;
                text-decoration: none;
            }
            /* 访问过的链接 a:visited */
            a:visited {
                color: orange;
            }
            /* 鼠标经过的链接 a:hover */
            a:hover {
                color: skyblue;
            }
            /* 鼠标按下还没弹起的链接 a:active */
            a:active {
                color: green;
            }
        </style>
    </head>
    <body>
        <a href="#">链接伪类选择器</a>
    </body>
</html>
```

* 为了确保生效，按照LVHA的顺序声明：`:link`,`:visited`,`:hover`,`:active`
* 链接指定样式需要单独指定a标签



##### `:focus`伪类选择器

`:focus`伪类选择器用于选取获得焦点的表单元素。

焦点就是光标，一般情况`<input>`类表单元素才能获取，因此这个选择器也主要针对于表单元素来说。

```html
input:focus {
   background-color: yellow;
}
```

谁获得了光标就会改变颜色。



#### 复合选择器总结

| 选择器         | 作用                   | 特征             | 使用情况 | 隔开符号及用法              |
| -------------- | ---------------------- | ---------------- | -------- | --------------------------- |
| 后代选择器     | 用来选择后代元素       | 可以是子孙后代   | 较多     | 符号是**空格** .nav a       |
| 子代选择器     | 选择最近一级元素       | 只选亲儿子       | 较少     | 符号是**大于** .nav>p       |
| 并集选择器     | 选择某些相同样式的元素 | 可以用于集体声明 | 较多     | 符号是**逗号** .nav,.header |
| 链接伪类选择器 | 选择不同状态的链接     | 跟链接相关       | 较多     | 重点记住a{}和a:hover        |
| `:focus`选择器 | 选择获得光标的表单     | 跟表单相关       | 较少     | 记住input:focus             |



### CSS的元素显示模式

元素显示模式就是元素（标签）以什么方式进行显示比如`<div>`自己多占一行，比如一行可以放多个`<span>`。

HTML元素一般分为两大类：块元素和行内元素。



#### 块元素

常见的块元素有：`<h1>~<h6>`，`<p>`，`<div>`，`<ul>`，`<ol>`，`<li>`等，其中`<div>`标签是最典型的块元素。

特点：

* 独占一行
* 高度，宽度，外边距以及内边距都可以控制
* 宽度默认是容器（父级宽度）的100%
* 是一个容器及盒子，里面可以放行内或者块级元素

注意：

* 文字类的元素内不能使用块级元素
* `<p>`标签主要用于存放文字，因此里面不能放块级元素，特别是不能放`<div>`
* `<h1>~<h6>`也不能放块级元素



#### 行内元素

常见的行内元素有`<a>`，`<strong>`，`<b>`，`<em>`，`<i>`，`<del>`，`<s>`，`<ins>`，`<u>`，`<span>`等，其中`<span>`是最典型的行内元素。行内元素也称内联元素。

特点：

* 相邻行内元素在一行上，一行可以显示多个
* 高，宽直接设置是无效的
* 默认宽度就是它本身内容的宽度
* 行内元素只能容纳文本或其他行内元素

注意：

* 链接里面不能放链接
* 特殊情况链接`<a>`里面可以放块级元素，但转换一下块级模式最安全



#### 行内块元素

在行内元素中有几个特殊的标签-----`<img />`，`<input />`，`<td>`，他们同时具有块元素和行内元素的特点，有些资料称行内块元素。

特点：

* 和相邻行内元素（行内块）在一行上，但是他们之间会有空白缝隙，一行可以显示多个（行内元素特点）
* 默认宽度就是他本身内容的宽度（行内元素特点）
* 高度，行高，外边距以及内边框都可以控制（块级元素特点）



#### 元素显示模式总结

| 元素模式   | 元素排列               | 设置样式           | 默认宽度         | 包含                   |
| ---------- | ---------------------- | ------------------ | ---------------- | ---------------------- |
| 块级元素   | 一行只能放一个块级元素 | 可以设置宽度高度   | 容器的100%       | 容器可以包含任何标签   |
| 行内元素   | 一行可以放多个行内元素 | 不可以设置宽度高度 | 它本身内容的宽度 | 容纳文本或其他行内元素 |
| 行内块元素 | 一行放多个行内块元素   | 可以设置宽度和高度 | 它本身内容的宽度 |                        |



####元素显示模式转换

简单理解：一个模式的元素需要另一种模式的特性，比如想要增加链接`<a>`的出发范围。

```html
<html>
     <head>
        <title>元素显示模式转换</title>
        <style>
            a {
                wdith: 150px;
                height: 50px;
                background-color: pink;
                /*行内变块级*/
                display: block;
            }
            div {
                wdith: 300px;
                height: 100px;
                background-color: purple;
                /*块级变行内*/
                display: inline;
            }
            span {
                wdith: 300px;
                height: 30px;
                background-color: skyblue;
                display: inline-block;
            }
        </style>
    </head>    
    <body>
        <a href="#">行内变块级</a>
        <div>
            块级变行内
        </div>
        <span>行内元素转换为行内块元素</span>
    </body>
</html>
```

![image-20200806224123311](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200806224123311.png)



**实践：（小米网站侧边栏）**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简单版小米侧边栏</title>
    <style>
        a {
            width: 300px;
            height: 40px;
            display: block;
            font-size: 14px;
            color: white;
            background-color: darkgray;
            text-decoration: none;
            text-indent: 2em;
            line-height: 40px;
        }
        a:hover {
            background-color: #ff6700;
        }
    </style>
</head>
<body>
    <a href="#">手机 电话卡</a>
    <a href="#">电视 盒子</a>
    <a href="#">笔记本 平板</a>
    <a href="#">出行 穿戴</a>
    <a href="#">智能 路由器</a>
    <a href="#">健康 儿童</a>
    <a href="#">耳机 音响</a>
</body>
</html>
```

**文字居中：line-height: height;**



### CSS背景

#### 背景颜色

background-color属性定义了元素的背景颜色。

```html
background-color: 颜色值;
```

一般情况下元素背景颜色默认值是transparent（透明），也可手动设置。



#### 背景图片

background-image属性描述了元素的背景图像。实际开发中常见于logo或者一些装饰性的小图片或者是超大的背景图片，非常便于控制位置。

```html
background-image: none | url(url);
```

```html
div {
   width: 300px;
   height: 300px;
   background-image: url(images/Logo.png); 
}
```

| 参数值 | 作用                             |
| ------ | -------------------------------- |
| none   | 无背景图（默认的）               |
| url    | 使用绝对或者相对地址指定背景图像 |



#### 背景平铺

如果需要在HTML页面上对背景图像进行平铺，可以使用background-repeat属性。

```html
background-repeat: repeat| no-repeat| repeat-x| repeat-y;
```

分别是：平铺|不平铺|沿x轴平铺（横向平铺）|沿y平铺（纵向平铺）

背景颜色和背景图片可同在，只不过**背景图片会压住背景颜色。**



#### 背景图片位置

利用background-position属性可以改变图片在背景中的位置。

```html
background-position: x y;
```

x坐标和y坐标。可以使用方位名词或者精准单位。

| 参数值   | 说明                                              |
| -------- | ------------------------------------------------- |
| length   | 百分数\|有浮点数字和单位标识符组成的长度值        |
| position | top\|center\|bottom\|left\|center\|right 方位名词 |

* left top和top left效果一样
* 如果只指定了一个方位名词，另一个省略则默认剧中对齐
* 如果参数值是精确坐标，那么第一个肯定是x坐标，第二个一定是y坐标
* 如果只指定一个数值，那该数值一定是x坐标，另一个默认垂直居中
* 也可以两种混用



#### 背景图像固定（背景附着）

background-attachment属性设置背景图像是否固定或者随着页面的其余部分滚动。

background-attachment后期可以制作视差滚动的效果。

```html
background-attachment: scroll| fixed;
```

| 参数   | 作用                     |
| ------ | ------------------------ |
| scroll | 背景图像是随对象内容滚动 |
| fixed  | 背景图像固定             |



#### 背景的复合写法

简化背景属性的代码，属性合并简写在同一个属性background中，从而节约代码量。

顺序：

```txt
background: 背景颜色 背景图片 背景平铺 背景图像滚动 背景图片位置;
```

```html
background: transparent url(image.ipg) repeat-y fixed top;
```



#### 背景颜色半透明

CSS为我们提供了背景颜色半透明效果。

```html
background: rgba(0,0,0,0.3);
```

* r-red、g-green、b-blue
* 最后一个参数是alpha透明度，取值范围在0-1之间
* 0.3可以省略为.3
* 只有背景颜色半透明



#### 背景总结

| 属性                  | 作用           | 值                                                   |
| --------------------- | -------------- | ---------------------------------------------------- |
| background-color      | 背景颜色       | 预定义的颜色/十六进制/RGB代码                        |
| background-image      | 背景图片       | url（图片路径）                                      |
| background-repeat     | 是否平铺       | repeat/no-repeat/repeat-x/repeat-y                   |
| background-position   | 背景位置       | length/position                                      |
| background-attachment | 背景附着       | scroll（背景滚动）/fixed（背景固定）                 |
| 背景简写              | 书写更简单     | 背景颜色 背景图片 背景平铺 背景图像滚动 背景图片位置 |
| 背景色半透明          | 背景颜色半透明 | background: rgba(0,0,0,0.3);                         |

