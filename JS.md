# JAVAScript

[TOC]

## 计算机相关

#### 编程语言

**编程：**就是让计算机为解决某个问题而使用某种程序设计语言编写程序代码,并最终得到结果的过程。

**计算机程序：**就是计算机所执行的一系列的指令集合,而程序全部都是用我们所掌握的语言来编写的,所以人们要控制计算机-定要通过计算机语言向计算机发出命令。

**计算机语言**指用于人与计算机之间通讯的语言,它是人与计算机之间传递信息的媒介。

计算机语言的种类非常的多,总的来说可以分成**机器语言,汇编语言和高级语言**三大类。

实际上计算机最终所执行的都是机器语言，它是由 "0” 和“1”组成的二进制数,**二进制是计算机语言的基础。**

**编程语言：**可以通过类似于人类语言的”语言”来控制计算机,让计算机为我们做事情, 这样的语言就叫做Programming Language 。

编程语言是用来控制计算机的一系列指令,它有固定的格式和词汇(不同编程语言的格式和词汇不一样) , 必须遵守。

如今**通用的编程语言有两种形式：汇编语言和高级语言**。

**汇编语言**和机器语言实质是相同的,都是直接对硬件操作,只不过指令采用了英文缩写的标识符,容易识别和记忆。

**高级语言**主要是相对于低级语言而言,它并不是特指某一种具体的语言 ,而是包括了很多编程语言, 常用的有C语言、C++、Java、C#、Python、 PHP、JavaScript. Go语言、Objective-C、 Swift等。

**编程语言和标记语言的区别：**

**编程语言**有很强的逻辑和行为能力。在编程语言里你会看到很多ifelse、for 、while等 具有逻辑性和行为能力的指令,这是主动的。

**标记语言( html )**不用于向计算机发出指令,常用于格式化和链接。标记语言的存在是用来被读取的,他是被动的。



#### 计算机基础

![image-20200903163621944](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200903163621944.png)

**数据存储：**

计算机内部使用二进制0和1来表示数据。

所有数据,包括文件、图片等最终都是以二进制数据( 0和1 )的形式存放在硬盘中的。

所有程序,包括操作系统,本质都是各种数据,也以二进制数据的形式存放在硬盘中。平时我们所说的安装软件,其实就是把程序文件复制到硬盘中。

**数据存储单位：**

bit< byte< kb< GB < TB <.....

* 位(bit): 1bit 可以保存- -个0或者1 ( 最小的存储单位)
* 字节(Byte): 1B= 8b
* 千字节(KB): 1KB= 1024B
* 兆字节(MB) : 1MB= 1024KB
* 吉字节(GB): 1GB = 1024MB
* 太字节(TB): 1TB= 1024GB
* ....



## JAVAScript

### 初识JS

* JavaScript是世界上最流行的语言之一, 是-种运行在客户端的脚本语言( Script是脚本的意思)
* 脚本语言:不需要编译,运行过程中由js解释器(js引擎)逐行来进行解释并执行
* 现在也可以基于Node.js技术进行服务器端编程



#### JAVAScript的作用

* 表单动态校验(密码强度检测) ( JS产生最初的目的)
* 网页特效
* 服务端开发(Node.js)
* 桌面程序(Electron)
* App(Cordova)
* 控制硬件物联网(Ruf)
* 游戏开发(cocos2d-js)



#### HTML/CSS/JS的关系

#####HTML/CSS标记语言--描述类语言

* HTML 决定网页结构和内容(决定看到什么) ,相当于人的身体
* CSS 决定网页呈现给用户的模样(决定好不好看) ,相当于给人穿衣服、化妆

##### JS脚本语言-编程类语言

* 实现业务逻辑和页面控制(决定功能) ,相当于人的各种动作



#### 浏览器执行JS

浏览器分成两部分：**渲染引擎**和**JS引擎**

