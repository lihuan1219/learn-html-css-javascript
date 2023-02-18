### HTML 超文本标记语言

Web标准构成：结构（HTML）、表现（CSS）、行为（交互效果Javascript）

#### 标签上

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

3.< html>根标签< head>头标签< title>标题< body>主体

< html lang="en">en定义语言为英语，zh-CN定义语言为中文；

```html
<meta charset="UTF-8"> 
```

UTF-8万国码；

##### 常用标签

1.标题标签：< h1>—< h6>(双标签)重要性依次递减，文字加粗，字号变大（h1字号最大），一个标题独占一行。

2.段落标签：< p>< /p>文本在段落中根据浏览器窗口大小自动换行，段与段有空隙。

3.换行标签：< br/>强制换行，单标签，没有空隙。

##### 文本格式化

1.**加粗**< strong>< /strong>或< b>< /b>

2.**倾斜**< em>< /em>或< i>< /i>

3.删除线< del>< /del>或< s></s>

4.下划线< ins>< /ins>或< u>< /u>

```html
	<strong>加粗</strong>文字
    <em>倾斜</em>文字
    <del>删除线</del>文字
    <ins>下划线</ins>文字
```

##### 盒子(装内容)

1.< div>< /div>分区，布局一行只有一个div,大盒子；

2.< span>< /span>跨行，一行可以有多个span，小盒子。

```html
    <div>单独占一行单独占一行单独占一行</div>
    <div>单独占一行单独占一行单独占一行</div>
    <span>百度</span>
    <span>新浪</span>
    <span>腾讯</span>
```

![1675852783383](.\images\1675852783383.png)

##### 图像标签和路径

1.图像标签<img src="图像URL" alt="替换文本，图像不能显示的文字">，**src**是< img>标签的**`必须属性`**，指定图像文件的路径和文件名；**title**:提示文本，鼠标放到图像上时显示文字；**width**(像素):设置图像宽度；**height**(像素)：设置图像高度（一般修改一个，另一个等比例缩放）；**border**(像素)：设置图像边框粗细（一般通过CSS设置）。

属性写在< img>标签名里后；属性不分先后，标签名与属性，属性与属性之间均以空格分开。属性采取键值对格式

```html
<img src="img.jpg" alt="" height="250"  title="草莓熊"><br/>
    <img src="img.jpg" alt="" width="250"  title="草莓熊"><br/>
    <img src="img1.jpg" alt="一人之下"><br/>
    <img src="img.jpg" alt="" height="250"  title="草莓熊" border="15"><br/>
```

2.路径

