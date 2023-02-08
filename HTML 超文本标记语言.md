### HTML 超文本标记语言

Web标准构成：结构（HTML）、表现（CSS）、行为（交互效果Javascript）

#### 标签

1.所有标签都在<>里：<html></html>双标签，单标签<br/>

2.包含关系（父子关系）

```html
<head>
	<title>
    </title>   
</head>
```

并列关系

```html
<head></head>
<body></body>
```

3.<html>根标签<head>头标签<title>标题<body>主体

<html lang="en">en定义语言为英语，zh-CN定义语言为中文；

```html
<meta charset="UTF-8"> 
```

UTF-8万国码；

##### 常用标签

1.标题标签：<h1>—<h6>(双标签)重要性依次递减，文字加粗，字号变大（h1字号最大），一个标题独占一行。

2.段落标签：<p></p>文本在段落中根据浏览器窗口大小自动换行，段与段有空隙。

3.换行标签：<br/>强制换行，单标签，没有空隙。

##### 文本格式化

1.**加粗**<strong></strong>或<b></b>

2.**倾斜**<em></em>或<i></i>

3.删除线<del></del>或<s></s>

4.下划线<ins></ins>或<u></u>

```html
	<strong>加粗</strong>文字
    <em>倾斜</em>文字
    <del>删除线</del>文字
    <ins>下划线</ins>文字
```

##### 盒子(装内容)

1.<div></div>分区，布局一行只有一个div,大盒子；

2.<span></span>跨行，一行可以有多个span，小盒子。

```html
    <div>单独占一行单独占一行单独占一行</div>
    <div>单独占一行单独占一行单独占一行</div>
    <span>百度</span>
    <span>新浪</span>
    <span>腾讯</span>
```

![1675852783383](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\1675852783383.png)

##### 图像标签和路径

1.图像标签<img src="图像URL" alt="替换文本，图像不能显示的文字">，**src**是<img>标签的**`必须属性`**，指定图像文件的路径和文件名；**title**:提示文本，鼠标放到图像上时显示文字；**width**(像素):设置图像宽度；**height**(像素)：设置图像高度（一般修改一个，另一个等比例缩放）；**border**(像素)：设置图像边框粗细（一般通过CSS设置）。

属性写在<img>标签名里后；属性不分先后，标签名与属性，属性与属性之间均以空格分开。属性采取键值对格式

```html
<img src="img.jpg" alt="" height="250"  title="草莓熊"><br/>
    <img src="img.jpg" alt="" width="250"  title="草莓熊"><br/>
    <img src="img1.jpg" alt="一人之下"><br/>
    <img src="img.jpg" alt="" height="250"  title="草莓熊" border="15"><br/>
```

2.路径

2.1相对路径：引用文件所在位置，图片相对于HTML页面的位置；同一级路径：直接写；上一级路径:加**../**+图片；下一级路径：文件名+"/"+图片。

2.2绝对路径：图片在电脑中的位置（不支持使用）C盘，D盘标，网页图片地址复制使用。

**链接标签**







