## 前端开发

### 前端开发语言

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

### HTML超文本标记语言

`<` 标记      `<html>` 标签     `<html> </html>` 标签对 

大多数为双标签，极少数为单标签，如换行标签`<br />` 。

标签的关系：<u>包含关系</u>和<u>并列关系</u> 

#### HTML基本结构标签

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

#### HTML常用标签

##### 标题标签`<h1>`-`<h6>`

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



##### 段落和换行标签

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



 ##### 文本格式化标签

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



##### `<div>`和`<span>`标签

`<div>`和`<span>`是没有语义的，它们是一个盒子，用来装内容。

```html
<div>这是头部</div>
<span>今日价格</span>
```

div是division的缩写，表示分割、分区。span意为跨度、跨距。

div独占一行（大盒子），span一行可以放多个（小盒子）。



##### 图像标签和路径

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



##### 超链接标签

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

6. 锚点链接



-----

### CSS