* **渲染引擎：**用来解析HTML与CSS ,俗称内核,比如chrome浏览器的blink , 老版本的webkit
* **JS 引擎：**也称为JS解释器。用来读取网页中的JavaScript代码 ,对其处理后运行,比如chrome浏览器的V8

浏览器本身并不会执行JS代码,而是通过内置JavaScript弓|擎(解释器)来执行JS代码。JS 引擎执行代码时逐行解释每一句源码(转换为机器语言) ,然后由计算机去执行,所以JavaScript语言归为脚本语言，会逐行解释执行。



#### JS的组成

![image-20200903170740673](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200903170740673.png)



#####ECMAScript

**ECMAScript**是由ECMA国际(原欧洲计算机制造商协会)进行标准化的一门编程语言,这种语言在万维网上应用广泛,它往往被称JavaScript或JScript ,但实际上后两者是ECMAScript语言的实现和扩展。

![image-20200903170844124](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200903170844124.png)

**ECMAScript : ECMAScript规定了JS的编程语法和基础核心知识,是所有浏览器厂商共同遵守的一套JS语法I业标准。**



##### DOM---文档对象模型

**文档对象模型( Document Object Model ,简称DOM)** , 是W3C组织推荐的处理可扩展标记语言的标准编程接口。通过DOM提供的接口可以对页面上的各种元素进行操作(大小、位置、颜色等)。



#####BOM---浏览器对象模型

**BOM (Browser Object Model ,简称BOM)**是指浏览器对象模型,它提供了独立于内容的、可以与浏览器窗进行互动的对象结构。通过BOM可以操作浏览器窗口,比如弹出框、控制浏览器跳转、获取分辨率等。



#### JS三种书写位置

JS有三种书写位置，分别为行内、内嵌和外部。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 2.内嵌式的JS -->
    <script>
        // alert('我是弹窗');
    </script>
    <!-- 3.外部JS script双标签 -->
    <script src="my.js"></script>
</head>
<body>
    <!-- 1.行内式的JS 直接写到元素的内部 -->
    <!-- <input type="button" value="点我" onclick="alert('消息提示：我被点了')"> -->
</body>
</html>
```



#####行内式JS

```html
<input type="button" value="点我试试" onclick="alert('嘿，我被点了')" />
```

* 可以将单行或少量JS代码写在HTML标签的事件属性中(以on开头的属性) , 如: onclick
* 注意单双引号的使用:在HTML中我们推荐使用双引号, JS中我们推荐使用单引号
* 可读性差，在htmI中编写JS大量代码时,不方便阅读;
* 引号易错,引号多层嵌套匹配时,非常容易弄混;
* 特殊情况下使用



##### 内嵌JS

```html
<script>
    alert('我是弹窗');
</script>
```

* 可以将多行JS代码写到`<script>`标签中
* 内嵌JS是学习时常用的方式



##### 外部JS文件

```html
<script src="my.js"></script>
```

* 利于HTML页面代码结构化,把大段JS代码独立到HTML页面之外,既美观,也方便文件级别的复用
* 引用外部JS文件的script标签中间不可以写代码
* 适合于JS代码量比较大的情况



#### JS注释

```js
//1.单行注释   快捷键：ctrl + /
/*2.多行注释   自己设置后的快捷键：shift + alt + /
  2.多行注释*/
```



####JS输入输出语句

为了方便信息的输入输出, JS中提供了一些输入输出语句,其常用的语句如下：

| 方法             | 说明                           | 归属   |
| ---------------- | ------------------------------ | ------ |
| alert(msg)       | 浏览器弹出警示框               | 浏览器 |
| console.log(msg) | 浏览器控制台打印输出信息       | 浏览器 |
| prompt(info)     | 浏览器弹出输入框，用户可以输入 | 浏览器 |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        // 这是一个输入框
        prompt('请输入你的年龄');
        // alert弹出警示框 输出的展示给用户的
        alert('计算的结果是');
        // console控制台输出 给程序员测试用的
        console.log('我是给程序员看的');
    </script>
</head>
<body> 
</body>
</html>
```



