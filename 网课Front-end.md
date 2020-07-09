## 前端开发

### 前端开发语言

* HTML 超文本标记语言 --- 结构

* CSS 层叠样式表 ------------ 样式

* JS(JavaScript) --------------- 行为

  ![ ](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200709104324473.png) 

  ![image-20200709104504888](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200709104504888.png)

----

### HTML超文本标记语言

`<` 标记      `<html>` 标签     `<html> </html>` 标签对

![image-20200709105242182](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200709105242182.png) 

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

| 标签名          | 定义       | 说明                                                   |
| --------------- | ---------- | ------------------------------------------------------ |
| <html></html>   | HTML标签   | 页面中最大的标签，根标签                               |
| <head></head>   | 文档的头部 | 在head标签中我们必须设置的标签是title                  |
| <title></title> | 文档的标题 | 让页面拥有一个属于自己的网页标题                       |
| <body></body>   | 文档的主体 | 元素包含文档的所有内容，页面内容基本都是放到body里面的 |

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

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200709165353699.png" alt="image-20200709165353699" style="zoom: 50%;" /> 



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

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200709170855481.png" alt="image-20200709170855481" style="zoom: 67%;" /> 

-----

### 下一主题



