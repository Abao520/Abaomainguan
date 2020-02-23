PHP开发特点：

对于公司来说，开发周期短（意味着效益高）

对于程序员来说，入门相对简单

web服务器端的开发语言，用来实现用户我的请求，注意区别js，js是客户端，浏览器的脚本语言

开源软件，所有操作系统稳定执行

入门简单，实现面向过程，面向对象。

支持主流的数据库，Mysql、oracle等



web的发展历程：

c/s阶段（客户端/服务器）：这个阶段网络带宽很小，这个可视化的界面是必须要安装在客户端上的。

b/s阶段（浏览器/服务器）：这个可视化的界面不需要预先安装在客户端上，使用者只需要通过浏览器来访问我们保存在服务器上的界面程序就可以了（html\css\js等）



开发环境介绍：wamp = windows+Apache+mysql+php  ；Lamp = liunx + Apache + mysql + php  这两种的区别只是他们的操作系统的位置不一样

静态代码和动态代码：

静态代码：使用HTMl、css、js、所编写的代码就是静态代码 

动态代码就是我们使用PHP编写的代码，就是动态代码。

静态网站和动态网站就是使用相对的代码来发的就是相对应的网站

静态网站：在网站设计中，纯粹HTML（标准通用标记语言的子集）格式的网页通常被称为“静态网页”，早期的网站一般都是由静态网页制作的。

静态网页的网址形式通常为：

也就是以.htm、.html、.shtml、.xml等为后后缀的。在HTML格式的网页上，也可以出现各种动态的效果，如.GIF格式的动画、FLASH、滚动字母等，这些“动态效果”只是视觉上的，与下面将要介绍的动态网页是不同的概念。

静态网站的特点：1）静态网页每个网页都有一个固定的URL，且网 页URL以.htm、.html、.shtml等常见形式为后缀，而不含“？”；

（2）网页内容一经发布到网站服务器上，无论是否有用户访问，每个静态网页都是保存在网站服务器上的，每个网页都是一个独立的文件；

（3）静态网页的内容相对稳定，因此容易被搜索引擎检索；

（4）静态网页没有数据库的支持，网站信息量很大时，完全依靠静态网页制作方式在网站制作和维护方面工作量较大，比较困难；

（5）静态网页的交互性较差，在功能方面有较大的限制 。

由于动态网页静态化的技术，一般网页前台的文件都是以htm、htm、shtml结尾。此类网站有后台，有数据库，前台页面与数据库没有任何交互的行为，此类网站与静态网站无异。可以视为静态网站。



动态网页：（1）动态网页以数据库技术为基础，可以大大降低网站维护的工作量；

（2）采用动态网页技术的网站可以实现更多的功能，如用户注册、用户登录、在线调查、用户管理、订单管理等等；

（3）动态网页实际上并不是独立存在于服务器上的网页文件，只有当用户请求时服务器才返回一个完整的网页；

（4）动态网页中的“？”搜索引擎一般不可能从一个网站的数据库中访问全部网页，或者出于技术方面的考虑，搜索蜘蛛不去抓取网址中“？”后面的内容，因此采用动态网页的网站在进行搜索引擎推广时需要做一定的技术处理才能适应搜索引擎的要求。

另外，如果扩展名为.asp但却没有连数据库，完全是静态的页面，那也是静态网站.asp只是扩展名

（5）静态网站因为没有和数据库连接，所以要有动态网站的效果就必须制作大量的网页，其中许多网页只能是虚假网页，根本实现不了动态网站的功能。

   

![1575721680545](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575721680545.png)!



打开这个文件以后我们可以看到conf这个文件夹，打开就可以找到我们的Apache的主配置文件：

![1575721894389](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575721894389.png)



其中打开以后我们就能够看到：ServerRoot ，也就是我们Apache的安装位置，因为我是安装的phpsuady

所以他就在这个里面：

![1575721875805](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575721875805.png)



Listen：这是Apache监听的端口号，端口号就是我们应用程序的服务通过这个端口来交流，这样就不会吧信息传递错误。

![1575722061988](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575722061988.png)