### 变量

白话:变量就是一一个装东西的盒子。

通俗:变量是用于存放数据的容器。我们通过变量名获取数据,甚至数据可以修改。

本质:变量是程序在内存中申请的一块用来存放数据的空间。

类似我们酒店的房间, 一个房间就可以看做是一个变量。

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200904235204002.png" alt="image-20200904235204002" style="zoom: 67%;" />



#### 变量的使用

变量在使用时分为两步：

* 声明变量
* 赋值



##### 声明变量

```js
//声明变量
var age;//声明一个名称为age的变量
```

* var是一个JS关键字.用来声明变量( variable变量的意思)。使用该关键字声明变量后,计算机会自动为变量分配内存空间,不需要程序员管
* age是程序员定义的变量名, 我们要通过变量名来访问内存中分配的空间



##### 赋值

```js
//声明一个名称为age的变量
var age;
//给age这个变量赋值为10
age = 10;
//输出结果
console.log(age);
```

* =用来把右边的值赋给左边的变量空间中此处代表赋值的意思
* 变量值是程序员保存到变量空间里的值



##### 变量的初始化

```js
var age = 18; //声明变量同时赋值为18
```

声明一个变量并负值，我们称之为变量的初始化。



##### 案例

1、有个叫卡卡西的人在旅店登记的时候前台让他填一张表，这张表里的内容要存到电脑上,表中的内容有:姓名、年龄、邮箱、家庭住址和工资,存储之后需要把这些信息显示出来,所显示的内容如下:
我叫旗木卡卡西,我住在火影村,我今年30岁了,我的邮箱是kakaxi@itcast.cn ,我的工资2000。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var myname = '旗木卡卡西';
        var address ='火影村';
        var age = 30;
        var email = 'kakaxi@itcast.cn';
        var salary = 2000;
        console.log(myname);
        console.log(address);
        console.log(age);
        console.log(email);
        console.log(salary);
    </script>
</head>
<body>
    
</body>
</html>
```



2、弹出一个输入框,提示用户输入姓名。
      弹出一一个对话框,输出用户刚才输入的姓名。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
    // 1.用户输入信息
    var myname = prompt('请输入您的名字');
    // 2.输出这个用户名
    alert(myname);
    </script>
</head>
<body>
    
</body>
</html>
```



#### 变量的语法扩展

##### 更新变量

一个变量被重新复赋值后，它原有的值就会被覆盖 。变量值将以最后一次赋的值为准。

```js
var age = 18;
age = 81; //最后的结果就是81因为18被覆盖掉了
```



#####同时声明多个变量

同时声明多个变量时，只需要写一个var，多个变量名之间使用英文逗号隔开。

```js
var age = 20,
    name = 'cxy',
    sex = 'nv';
```



##### 声明变量的特殊情况

| 情况                        | 说明                   | 结果      |
| --------------------------- | ---------------------- | --------- |
| var age; console.log(age);  | 只声明 不赋值          | undefined |
| console.log(age)            | 不声明 不赋值 直接使用 | 报错      |
| age = 10; console.log(age); | 不声明 只赋值          | 10        |



#### 变量的命名规范

* 由字母(A-Z、a-z).数字(0-9)、 下划线(_)、元符号($ )组成,如: usrAge, num01, name
* 严格区分大小写。var app;和var App;是两个变量
* 不能以数字开头。18age 是错误的
* 不能是关键字保留字。例如:var、for、while
* 变量名必须有意义。MMD BBD       nl→age
* **遵守驼峰命名法。首字母小写，后面单词的首字母需要大写。myFirstName**



##### 案例

交换变量值。

<img src="C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200905110835643.png" alt="image-20200905110835643" style="zoom:67%;" />

```js 
//1.我们需要一个临时变量
//2.把apple1给我们的临时变量
//3.把apple2里面的苹果给apple1
//4.把临时变量的值给apple2
var temp;//声明了一个临时变量为空
var apple1 = '青苹果';
var apple2 = '红苹果';
temp = apple1;//把右边给左边
apple1 = apple2;
apple2 = temp;//给谁谁接收
console.log(apple1);
console.log(apple2);
```