2.1相对路径：引用文件所在位置，图片相对于HTML页面的位置；同一级路径：直接写；上一级路径:加**../**+图片；下一级路径：文件名+"/"+图片。

2.2绝对路径：图片在电脑中的位置（不支持使用）C盘，D盘标，网页图片地址复制使用。

##### **链接标签**

1.语法格式:< a href="跳转目标" target="目标窗口的弹出方式">< /a>，href必须属性，目标的url地址，target：打开方式，_self为默认值（当前窗口）， _blank为在新窗口打开。

2.分类：外部链接：跳转别的页面，必须为http://的开头

​               内部链接：打开文件夹目录文件页面。

  			 空链接：内容为空，< a href="#">< /a>

​			  下载链接：地址链接为文件.exe、zip等压缩包形式，文件夹目录中直接写。

​			   网页元素链接：直接讲图片，音频等写在文本位置。

​			   锚点链接：点击链接，快速定位到页面中的某一具体位置，1在href属性中，设置属性值为**#名字**的形式< a href="#name">姓名< /a>，2找到目标位置标签，添加一个id属性=上一步的名字，< q id="name">姓名< /q>

##### 注释

解释为什么用：选中不出现的文字使用快捷键：Ctrl+?(/)

##### 特殊字符

空格：&nbsp ;一个空格 ；小于号:&lt；大于号:&gt；(需要添加分号)

#### 标签下

##### 表格标签

1.用于显示数据，数据内容规律，可读性好，展示数据作用。

2.组成：

```html
<table>定义一个表格
	<tr>定义表格中的行
		<td>单元格内的标签</td>单元格<td></td>
	</tr>
    <tr>定义表格中的行
		<td>单元格内的标签</td>单元格<td></td>
	</tr>
</table>
```

表头单元格（th）：文字内容加粗居中显示，一块一块

```html
<table>定义一个表格
	<tr>定义表格中的行
		<th>姓名</th>
        <th>班级</th>
	</tr>
    <tr>定义表格中的行
		<td></td>  <td></td>
	</tr>
</table>
```

3.属性（一般用CSS写，写在table中）

- align:对齐方式（left、center、right)


- border:是否拥有边框（1或"",默认为""）


- cellpadding:单元边沿(边框)与内容(文字)之间的空白，默认值1像素（像素值）


- cellspacing:单元格之间的空白，默认值2（像素值），习惯为0


- width:表格的宽度（像素值或百分比）

###### 4.表格结构

thead表格的头部区域（范围更广）内部必须有tr一般在第一行，tbody表格的主体区域，主要放数据。

###### 5.合并单元格（写在td中）

跨行合并：rowspan="合并单元格的个数"以上为目标单元格

跨列合并：colspan="合并单元格的个数"以左侧为目标单元

最后删除多余单元格

##### 列表标签

1.无序列表

```html
<ul>
	<li>列表项</li>
	<li>列表项</li>……
</ul>
```

列表项之间没有顺序之分，为并列关系，ul标签中只能嵌套li标签，直接在ul标签中输入其他标签或文字是不被允许的。li标签中可以放其他标签。

2.有序列表

```html
<ol>
	<li>列表项1</li>
	<li>列表项2</li>……
</ol>
```

有序列表有样式属性，采用CSS设置，ol标签与ul用法一致。

3.自定义列表

对于术语或名词进行解释和描述，定义列表项前没有任何项目符号。

```html
<dl>
	<dt>名词</dt>
	<dd>名词解释1</dd>
	<dd>名词解释2</dd>
</dl>
```

dl中只能有dt，dd标签；一个dt中可以对应多个dd；

##### 表单标签

组成：表单域、表单控件（表单元素）和提示信息

1.表单域（包含表单元素的区域）：form标签定义表单域，实现用户信息收集和传递，form标签将它范围内的表单元素信息提交给服务器；

< form action="url地址" method="提交方式（get/post）" name="表单域名称">表单元素< /form>

2.表单控件（表单元素）：

input输入表单元素：< input type="属性值" name="元素名称" >type为必须属性，type属性设置不同的属性值指定的控件类型不同；

input标签为单标签属性有：type、name（区别表单元素）、value、checked(单选和复选可以使用，当网页一打开就可以默认选中这个按钮，checked="checked")、

maxlength（规定输入字段中字符的最大长度，属性值为正整数）

type属性值有：text文本框（输入任何文字）例：name="username" value="请输入用户名（只有在文本框使用可以直接看到，其他属性值只能从后台看到）"

​							password密码框（字符被隐藏）例：name="pwd"

​							radio单选按钮(name必须有相同的名字name才可以实现单选)

​							checkbox复选框(name名字也要相同)	

​							submit提交按钮< input type="submit" value="改按钮上的名字">

​							reset重置按钮，默认为重置，可通过value改（将数据进行清除，恢复初始状态

​							button可点击按钮，多数用于通过JS脚本，通过value写名

​							file文件域，上传文件

- label标签为input元素定义标注，绑定一个表单元素，点击label时，浏览器就会自动转移到绑定的表单元素上。

  ```html
  性别：<label for="sex">男</label>
  <input type="radio" name="sex" id="sex">
  ```

  重点：label中的for属性要与相关元素的id属性相同

- select下拉表单元素：select中至少包含一对option

  ​									在option中定义selected="selected"时，当前选项为默认选项

  ```html
  <select name="" id="">
              <option value="">山东</option>
              <option value="">上海</option>
              <option value="">南京</option>
              <option value="">北京</option> </select>
  ```

- textarea文本域元素：当内容较多时使用，特大号文本框

  < textarea name="" id="" cols="30" rows="10">文本内< /textarea>  ；

  cols：每行字符数，rows：显示的行数

  