我们的默认端口号为80，我们只要输入我们的回环地址即可访问我们的主页面，如果在下面加一个8080端口，我们也可以用8080端口来访问我们的主页面：

![1575722685703](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575722685703.png)

![1575722702828](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575722702828.png)

接下来是我们的加载模块，即我们在登录我们的页面的时候需要记载什么东西：

![1575723159124](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575723159124.png)

加了#的为注释，我们可以通过吧#扔掉来解锁我们需要的模块。

```
ServerAdmin：是我们自己设置的，如果遇到什么问题，Apache会给我们的邮箱发送邮件。
```

![1575723275572](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575723275572.png)

```
DocumentRoot ：用于设置文档，站点的根目录，我们就可以访问我们的根目录路径来访问我们的网页。
```

![1575723435871](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575723435871.png)

DocumentRoot  和servername是相对应的，当外部通过域名来访问我们的Apache服务器的时候，他会到这个域名对应的DocumentRoot 指定的目录来找我们的文件，如果有，就返回没有就报错。



这个是我们的默认访问的页面，也就是我们如果没有根上对应的路径，直接访问的话就返回这一个页面：

![1575723790034](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575723790034.png)



我们也可以更改我们的默认页面为其他页面。

我们配置一个网站首先要配置站点的域名：

我们是用：severname来配置域名，配置好域名以后我们需要配置域名对应的站点根目录，就是我们访问这个域名的时候，我们会 到我们的服务器端的哪个盘符里找我们写好的页面，我们使用DocumentRoot “我们的绝对路径” 来配置我们的根目录。接着我们就需要配置我们的默认首页，即我们访问域名后给我们的回显页面是哪一个，利用DirectoryIndex 加我们的网页来实现默认网页的配置，然后就可以开始配置我们所需要的的一些其他东西，例如我们允许列出目录结构，开启外部配置文件等，但是要记住格式，我们要在这样的格式下配置：

<Directory "C:\phpStudy\PHPTutorial\hello">
我们想要配置的东西

 </Directory>

![1575788527166](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575788527166.png)

在host文件中需要配置域名和IP地址的对应关系，这样我们才能够访问我们的这个网页，如果我们的域名是存在的，我们就可以直接使用，不需要在本地的host文件中更改，因为他会自动使用dns帮你解析到你的服务器地址。



![1575788949002](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575788949002.png)

然后访问一次：

![1575788977428](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575788977428.png)

我们要记住，我们只要配置过文件，都需要重新启动Apache，这样才能使我们的配置起作用。



接下来我们看httpd.exe的作用：

他的位置在我们的bin目录中

![1575789688136](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575789688136.png)

他的作用是启动Apache，还可以进行Apache的服务维护，我们需要在cmd中打开它，我们进入他的目录然后使用他的语法：httpe.exe -k  stop 来关闭Apache的服务

![1575790130844](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575790130844.png)

我们在电脑上使用的时候需要用管理员的方式，这只是用在win10 的采用

还可以配置文件的语法检查：他的语法为httpd -t 然后回车就可以帮我们检查代码是否有错：

![1575791002998](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575791002998.png)



我们只需要看这个行号就可以了，根据前面的信息我们就可以找到我们的错误。一般我们的Apache启动不了的时候也可以用这个来解决。

我们接下来配置我们的环境变量，我们通过配置可以直接在初始的页面使用httpd.exe，不用进入我们的的盘符和bin目录。

我们在搜索的框里面搜索环境就可以配置我们的变量：

![1575793992259](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575793992259.png)

打开：

![1575794047127](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575794047127.png)

我们点击红色圈里的环境变量：

![1575794152247](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575794152247.png)

然后把我们bin目录的路径复制到我们的下面框里面：

![1575794588126](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575794588126.png)

然后一路确定就可以了，我们来试一试看看是否可以运行：

![1575794626461](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575794626461.png)

这样就完成了！

虚拟主机的配置：

所谓的虚拟主机就是使用一个Apache软件，配置多个主机（域名），就和我们的虚拟机是一样的，我们配置多个主机在我们的httpd-vhost.exe中进行配置，默认是没有开启的，想要开启的话，我们需要在主扩文件里先配置：