### 数据类型

在计算机中,不同的数据所需占用的存储空间是不同的,为了便于把数据分成所需内存大小不同的数据，充分利用存储空间，于是定义了不同的数据类型。

简单来说,数据类型就是数据的类别型号。比如姓名“张E”,年龄18, 这些数据的类型是不一样的。

变量是用来存储值的所在处,它们有名字和数据类型。变量的数据类型决定了如何将代表这些值的位存储到计算机的内存中。**JavaScript 是一种弱类型或者说动态语言。**这意味着不用提前声明变量的类型,在程序运行过程中,类型会被自动确定。

```js
var age = 10;          //这是一个数字型
var areYouOk = '是的'； //这是一个字符串
```

**JS的变量数据类型时只有程序在运行过程中，根据等号右边的值来确定的。**

**<u>JS有用动态类型，同时也意味着相同的变量可用作不同的类型。</u>**

```js
var x = 6;      //x为数字
var x = 'Bill'; //x为字符串
```



**JS把数据类型分为两类：**

* 简单数据类型（Number,String,Boolean,Undefined,Null）
* 复杂数据类型（object）



#### 简单数据类型（基本数据类型）

JAVAScript中的简单数据类型及其说明如下：

| 简单数据类型 | 说明                                             | 默认值    |
| ------------ | ------------------------------------------------ | --------- |
| Number       | 数字型，包含 整型值和浮点型值，如21、0.21        | 0         |
| Boolean      | 布尔值类型，如true、false等价于1和0              | false     |
| String       | 字符串类型，如"张三"。JS里字符串都带引号         | ""        |
| Undefined    | var a;声明了变量a但是没有给值，此时a = undefined | undefined |
| Null         | var a = null;声明了变量a为空值                   | null      |



##### 数字型Number

###### 数字型进制

最常见的进制有二进制、八进制、十进制、十六进制。

```js
// 1.八进制数字序列范围: 0~7
//数字前面加0 表示八进制
var num1 = 07;
//对应十进制的7
var num2 = 019; 
// 对应十进制的19
var num3 = 08;
//对应十进制的8
// 2.十六进制数字序列范围: 0~9以及A~F
//数字前面加0x 表示十六进制
var num = 0xA;
```

**在JS中八进制前面加0 ,十六进制前面加0x。**



###### 数字型范围

JavaScript中数值的最大和最小值

```js
alert (Number .MAX VALUE); // 1. 7976931348 623157e+308
alert (Number .MIN VALUE); // 5e-324
```



###### 数字型三个特殊值

```js
alert (Infinity) ; // Infinity
alert(-Infinity);  // - Infinity
alert (NaN) ;      //NaN
```

* Infinity ,代表无穷大,大于任何数值
* -Infinity ,代表无穷小，小于任何数值
* NaN , Not a number ,代表一个非数值



######isNaN()

isNaN()这个方法用来判断非数字，并且返回一个值 如果是数字返回的时false，如果不是数字返回的是true。

![image-20200905121418217](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200905121418217.png)

```js
var usrAge = 21;
var isOk = isNaN (userAge) ;
console .log (i sNum) ;// false， 21不是一个非数字
var usrName = "andy";
console . log (isNaN (userName)); // true"andy"是一个非数字
```



##### 字符串型String

字符串型可以是引号中的任意文本,其语法为双引号””和单引号”。

```js
var strMsg = "我爱北京天安门~"; // 使用双引号表示字符串
var strMsg2 = '我爱吃猪蹄~'; // 使用单引号表示字符串
//常见错误
var strMsg3 =我爱大肘子;
//报错,没使用引号,会被认为是js代码,但js没有这些语法
```

**因为HTML标签里面的属性使用的是双引号，JS这里我们更推荐使用单引号。**



###### 字符串引号嵌套

