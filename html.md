快捷键：ctrl+w 选中代码









# HTML的学习

HTML的样式：外部样式：
从外部引用css来进行修改：语法为：

```html
<link rel="stylesheet" type="text/css" href="mystyle.css">
```

这样就可以使用外部的css文件来修改对应得标签，在css文件中，我们对需要时候用的标签进行对应得风格修改，在我们的网页中直接使用就可以了如下：


![1580464745372](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580464745372.png)

![1580464759188](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580464759188.png)

![1580464777190](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580464777190.png)

## 内部样式表：

我们直接在网页的内部直接使用style对标签进行修改。语法为：

```html
<style type="text/css">
    p{你想要得样式
        
    }
</style>
```

![1580465122567](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580465122567.png)

我们写外联和内联的时候最好是在头部写，方便修改也方便查看

## 内联样式：

这种就是直接在我们所需要的修改的标签位置直接写，他的语法为：

```html
<p style="color:red;....">
```

![1580465476873](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580465476873.png)

# HTML的链接：

链接数据：

## 文本链接

html插入链接跳转，语法为：

```html
<a href="http://www.xxxxx.com.cn">"在这个地方输入你的链接的名字"</a>
```

![1580465806645](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580465806645.png)

## 图片链接：

```html
<a href="http://www.baidu.com"><img src="你的图片地址"></a>
```

## 属性：

### href属性：

指向另外一个文档的链接

### name属性：

创建文档内的链接（锚点）语法为：

```html
<a name="top(自定义的名字)">这是顶端</a>
<a href="#top你定义的名字)">点击跳转</a>
```

在网页常见的就是点击回到顶端，点击到某一个地方，这就是这个name的作用：
![1580477782013](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580477782013.png)

## img标签属性：

alt:替换文本属性；width：宽；height：高；这是在我们使用图片链接的时候就可以使用的属性，也是插入图片的属性：
![1580477149639](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580477149639.png)

这样就可以控制大小了，除此以外，有的时候图片加载失败了，当人看到的时候不知道是什么东西，所以再使用alt这个属性来定义我们的图片：


![1580477290340](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580477290340.png)

# 表格：

## 表格的标签：

### "<table>":

定义表格，在标签内还有设置边框得属性--borde="1"，数值越大边框得线体越粗，为0的时候就没有边框

### <caption>:

定义表格的标题，就是我们这个表格是什么表格

### <th>：

定义表格的表头，就比如姓名，电话号码之类统计的东西

### <tr>：

定义表格的行（竖着写内容）

### <td>：

定义表格的单元（就是横着写内容）

### <thead>：

定义表格的页眉

### <thbody>：

定义表格的主体

### <tfoot>：

定义表格的页眉

### <col>：

定义表格的列属性

![1580480149770](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580480149770.png)

除此以外，还可以在表格里面嵌入表格，嵌入列表，还有可以设置单元格边距：

![1580532172501](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580532172501.png)

## 列表：

无序列表：使用"<ul>""<li>"标签来定义，属性有:disc、circle、square，这几个都是用来改变每一个列表前面的符号的，默认得到是实心圆，可以通过引入css来进行美化，更换：
![1580533370859](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580533370859.png)

有序列表：使用"<ol>""<li>"标签定义，属性有：A、a、I、i、start，这几个属性是用来进行排序使用的，我们使用a属性，就是从a-z排序，以此类推,start适用于我们排序是从什么数字开始的，一般我们都是从1开始，但也可以从任意的数字开始：

![1580533814740](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580533814740.png)

嵌套列表：使用"<ul>""<ol>""<li>"标签定义。嵌套列表就是在列表里面在放一个列表
![1580535452531](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580535452531.png)

自定义标签：使用"<di>""<dt>""<dd>"定义

![1580535758158](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580535758158.png)

## 块元素的使用：

所谓的快元素就是能够以新的一行开头的标签，常见的段落，标题，列表都是这样的