![1575795111613](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575795111613.png)

我们将他的启用，直接去点#然后重启Apache就可以继续配置了。

在扩展配置文件中配置多个主机：

![1575795340166](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1575795340166.png)

在这里面我们的有配置的格式和案例，我们可以直接全部删掉，然后就可以按照我们自己的方式来配置我们的虚拟主机了：

我们配置第一个虚拟主机：

主机A: 域名为：www.one.com 站点根目录为：C:\phpStudy\PHPTutorial\one   默认首页为：one.html  允许列出目录结构 不允许110.11..110.110的访问

主机B:域名为：www.two.com  站点根目录为：C:\phpStudy\PHPTutorial\two   默认首页为two.html，不允许120.120.120.120的ip访问：

![1576062912943](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576062912943.png)

这就是基本的配置，我们在下面的主机b也是相同的配置办法。接下来我们利用我们的额httpd.exe来检测我们的语法是否有错误：

![1576063004060](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576063004060.png)

ok语法没错我们就可以重启我们的Apache来访问我们的域名（在这之前我已经用host文件解析了我们的域名）：

![1576063097123](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576063097123.png)

![1576063130074](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576063130074.png)

这样我们就完成了虚拟主机的配置。



接下来看Apache的外部配置文件：

我们的Apache除了我们的httpd.conf 和httpd-vhosts.conf这两个配置文件以外，还可以在另外一个文件中书写我们的Apache配置，这个文件就是外部配置文件，默认文件名为：.htaccess

首先我们要开启我们的外部文件：在我们的主机配置里面配置我们创建一个新的虚拟主机：

![1576064911265](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576064911265.png)

我们只需要在我们的网站特性里面加入这一条语句，就可以开始创建我们的.htaccess文件，但是我们不能直接通过更名的方式来创建，而是要通过我们的编辑器来创建，我们需要把这个文件保存到我们的网站根目录里面：

![1576065219725](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576065219725.png)

这样我们就成功的创建了我们那的.htaccess文件，我们在我们的目录里也可以看到这个文件。

我们接下来看看这个文件的作用，我们刚刚配置Apache的时候，每次配置都需要重新启动我们的Apache，有一点麻烦，但是我们在这个文件里面更改的话就不要重启我们的Apache，

![1576065692912](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576065692912.png)

![1576065706783](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576065706783.png)

![1576065720696](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576065720696.png)

这样我们就可以在我们的htaccess的文件中配置，这就是我们.htaccess文件的主要作用，除此以外我们还可以使用它来做域名重定向、自定义错误提示页面等，我们就来尝试错误页面显示的自定义，他的语法是：ErrorDocument  404（#错误代码）/错误提示文件的路径   如下：

![1576067182050](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576067182050.png)

其中404的文件是我们自定义的，他存放的位置也是我们的网站根目录里面：

![1576067255466](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576067255466.png)



除此以外我们可以自定义404文件的内容：

![1576067286207](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576067286207.png)

我们访问一次我们的错误页面：

![1576067320728](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576067320728.png)

这就是我们自定义的界面。我们以后再讲解我们的URl重定向。

接下来我们来了解mysql的相关知识：

安装我的过程我们就不管了，这个百度有，而且我们的PHPStudy也会帮我们打包好。我们先来在配置好环境变量以后就可以直接使用我们的cmd命令进入我们的数据库，他的登录命令为：MySQL -u 你的数据库名字 -p  然后他会要求输入密码，输入以后我们就进入了我们的数据库如下：

![1576068527350](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576068527350.png)



这就是我们的登录方式，当然也可以通过可视化的图形界面登录：

![1576068574183](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576068574183.png)

这里我穿插讲一下PHP的安装，我们的PHP就是一个软件包，不需要安装，只需要在Apache启动的过程中来加载我们的PHP功能模块即可，我是直接使用的PHPstudy：

![1576068804667](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576068804667.png)

这里面是可以选择的。

我们之所以安装这个PHP是因为Apache的默认只可处理我们的HTML文件，我们安装了PHP文件就可以让我们的Apache支持php文件的请求，我们在我们的主配置文件里加载我们的PHP和服务的配置：![1576069946524](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576069946524.png)