JS可以**用单引号嵌套双引号**，或者用**双引号嵌套单引号**（**<u>外双内单，外单内双</u>** ）

```js
var strMsg = '我是"高帅富"程序猿'; // 可以用"包含"
var strMsg2 = "我是'高帅富程序猿"; // 也可以用"包含"
//常见错误
var badQuotes = 'What on earth?"; //报错,不能单双引号搭配
```



###### 字符串转义符

类似HTML里面的特殊字符,字符串中也有特殊字符,我们称之为转义符。
转义符都是\开头的,常用的转义符及其说明如下

| 转义符 | 解释说明                 |
| ------ | ------------------------ |
| \n     | 换行符，n是newline的意思 |
| \\\    | 斜杠\                    |
| \\'    | '单引号                  |
| \\"    | "双引号                  |
| \t     | tab 缩进                 |
| \b     | 空格，b是blank的意思     |



###### 字符串长度

字符串是由若干字符组成的,这些字符的数量就是字符串的长度。通过字符串的length属性可以获取整个字符串的长度。

```js
var strMsg = "我是帅气多金的程序猿! ";
alert (strMsg. length); //显示11
```



###### 字符串拼接

* 多个字符串之间可以使用 +进行拼接,其拼接方式为字符串+任何类型=拼接之后的新字符串
* 拼接前会把与字符串相加的任何类型转成字符串,再拼接成一一个新的字符串

```js
//1.1字符串"相加”
alert('hello' +，，+ 'world'); // hello world 
//1.2数值字符串"相加"
alert("100' + '100"); // 100100
//1.3数值字符串+数值
alert('11' + 12);    // 1112
```

**+号总结口诀：数值相加，字符相连**



###### 字符串拼接加强

```js
console.log('pink老师' + 18);   //只要有字符就会相连
var age = 18;
// console. log( 'pink老师age岁啦'); //这样不行哦
console.log('pink老师' + age) ; // pink老师18
console.1og('pink老师' + age + '岁啦'); // pink老师18岁啦
```

* 我们通常会将字符串和变量来拼接，因为变量可以很方便地修改里面的值
* 变量是不能添加引号的,因为加引号的变量会变成字符串
* 如果变量两侧都有字符串拼接,口诀“引引加加”, 删掉数字,变量写加中间



#####案例：显示年龄

案例分析：

![image-20200905131717837](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200905131717837.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var age = prompt('请输入您的年龄');
        var str = '您今年已经'+ age + '岁了';
        alert(str);
    </script>
</head>
<body>
</body>
</html>
```



##### 布尔型Boolean

布尔类型有两个值: true和false , 其中true表示真(对) ，而false表示假(错)。
布尔型和数字型相加的时候，true 的值为1 , false 的值为0。

```js
console. log(true + 1);  // 2
console. log(false + 1); // 1
```



##### Undefined和Null

一个声明后没有被赋值的变量会有一个默认值 undefined (如果进行相连或者相加时,注意结果)

```js
var variable;
console.log (variable);        // unde fined
console.1og('你好' + variable); // 你好undefined
console.1og(11 + variable) ;   // NaN
console.log(true + variable) ; // NaN
```

一个声明变量给null值,里面存的值为空(学习对象时,我们继续研究nul)

```js
var vari = null;
console.1og('你好' + vari); // 你好null
console. log(11 + vari) ;  // 11
console. log(true + vari) ;// 1
```



####获取变量数据类型

##### 获取检测变量的数据类型

typeof可用来获取检测变量的数据类型。

```js
var num = 10;
console.log(typeof num);
```

![image-20200905134851220](C:\Users\CXY\AppData\Roaming\Typora\typora-user-images\image-20200905134851220.png)



##### 字面量

字面量是在源代码中一个固定值的表示法 ,通俗来说,就是字面量表示如何表达这个值。

* 数字字面量:8,9,10
* 字符串字面量:‘黑马程序员, "大前端”
* 布尔字面量: true , false



#### 数据类型的转换



