## 内联元素：

指通常不会以新的一行开始的标签，如字体加粗“<b>”，超链接标签，图片标签等等

## div元素：

div元素也被称为块元素，主要是组合html元素的容器

""<span>""元素
内联元素，作为文本的容器，如下：

![1580572089280](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580572089280.png)

# html的布局

## 使用""<div>""元素布局：

先定义一个全局控制的div，既div id="container"，这个就是我们网页的底面，然后在在这个div里面继续添加其他的部分，比如头部""<div id="head">""，底部"<div id="xxx">"，左边模块"<div id="xxx">"，右边模块："<div id="xxx">：
![1580652050959](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580652050959.png)

然后我们在头部来对每一个标签进行操作：在这里我们定义全局标签的高时，使用950px而不是和宽一样使用100%，是因为使用100%的话屏幕没有办法铺满，宽度有限，但是高度没有限制，你的网页可以无限长，只要你愿意。所以我们就需要使用950px

![1580652184917](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580652184917.png)

这里后面的一个红框是定义头部的布局。以此类推我们的其他标签也是这么定义的：

定义左右布局的时候需要加一个浮动（float），选择从左到右，不然你的左右是不会在同一个平面的，他会换行：



![1580652844958](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580652844958.png)

使用了以后：

![1580653265241](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580653265241.png)

## 使用”<table>“元素布局：

使用table是一样的布局方式，但是我们使用table的话，就不能使用margin，而是要使用marginleft，和marginright来消除边框，在里面布局就需要使用""<tr>"",并且需要使用合并单元格:
![1580654529869](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580654529869.png)

## HTML表单的创建：

首先表单是用来获取用户输入的不同的类型数据，常用的标签有：
![1580654698534](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580654698534.png)

首先是我们常见的登录框：先定义一个from表单，然后在放置一个"<input type="">"这个位置type得到类型选择就是我们输入框的类型：
![1580655239709](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580655239709.png)

在一般的网站都会有一个选择的地方，我们称为复选框："<input type="checkbox">"

![1580655387035](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580655387035.png)

然后还有只能选择一个选项的单选框："<input type="radio">",后面的name就是为了确保我们只能选择一个，如果name不设置，或者给他赋的值不一样，我们就起不到单选的作用

![1580655672292](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580655672292.png)

下拉列表：下拉列表就是我们在一些地方可以看到点击以后会出现很多行的东西，使用方式为：

```html
<select>
    <option>x选项一</option>
    <option>选项二</option>
</select>
```

![1580656236865](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580656236865.png)



文本域：
文本域就是留言板，反馈位置的实现，我们添加文本域就可以在我们得到网页上留言什么的：

```html
<textarea cols="30" rows="30">留言板</textarea>
```

![1580656509563](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580656509563.png)

创建一个按钮：
按钮有button和submit，第一个一般是用来点击的，第二个是用来提交表单，我们注册时候需要提交，据需要使用这个标签：

```html
<input type="button" value="自定义按钮的名字">
<input type="submit" value="自定义提交按钮的名字">
```

![1580656861410](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580656861410.png)

## html和php的交互：

在这里最主要的就是action和method的使用，action是我们提交表单得到位置，method是我们提交的方式，使用post更加安全：
![1580661855508](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580661855508.png)

## html框架：

其他框架例如frameset和frame不做过多的说明，主要看内联框架：iframe：

iframe是用来对我们其他的页面进行引用，比如index.html是一个页面，我们可以使用iframe进行引用这个页面，并对这个页面进行操作：

```html
<iframe src="index.php" width="100%" height="40%"></iframe>
```

![1580663816066](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580663816066.png)

我们在这里提一个属性：target属性，这个属性是在我们的a标签使用，是用来打开连接，他可以选择在本页面点开链接" _self"，也可以选择在其他页面打开连接" _blank"

![1580664173269](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580664173269.png)