重启我们的Apache，这样我们在使用的时候就可以启动我们的PHP了。我们来加载一个PHP网页看是否启动了我们的PHP服务：

![1576069661179](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576069661179.png)

我们访问一次：

![1576069694726](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576069694726.png)

这样就表示我们成功的开启了我们的PHP服务。

然后我们就来加载php的配置文件：

PHP文件位于我们的PHP文件目录中：

![1576070324162](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576070324162.png)

这两个文件其实不是我们的配置文件，我们根据我们的实际情况选择不同的模板文件，处于开发的时候就选择我们的development文件，处于上线的阶段就使用我们的production的文件。我们现在就将我们的第一个改为pip-ini就可以了，为了我们的安全，我们可以复制一下再改名字：

![1576070670701](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576070670701.png)

接下来我们就设置它，还是在我们Apache的主配置文件中：

![1576070824721](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576070824721.png)

这个文件的配置不会影响我们的php，只是没法使用更多的功能，只能使用他默认的模块，我们创建了一个PHP文件，由于PHP的模块必须由Apache来加载，所以我们必须使用域名来访问我们的PHP文件，我们如果直接点击右键选择浏览器运行的话是不会运行的：

![1576076072040](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576076072040.png)

![1576076087955](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576076087955.png)

这样我们一定要使用域名来使用，我们的PHP文件也要放在我们的根目录下。

我们可以使用PHPinfo来加载我们的配置文件：

![1576076629391](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576076629391.png)

以后我们加载了我们的某些功能模块，我们就可以在这个文件来查看。

我们接下来设置我们的时间，一般来说php的默认设置是0时区的时间，我们是东八区所以我们需要设置好时间，下面是我们默认的时间：

![1576077060542](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576077060542.png)

我们发现刚好差了8小时，所以我们要在php.ini中设置，我们找到[date]：

![1576077338482](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576077338482.png)

更改为如下我们就可以使用我们的时区（prc是中国的缩写），然后重启Apache，再打开我们的PHP文件：

![1576077539981](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576077539981.png)

这样我们的时间就配置好了。

# PHP的学习

php是一种服务器端嵌入html的脚本语言，嵌入html的意思就是我们可以使用php标签（<?php...?>）将我们想要动态输出的数据嵌入到html代码，所以从这个方面来说我们的php是动态脚本语言，我们怎么来理解我们的php呢？我们知道，html是一个静态页面，我们不能够使用它来传输我们的数据，但是我们的php是动态的，是可以传输数据的，我们在一个静态的代码里面插入php代码，我们这个页面的格式任然是一个html页面，只是我们使用了php来做到了一些操纵而已，比如这个：

![1576079298775](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576079298775.png)

![1576079320179](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576079320179.png)

我们以后echo的地方就是从我们的数据库里面获取数据，而不是现在这样的写死。

## PHP的语法规则

因为我们的php配置时我们在Apache的主配置文件中配置了我们的PHP文件的扩展名为.php，所有我们所有的PHP文件都是以.php来结尾，你也可以在配置中自定义你的结尾，但是一般都是以.php；其次就是我们的PHP文件只能通过域名来访问。PHP文件是不能包含中文，我们的访问路径也是不能有中文；我们的PHP的每一条语句后面都需要有一个‘ ；’ ，我们的js就可以省略；PHP中的函数名，变量名，要大小写敏感。其余的函数名，方法名，类名都不区分大小写，但是建议还是区分一下。

## PHP标记

PHP存在4种标签：

<?php....?>格式：

![1576148548700](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576148548700.png)

script格式：

![1576148867149](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576148867149.png)

短格式：<?....?> 但是短格式默认是不开启，我们要在php.pip中进行配置：

![1576149063919](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576149063919.png)

![1576149149726](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576149149726.png)

最后一种是asp格式：<%...%> 格式：

![1576149219031](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576149219031.png)

提示：我们在使用短格式的时候需要配置中开启。如果我们的整个文档都是php代码的话我们结束标签建议不写。如果有html代码的话就加上结束标签，并且如果我们有结束符的话最后一行代码可以不加分号。