在这里我们来学“_prent”，这个属性，这个属性在有iframe标签时最好用，他的作用是在父表打开这个链接：


![1580715377446](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580715377446.png)

![1580715404198](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580715404198.png)

能够很好的看出，这个页面没有使用“_prent”，就是在当前的蓝色页面打开我们的链接，如果使用了的话就是在承载他的页面上打开。最后一个是"_top"属性，这个属性是在最底部承载的页面打开网页。

## html背景

背景标签：background：

背景颜色：bgcolor：

颜色是一个由16进制符号来定义的，这个符号由红、绿和蓝色的值（组成rgb）

![1580715864398](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580715864398.png)

红色：#FF0000 绿色：#00FF00  蓝色：0000FF

## html实体：

实体：就是将我们的一些预留符号转化为可以显示的字符串：

![1580735945020](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580735945020.png)

其他的符号可以百度

## XHTML:

xhtml是指可扩展超文本标记语言，和html4.01几乎是相同的，语法上，xhtml是更加严格更加纯净的html版本，xhtml是以xml应用的方式来定义的html，得到主流的浏览器支持，

使用XHTML是为了保证代码的完整性和良好性，简单的说就是保证我们写的代码是规范的。

### xhtml元素语法：

xhtml元素必需正确嵌套：

正确嵌套是指我们

xhtml元素必须始终关闭：

我们使用的所有标签都需要成对出现，就算是空标签也需要使用反斜杠进行闭合

xhtml元素必须小写

xhtml文档必须有一个根元素

### xhtml属性语法：

XHTMl的属性必须小写

XHTMl属性值必需要使用引号包围

XHTMl属性最小化是禁止的：

# html4和5的区别：

![1580737257064](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580737257064.png)



## 新增元素和废除元素：

![1580737479124](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580737479124.png)

![1580737629963](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580737629963.png)

## 新增的属性和废除的属性：

![1580737682983](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580737682983.png)

## 全局属性：

全局属性是指对任何元素都适用的属性

![1580737903408](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580737903408.png)

contenEditable属性：

这个属性的值为ture时就可以对该元素进行编辑，为falase时就不可以编辑：

![1580738458786](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580738458786.png)

designMode属性：只能在JavaScript中被修改编辑，是用来指定全局的元素是否能够编辑，指定值为off为不可编辑，on可以编辑。

hidden属性：通知浏览器不渲染该元素，是这个元素处于不可见的状态，但是元素中的内容还在，可以使用JavaScript来取消该元素，让里面的内容可以被显示，值为true时为不可见，为flase时是可见：

![1580738932863](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580738932863.png)

![1580739009177](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580739009177.png)

spellcheck属性：是针对input和text元素二提供的新属性。作用是拼写的语法检查，当我们拼写错误时就会在下面显示一条波浪线，火狐没有提示，我是用的谷歌就可以了


![1580739396653](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580739396653.png)

tabindex属性：

这个元素是用于使用tab键进行切换元素是使用，使用这个标签可以使元素能够用tab来进行遍历，也可以使用这个属性改变遍历顺序：

![1580739980958](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580739980958.png)

![1580740012524](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580740012524.png)

## 新增的主体结构元素：

article元素：这个元素代表文档，页面或是程序中独立的、完整的、可以独自被外部引用的内容。引用的内容可以是一篇文章，论坛的帖子，一段用户的评论或者是独立的插件，任何独立的内容都可以
article元素是可以嵌套使用的。
article元素是可以用来表示插件的。

![1580741248985](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580741248985.png)

这个可以在article元素中写一个完整的页面，说白了就是用来这个元素来添加独立的页面

section元素：
![1580741401616](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580741401616.png)

section元素适用于对文档的内容进行分块，比如在一个网页中的文章对每一段进行操作，这个时候就需要使用section而不是使用article元素，article适用于自写或引用独立的页面或其他的，article是往往是一个完整的，article不是，article是宿主，section是寄生物。

![1580742227375](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1580742227375.png)