## PHP的注释

单行注释：//

多行注释：/**/

![1576149564354](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576149564354.png)

# 变量及操作

## 概念

程序语言就是对内存进行操作（堆内存进行读写的操作）

变量是内存中用于临时存储数据的空间，这个空间有一个名字，这个名字就是变量名，变量名就是用于对这个内存中的数据引用的。简单来说，我们要把硬盘中的某一条数据取出来，我们首先就在内存中分一块空间出来，我们自定义这个空间的名字（变量名）然后我们就把我们要取的那条数据放在这个变量名里面，然后通过内存将这条数据放在我们的cpu里面执行，  我们执行的时候直接引用这个变量名就可以直接使用我们的数据。

## 声明

语法：$变量名=值

说明：PHP中的变量名只能是$开头，变量名这能包含字母、数字、下划线，并且不能以数字开头，不能个和关键字重名，比如我们定义变量进行加减：

![1576150934418](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576150934418.png)

这就是变量的定义。

## 修改变量的值

更改变量的话直接覆盖就可以了：

![1576151298947](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576151298947.png)

删除变量的语法为：unset（$...）：

![1576151427480](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576151427480.png)

我们会发现我们第一次可以输出，但是第二次我们的变量被删了，所以就会报错

## 可变变量

接下来我们来看可变变量：

![1576152014794](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576152014794.png)

作用：用一个变量访问另外一个变、通过一个变量创建另一个变量：

![1576152352032](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576152352032.png)

通过这样的方式我们就可以创建变量。

## 预定义变量

我们php帮我们预先定义了一组变量，这些变量在我们的不同需求中使用：

![1576152972151](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576152972151.png)

$_GET 

$_POST

$_REQUEST

这三个变量是用来接收前台的表单使用，分别是接收get方式提交、post方式提交、两种方式都可以接收。

$_SERVER 记录了服务器端和客户端的相关信息：

![1576153158621](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576153158621.png)

$_COOKIE
一种会话技术

$_SEEION
一种会话技术

$_FILES
记录用户上传的文件信息

$GLOBAL
记录全局变量

# 内存的原理

## 内存结构

我们先拿一个图来形象的表示他：

![1576154377464](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576154377464.png)

栈区
这个区域是保存的是变量名 （我们术语叫”引用“）对于cpu来说，他的读取速度最快。

堆区
存储的复杂的数据，数组、对象、字符串。



数据段
存储的简单的数据，例如：整型、浮点型、布尔值。但是我们的字符是不在这里面，

代码段
存储的是源代码对应的机器指令（高级语言代码转换为机器语言，机器语言转换为高级语言的地方）



输出缓存
只要是遇到了输出命令，都会将所要输出的数据都要放在我们的这会输出缓存区。



php嵌入到我们的html的执行过程

当php模块在处理的时候，只会处理我们的php标签内的代码，而不会处理html ，在这里面的html只相当于字符串。

## PHP的传值方式

赋值传值：使用一个变量a为另一个变量b赋值时传递的是a的值，在我们的php中默认的使用赋值传值的有：整型，浮点型、布尔值、字符串等

![1576323272688](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576323272688.png)

引用传值：使用一个变量a为另一个变量b赋值时传递的是a的地址而不是值：

## 常量

常量是一种特殊的变量，也适用于储存数据的，但是常量只要定义我们就不能进行修改，也不允许删除，他定义的数据类型也只能是基本的常量，他的语法为:

```php
<?php
    defin(常量，值);

```

 或者：const 常量名 =值

![1576324394462](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576324394462.png)

define和const的区别：define定义的常量可以在我们的分支结构中可以定义，但是const不行，define定义的常量是可以自定义大小写，一般的常量是有区分的，一般定义常量是用全部大写，这样比较好区分我们的变量和常量。他的语法为：

define （key，values，true）我们写了true的话就是不区分大小写。我们判断一个常量是否存在使用：

```php
define ("pi",123456);
$result = defined("pi");
var_dump($result);
```

![1576325235836](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576325235836.png)

我们使用get_defined_constants();这个函数来输出我们的所有已经定义的变量：

![1576325612995](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576325612995.png)