---

typora-copy-images-to: 图片
---

# 什么是SQL

SQL是一种结构化的查询语句，使用它可以让我们拥有访问数据库的能力，它是一种标准的ANSI的标准计算机语言，简单的来说就是我们可以使用这种语句对数据库进行操作，什么是数据库？数据库就相当于一个仓库，我们在网页上接收的数据就需要保存在我们的数据库中，所以我们一般就需要对数据库进行数据操作。这也是我们为什么需要学习SQL语句的原因。

## SQL能够做什么？

sql可以对数据库进行查询，取回数据、插入数据、删除数据、变更数据、创建新的数据库、创建新的数据表...总的一句话来说：增删涂改他都能够做，这就是我们SQL的作用。我们在学习之前要把我们得数据库和SQL语句区分开，数据库是数据库，他是存储的工具，SQL是SQL他是查询数据的东西，不能够混为一谈。我们的SQL可以和 MS Access、DB2、Informix、MS SQL Server、Oracle、Sybase 以及其他数据库系统协同使用。但是不是说我们的SQL语句是唯一的，他也有许多的版本。除了SQL的标准外，大部分的数据库程序都有他们自己的私有扩展。

## 我们在哪儿使用SQL？

说到这估计很多人还是对我们的SQL的用处不太了解，我们刚刚提到这么多，无非就是在说SQL的用处，但是我们在哪儿使用的到呢？我们常见的地方就是我们网站中，比如我们登陆的时候，我们的前端把我们的数据发送到我们的数据库中进行比对，如果我们的数据匹配则成功登陆，这里就是我们体现数据库的作用的地方，我们能够把我们的数据存放在这个地方，但是我们的网站在进行数据比对时，是怎么告诉我们的数据库呢？这就是SQL的功劳了。我在给大家普及一下我们带有数据库的网站需要哪些东西：

首先是数据库程序（RDBMS）：比如MySQL、SQLServer、MS Access等，我们的数据库程序就是指数据库管理系统，他是SQL的基础，同样也是我们现代所有数据库系统的基础，他的数据储存在数据中的tables中，tables是数据项的集合，由表和列组成。

## RDBMS术语

- **数据库:** 数据库是一些关联表的集合。
- **数据表:** 表是数据的矩阵。在一个数据库中的表看起来像一个简单的电子表格。
- **列:** 一列(数据元素) 包含了相同类型的数据
- **行：**一行（=元组，或记录）是一组相关的数据，例如一条用户订阅的数据。
- **冗余**：存储两倍数据，冗余降低了性能，但提高了数据的安全性。
- **主键**：主键是唯一的。一个数据表中只能包含一个主键。你可以使用主键来查询数据。
- **外键：**外键用于关联两个表。
- **复合键**：复合键（组合键）将多个列作为一个索引键，一般用于复合索引。
- **索引：**使用索引可快速访问数据库表中的特定信息。索引是对数据库表中一列或多列的值进行排序的一种结构。类似于书籍的目录。
- **参照完整性:** 参照的完整性要求关系中不允许引用不存在的实体。与实体完整性是关系模型必须满足的完整性约束条件，目的是保证数据的一致性。

- **表头(header)**: 每一列的名称;
- **列(col)**: 具有相同数据类型的数据的集合;
- **行(row):** 每一行用来描述某条记录的具体信息;
- **值(value):** 行的具体信息, 每个值必须与该列的数据类型相同;
- **键(key)**: 键的值在当前列中具有唯一性。

## SQL语句的注意事项

我们的mysql的默认是需要我们在每条 SQL 命令的末端使用分号 ，但是我们可以设置为不需要，分号是数据库中分隔每条SQL语句的标准，我们把SQL语句分为两部分：数据操作语言和数据定义语言。

数据操作语言（部分/常用）：

- SELECT - 从数据库表中获取数据
- UPDATE - 更新数据库表中的数据
- DELETE - 从数据库表中删除数据
- INSERT INTO - 向数据库表中插入数据

数据库定义语言（同上）：

- CREATE DATABASE - 创建新数据库
- ALTER DATABASE - 修改数据库
- CREATE TABLE - 创建新表
- ALTER TABLE - 变更（改变）数据库表
- DROP TABLE - 删除表
- CREATE INDEX - 创建索引（搜索键）
- DROP INDEX - 删除索引



# MYSQL数据库

首先我们登录我们的mysql，登录的语法为：

"MySQL " 然后就会要求我们输入密码，这样我们就能够登录上我们的数据库了：

![1576235259215](C:\Users\15749\Desktop\typora图片\1576235259215.png)

 使用

```mysql
 show databases;
```

来列出我们数据库管理系统的数据库列表：

![1576235351881](C:\Users\15749\Desktop\typora图片\1576235351881.png)

我们使用 "

```mysql
use 你想打开的数据库名;
```

"来选择我们要操作的数据库，然后show我们这个库里面的表单，我们以test_db为例子：

![1576235465476](C:\Users\15749\Desktop\typora图片\1576235465476.png)

我们可以看到我们的test_db库中有三个表单，我们可以从查询这三个表中的数据，使用 

```mysql
show columns from 你想要查询的表单 ;
```

 但是我们这三个表里都没有东西：

![1576235799325](C:\Users\15749\Desktop\typora图片\1576235799325.png)

我们很容易看到我们这个表单里的东西。（有这些东西是我是上次的烂尾楼哈哈哈），我们可以看其他的表中是否有数据：

![1576235924876](C:\Users\15749\Desktop\typora图片\1576235924876.png)

然后我们可以使用

```mysql
show index from 你想要查询的表单;
```

 来显示这个表的详细索引信息，我们还是以tb_emp4为例：

![1576236055743](C:\Users\15749\Desktop\typora图片\1576236055743.png)

## MySQL PHP语法

mysql可以运用很多语言， PERL, C, C++, JAVA 和 PHP ，这些语言中PHP是开发中运用最广的，所以我们就在PHP的基础上来使用我们的mysql。

### mysql的连接

我们刚才使用的就是一二进制方式来连接我们的数据库，我们可以使用PHP脚本来连接我们的mysql，PHP中提供了" mysqli_connect() " 来为我们连接，包含六个参数：
host：主机的IP地址
username：mysql的登录名
password：mysql的登录密码
dbname：我们使用的数据库
port：mysql数据库我的服务端口
socket：规定 socket 或要使用的已命名 pipe 

 mysqli_close() ：用来断开我们的连接只有一个参数，语法为："bool mysqli_close ( mysqli $link )",我们就来试试连接我们的数据，使用php：

![1576236994097](C:\Users\15749\Desktop\typora图片\1576236994097.png)

## mysql创建数据库

我们在登陆了我们的mysql服务以后，就可以使用我们的" create "来创建，语法为：

```mysql
CREATE DATABASE 数据库名;
```

 (虽然没有大小写区分，但是还是为了我们的辨别使用大写吧)，我们来创建一个gitchat 的数据库：

![1576237356894](C:\Users\15749\Desktop\typora图片\1576237356894.png)

这样我们就创建了这样的一个数据库，这里我提一下，我们现在是root用户所以不会出现权限不够，但是我们有些时候没有权限。

## PHP创建数据库

我们使用php看来创建，语法为

```php
mysqli_query(connection,query,resultmode); 
```

这里面的三个参数为 *connection*（规定使用MySQL连接） *query*（规定我们的查询字符串） 、 *resultmode*（这个可以不写，就使用默认的） 我们就使用这个语句来创建我们的test数据库：

![1576238956118](C:\Users\15749\Desktop\typora图片\1576238956118.png)

我们可以看到我们的gitchat和test被成功创建

接下来我们学习删除数据库，语法为：

```mysql
DROP DATABASE 数据库名;
```

我们来实验一下，例如我们删除test_db这个数据库：

![1576239114339](C:\Users\15749\Desktop\typora图片\1576239114339.png)

相应的，我们使用php来删除我们的test库，只需要把我们的$sql的命令改为""DROP DATABASE 数据库名""就可以了：

![1576239244389](C:\Users\15749\Desktop\typora图片\1576239244389.png)

![1576239285029](C:\Users\15749\Desktop\typora图片\1576239285029.png)

我们发现已经成功删除了，当然对应的返回语句也要改一下。

## MySQL连接指定的数据库

他的语法为："mysqli_select_db(connection,dbname);" 第一个参数是必须使用MYSQL的连接，第二个是我们要指定的数据库名字：

![1576239709343](C:\Users\15749\Desktop\typora图片\1576239709343.png)

mysql的数据类型：
mysql中定义的数据字段的类型对数据库的优化起到非常重要的作用，mysql支持 多种类型，我们把它分为三类：数值、日期/时间、字符串和类型。我们首先看数值型：

MySQL支持所有标准SQL数值数据类型，这些类型包括严格数值数据类型(INTEGER、SMALLINT、DECIMAL和NUMERIC)，以及近似数值数据类型(FLOAT、REAL和DOUBLE PRECISION)。

关键字INT是INTEGER的同义词，关键字DEC是DECIMAL的同义词。

 BIT数据类型保存位字段值，并且支持MyISAM、MEMORY、InnoDB和BDB表。 

 作为SQL标准的扩展，MySQL也支持整数类型TINYINT、MEDIUMINT和BIGINT。下面的表显示了需要的每个整数类型的存储和范围。 

![1576239994562](C:\Users\15749\Desktop\typora图片\1576239994562.png)

日期和时间型：
表示时间值的日期和时间类型为DATETIME、DATE、TIMESTAMP、TIME和YEAR。每个时间类型有一个有效值范围和一个"零"值，当指定不合法的MySQL不能表示的值时使用"零"值。

![1576240045508](C:\Users\15749\Desktop\typora图片\1576240045508.png)

字符串类型：
字符串类型指CHAR、VARCHAR、BINARY、VARBINARY、BLOB、TEXT、ENUM和SET。该节描述了这些类型如何工作以及如何在查询中使用这些类型。

![1576240087496](C:\Users\15749\Desktop\typora图片\1576240087496.png)

CHAR 和 VARCHAR 类型类似，但它们保存和检索的方式不同。它们的最大长度和是否尾部空格被保留等方面也不同。在存储或检索过程中不进行大小写转换。

BINARY 和 VARBINARY 类似于 CHAR 和 VARCHAR，不同的是它们包含二进制字符串而不要非二进制字符串。也就是说，它们包含字节字符串而不是字符字符串。这说明它们没有字符集，并且排序和比较基于列值字节的数值值。

BLOB 是一个二进制大对象，可以容纳可变数量的数据。有 4 种 BLOB 类型：TINYBLOB、BLOB、MEDIUMBLOB 和 LONGBLOB。它们区别在于可容纳存储范围不同。 

 有 4 种 TEXT 类型：TINYTEXT、TEXT、MEDIUMTEXT 和 LONGTEXT。对应的这 4 种 BLOB 类型，可存储的最大长度不同，可根据实际情况选择。

**总结起来，有几点：**

- 经常变化的字段用 varchar

- 知道固定长度的用 char

- 尽量用 varchar

- 超过 255 字符的只能用 varchar 或者 text

- 能用 varchar 的地方不用 text

  

## 数据表的创建

我们就开始在我们的gitchat这个数据库中创建我们的数据表，他的通用语法为:"CREATE TABLE table_name (column_name column_type);"  我们这里设计一个自增的功能，我们要用到：AUTO_INCREMENT 来定义我们的自增主键，他有两种定义的办法，一种是在我们的定义是时就设置，还有就是在最后设置，这个主键的作用很明显，就是一个自增的作用，我们在使用的时候可以为我们的列表增加序号，我们先来看第一种：
我将源代码写下来:

```mysql
use GITCHAT;
CREATE TABLE user(
    id INT NOT NULL PRIMAry KEY AUTO_INCREMENT,
    name VARCHAR(40）NOT NULL
                 );
    
```

![1576253892651](C:\Users\15749\Desktop\typora图片\1576253892651.png)

成功创建以后我们就给他插入一个值：

```mysql 
INSERT INTO user(id,name) VALUES("1","北美第一突破手");
```

因为今早不小心删掉了我的user表单，只好新建了一个，然后我们把我们的数据插入：

![1576294406441](C:\Users\15749\Desktop\typora图片\1576294406441.png)



接下里就到了我们的关键，我们在插入一条数据：

```mysql
INSERT INTO student (name,age) values ("GITCHAT","19");
```

![1576294530882](C:\Users\15749\Desktop\typora图片\1576294530882.png)

我们发现我们的数据成功加入，并且在这之前我们并没有给id赋值，这就是主键的自增。当然只是在定义的时候设置，我们也可以定义完了以后在设置我们再来一个表单如下：

```mysql
CREATE TABLE student2(
    name VARCHAR(5) NOT NULL,
    age INT NOT NULL
    );
```

![1576295776632](C:\Users\15749\Desktop\typora图片\1576295776632.png)

我们可以发现我们的KEY是没有设置的，接下来我们使用：

```mysql
 alter table student2 add id int not null primary key Auto_increment;
```

来实现主键的添加：

![1576295812249](C:\Users\15749\Desktop\typora图片\1576295812249.png)

这样我们就成功的添加了我们的自增主键为id，我们来试验一下：

![1576295953422](C:\Users\15749\Desktop\typora图片\1576295953422.png)

我们的第二次的id没有设置，也自动的帮我们增加了，当然我们的id初始值是可以改变的，我们可以设置为3，然后他还是会帮我们从3开始增加。

接下来就是删除表单：语法为

```mysql
DROP TABLES table_name ;
```

,接下来我们删除我们的表单：

![1576250278887](C:\Users\15749\Desktop\typora图片\1576250278887.png)

我们就删除了我们的表。关于在php中进行建表和删表都是更改我们的$SQL就可以了：

![1576250518894](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\1576250518894.png)

我们检查一下：

![1576250602322](C:\Users\15749\Desktop\typora图片\1576250602322.png)

![1576250842981](C:\Users\15749\Desktop\typora图片\1576250842981.png)

成功。

我们接下来看插入数据的方法：语法为

```mysql
INSERT INTO 你的表单名 （"你定义的列名","你定义的列名","你定义的列名","你定义的列名","你定义的列名"）VALUES ("插入的值","插入的值","插入的值","插入的值")  ：
```

![1576251159650](C:\Users\15749\Desktop\typora图片\1576251159650.png)

![1576251185706](C:\Users\15749\Desktop\typora图片\1576251185706.png)

```mysql
SELECT column_name,column_name FROM table_name [WHERE Clause] [LIMIT N][ OFFSET M]
```

- 查询语句中你可以使用一个或者多个表，表之间使用逗号(,)分割，并使用WHERE语句来设定查询条件。
- SELECT 命令可以读取一条或者多条记录。
- 你可以使用星号（*）来代替其他字段，SELECT语句会返回表的所有字段数据
- 你可以使用 WHERE 语句来包含任何条件。
- 你可以使用 LIMIT 属性来设定返回的记录数。
- 你可以通过OFFSET指定SELECT语句开始查询的数据偏移量。默认情况下偏移量为0。

比如我要查询我们student表中的name为北美第一突破手的所有信息的语句为：

```mysql
SELECT * FROM student WHERE name = "北美第一突破手";
```

![1576305331488](C:\Users\15749\Desktop\typora图片\1576305331488.png)

我们也可以换一种：比如我要查询我们student表中的id为2的所有信息的语句为：

```sql
SELECT * FROM student WHERE id = "1";
```

![1576305484261](C:\Users\15749\Desktop\typora图片\1576305484261.png)

这是where的使用符号，where的语句是大小写不敏感的，要是需要区分大小写就需要加上 BINARY  ：

| 操作符  | 描述         |
| ------- | ------------ |
| =       | 等于         |
| <>      | 不等于       |
| >       | 大于         |
| <       | 小于         |
| >=      | 大于等于     |
| <=      | 小于等于     |
| BETWEEN | 在某个范围内 |
| LIKE    | 搜索某种模式 |

我们的where还可以使用and和or来增加更多的条件，比如我要找id = 2 并且name=北美第一突破手 的信息，我们就可以构造:

```mysql
SELECT * FROM student WHERE id = "1" AND name = "北美第一突破手"; 
```

![1576305930231](C:\Users\15749\Desktop\typora图片\1576305930231.png)

我们接着查找所有信息，id=2 或者id =1 ：

```sql
SELECT * FROM student WHERE id = "1" OR id = "2";
```

![1576306057381](C:\Users\15749\Desktop\typora图片\1576306057381.png)

我们就查到了我们所有满足条件的额信息。我们现在在里面加两条数据，但是我们要区分大小写：

![1576306351736](C:\Users\15749\Desktop\typora图片\1576306351736.png)

我们再来查一次我们的数据，我们的要求是查询name为abc的所有数据：

![1576306444348](C:\Users\15749\Desktop\typora图片\1576306444348.png)

我们发现我们的数据库告诉我们了两个数据，我们只查询abc但他把ABC的数据也放出来了，这样就不是我们想要的结果了，所以我们为了避免这种情况我们就需要加上限定语句 BINARY ，我们还是上面的要求重新查询一次，使用我们的限定语句：

```sql
SELECT * FROM student WHERE BINARY name = "abc";
```

![1576306707431](C:\Users\15749\Desktop\typora图片\1576306707431.png)

我们就只查到了满足我们需求的信息了。

## SQL UPDATAE 更新

我们如果需要更新或者修改某些表里面的数据时，我们使用 SQL UPDATE的语句来进行更新，他的语法为：women

```mysql
UPDATE table_name SET field1=new-value1, field2=new-value2
[WHERE Clause]
```

我们来更新我们id =4 的信息：

```sql
UPDATE student SET name = "cde",age = "16" WHERE id = "4";
```

![1576307757217](C:\Users\15749\Desktop\typora图片\1576307757217.png)

这样我们成功的更新了我们的数据。但是我们有时候只是想要更改一点就可以了，那么我们下面的语句就可以完成：

```sql
UPDATE 表名 SET 想要修改数据的名字 = REPLACE(想要修改数据的名字 , '旧数据', '新数据') WHERE id = 4; 
```

我们接下来还是id = 4 的信息，我们只要改他的name的值就可以了：

```sql
UPDATE student SET name = REPLACE(name, 'cde', '阿宝面馆') where id=4; 
```

![1576308048487](C:\Users\15749\Desktop\typora图片\1576308048487.png)

这样我们就完成了数据的修改。我们数据除了增加还有删除，我们就使用我们的DELETE来删除
他的语法为：

```sql
DELETE FROM table_name WHERE = "";
```

我们删除我们student中id=3的数据：

```sql
DELETE FROM student WHERE id = 3 ;
```

![1576308569760](C:\Users\15749\Desktop\typora图片\1576308569760.png)

我们就可以做到删除数据。



## SQL LIKE 子句

我们到现在已经知道了，使用seiect来读取我们数据并且可以使用我们的where做限定，但是有的时候我们需要获取字段里包含某些条件的数据，那么我们就可以使用LIKE来限定，这个和我们的正则有点相似，也是来进行匹配，我们的LIKE中使用%来代替任意字符，如果没有这个%的话，我们的LIKE语句就和 = 没有区别，我们看到我们的语法：

```sql
SELECT 你想要查询的数据 WHERE 那一列 LIKE "%包含的字符" AND "%包含的字符"
```

-  你可以在 WHERE 子句中指定任何条件。
-  你可以在 WHERE 子句中使用LIKE子句。
-   你可以使用LIKE子句代替等号 =。
-   LIKE 通常与 % 一同使用，类似于一个元字符的搜索。
-  你可以使用 AND 或者 OR 指定一个或多个条件。
-  你可以在 DELETE 或 UPDATE 命令中使用  WHERE...LIKE 子句来指定条件。我么可以删除所有含有我们匹配符号的数据

我们在这之前先添加两条数据：

![1576309544005](C:\Users\15749\Desktop\typora图片\1576309544005.png)



然后使用我们的LIKE来进行匹配删除：

```sql
DELETE  FROM student WHERE name LIKE "%de";
```

![1576309535658](C:\Users\15749\Desktop\typora图片\1576309535658.png)

这样我们就name结尾为de的所有数据删除了，我们也可以使用LIKE来进行查找，相当于，模糊查找一样,我们就查找id为任何一个值的所有数据：

```sql
SELECT * FROM student WHERE id LIKE "%";
```

![1576309704173](C:\Users\15749\Desktop\typora图片\1576309704173.png)

j这就是LIKE的用法。当然我们的SQL还提供了其他的字符串匹配的方法：

| 符号 | 用处                                              |
| ---- | ------------------------------------------------- |
| %    | 代表0个或者多个任意的字符，如果是中文使用%%来代替 |
| _    | 代表一个任意一个字符，                            |
| [ ]  | 代表匹配在这个括号里的任何一个字符                |
| [^]  | 代表不匹配任何一个不再这里面的字符                |

我们来试一下：
![1576310265282](C:\Users\15749\Desktop\typora图片\1576310265282.png)

我们首先使用"_"这个来匹配：

```sql
SELECT *FROM student WHERE name LIKE "abcde_";
```

![1576310452224](C:\Users\15749\Desktop\typora图片\1576310452224.png)

我们接下俩看"[]"这个匹配：

```sql
SELECT * FROM student WHERE age LIKE "1[9765]";
```



## MYSQL UNION操作符

MySQL UNION适用于连接两个查询语句的内容，集合到一个集合中，我们在注入的时候也称为联合查询，他的语法为：

```sql
SELECT 查询的列名 FROM 要检索的数据表 WHERE = "限定的字符" UNION [ ALL | DISTINCT] SELECT 列名 FROM 要检索的数据表 WHERE = "限定的字符";

```

**DISTINCT:** 可选，删除结果集中重复的数据。默认情况下 UNION 操作符已经删除了重复数据，所以 DISTINCT 修饰符对结果没啥影响。

**ALL:** 可选，返回所有结果集，包含重复数据。我们来试一试这个查询方式：

![1576312740879](C:\Users\15749\Desktop\typora图片\1576312740879.png)

我们来查询这两个表中的 id，age，name，并且age为18的人：

```sql
SELECT id,age,name FROM student WHERE age = 18 UNION ALL SELECT id, age,name FROM student2  WHERE age =18 ORDER BY age;
```

![1576313294561](C:\Users\15749\Desktop\typora图片\1576313294561.png)

这个查询语句的作用就是把多个表中的数据查出来，我们也可以一个一个查，但是就没有这么方便，并且还要汇总，所以我们就使用这个。

## 排序语法

ORDER BY 语句用于根据指定的列对结果集进行排序。怎么来理解呢？就是我们查到数据以后按照那一列的内容进行排序，比如我们使用id来排序如下：（我们默认是升序）

```sql
SELECT * FROM student ORDER BY id;
```

![1576318934922](C:\Users\15749\Desktop\typora图片\1576318934922.png)

我们使用name来排序：

```sql
SELECT * FROM student ORDER BY name;
```

![1576318991102](C:\Users\15749\Desktop\typora图片\1576318991102.png)

这就是他的作用。如果您希望按照降序对记录进行排序，可以使用 DESC 关键字。如下：

```sql
SELECT * FROM student ORDER BY id DESC;
```

![1576319095203](C:\Users\15749\Desktop\typora图片\1576319095203.png)

MySQL 排序我们知道从 MySQL 表中使用 SQL SELECT 语句来读取：

**MySQL 拼音排序**

如果字符集采用的是 gbk(汉字编码字符集)，直接在查询语句后边添加 ORDER BY：

```sql
SELECT * 
FROM runoob_tbl
ORDER BY runoob_title;
```

如果字符集采用的是 utf8(万国码)，需要先对字段进行转码然后排序：

```sql
SELECT * 
FROM runoob_tbl
ORDER BY CONVERT(runoob_title using gbk);
```

## MySQL GROUP BY 语句 

### GROUP BY 语法

```sql
SELECT 我们想要谁来排序, SUM和其他的计数函数(用于计数的列) FROM table_name WHERE column_name operator value GROUP BY 我们想要谁来排序;
```



GROUP BY 语句根据一个或多个列对结果集进行分组,在分组的列上我们可以使用 COUNT, SUM, AVG,等函数。 简单的来说就和空间一样，我们今天有哪些人访问了我们的空间，然后访问了多少次，分别记录在一个列中，然后我们就使用SUM计算函数，使用GROUP BY 进行排列，我们举例说明，我们先做一个表 ：

![1576320385617](C:\Users\15749\Desktop\typora图片\1576320385617.png)

我们用来记录我们的访客，然后添加数据：

![1576320433019](C:\Users\15749\Desktop\typora图片\1576320433019.png)

我们可以看出小明这两天都有访问，我们就可以使用GROUP BY 和SUM 函数来集合我们的每一列：

```sql
SELECT name,sum(times) FROM look GROUP BY name;
```

![1576320611490](C:\Users\15749\Desktop\typora图片\1576320611490.png)

我们就这两天所有人的访问给算出来了，当然我们如果只看小明的就可以直接用WHERE来限定他：

```sql
SELECT name,sum(times) FROM look WHERE name = "小明" GROUP BY name;
```

![1576320876685](C:\Users\15749\Desktop\typora图片\1576320876685.png)

我给大家讲一下另外两个函数的作用，SUM是计算和的意思、COUNT 就是统计我们的表中有多少条数据，一行算一条数据。AVG计算平均值的意思。

![1576321383472](C:\Users\15749\Desktop\typora图片\1576321383472.png)

![1576321430074](C:\Users\15749\Desktop\typora图片\1576321430074.png)



## MySQL连接符号

在讲解连接符号的时候我们可以使用我们先了解一下我们的各种键的约束：
约束用于限制加入表的数据的类型。可以在创建表时规定约束（通过 CREATE TABLE 语句），或者在表创建之后也可以（通过 ALTER TABLE 语句），这是两种办法，由于我习惯了在建表的时候就将我们的约束写好，所以下面的演示都是基于在建表时的操作。

我们将主要探讨以下几种约束：

- NOT NULL 非空约束，我们在定义数据表的时候为了使我们的表单内的数据不为空，就需要使用非空约束，我们如果使用这个约束就表示我们这一个列不接受任何空值（null）值，也就表明如果我们不在这里面添加值的话是不能够直接进行数据的更新和修改，使用非空约束可以使任何事情更快（增删涂改）而且每列可以节省一位。在我们开发时，如果提交给数据库的数据不符合数据库的条件，既我们数据库中没有这条数据，则会报错，null值是不会用上索引的，如果从安全的角度来讲，除非必须为null，尽量是使用约束，这样我们的语句就不会报错，从而不泄露我们的信息

- UNIQUE  约束唯一标识数据库表中的每条记录，简单的来说就是避免重复，我们在定义列的时候给它加上UNIQUE的约束，我们的这一列就不会出现重复的数据，我们的一个表中可以出现多个这个约束，你可以在每一列都加上，我们我来举个例子：
  ![1576497166586](C:\Users\15749\Desktop\typora图片\1576497166586.png)

  我们在这个表里面限制我们的id_card约束为UBIQUE，我们添加第一条数据id=1  id_card=123，可以成功的插入数据，我们插入第二条 id =2 id_card  = 123就添加失败：

  ![1576497345352](C:\Users\15749\Desktop\typora图片\1576497345352.png)

  当我们插入下一条：id = 1 id_card = 234,数据添加成功：

  ![1576497415035](C:\Users\15749\AppData\Roaming\Typora\typora-user-images\157649741  5035.png)

  查表：

  ![1576497448754](C:\Users\15749\Desktop\typora图片\1576497448754.png)

  我们发现们的id可以为重复的，但是我们的id_card就没法重复，这就是UNIQUE 这个主键的约束，我们的身份证数据就是这个方式来录入的，名字可以一样，但是你们的号码一定不同。

- PRIMARY KEY 主键约束，唯一的标识我们的每一条数据，我们在上面就已经使用过这个约束了，但是不同的是我们在后面还有一个AUTO_INCREMENT （用于主键增长）这个函数，我们主键约束要求一个表中都应该有一个主键（非强制，约定俗成），但也只能有一个主键，主键也是唯一的不能有重复的。主键的列的数据类型可以不一样，我们亦可以添加多个列为主键，添加了以后我们就可以定位找到我们想要的数据。

- FOREIGN KEY 外键约束，我们这个约束是为了让我们多个表之间联系，怎么来理解他呢？我们有两个表，分别的放着有关联的数据，比如我们的客户和客户的订单，我们第一个表存放客户信息，第二个表存放，订单和金额信息，我们要是想要将两个表中的数据整合，就需要使用我们的外键约束，我们使用了外键以后就可以在在一条插入语句中插入两个表的数据，如果父表中没有的对应的字段的话，就能不能够插入数据，下面是我们的一个例子，建表的语句如下：
  
```sql
  create table father_table
	(
  		id int primary key not null,
		name varchar(40)
  		);
create table son_table
  	(
  		uid int not null ,
  		price int(11),
  		foreign key(uid) references father_table(id)
  		);
```

  我们首先建立父表，如果不建立的话是不能够成功的，我们使用外键的时候需要注意一些事项：我们的父表字段必须为主键，子表的外键和父表的主键的类型。
  ![1576654952955](C:\Users\15749\Desktop\typora图片\1576654952955.png)
  我们在使用语句来添加子表的数据：
  ![1576655401184](C:\Users\15749\Desktop\typora图片\1576655401184.png)

  添加失败，因为我们父表中没有这一列，我们接下来在我们的父表中添加一些数据，然后再添加子表，我们发现就可以添加了，这就是外键约束的效果：

  ![1576656073931](C:\Users\15749\Desktop\typora图片\1576656073931.png)

  在这里我要提示一下关于如何删除有外键约束的表，我们删除的时候需要将我们的外键约束关闭，不然的话是不能够删除的，输入 SET FOREIGN_KEY_CHECKS=1;开启约束， SET FOREIGN_KEY_CHECKS=0;关闭约束，这样我们就可以删除我们的数据表，删除后就将约束打开。

  CHECK：CHECK 约束用于限制列中的值的范围。如果对单个列定义 CHECK 约束，那么该列只允许特定的值。如果对一个表定义 CHECK 约束，那么此约束会在特定的列中对值进行限制。例如我们的数据限制不能为0我们就可以使用这个约束。

  DEFAULT：DEFAULT 约束用于向列中插入默认值。如果没有规定其他的值，那么会将默认值添加到所有的新记录。比如我们下面的这个例子，我们在建库的时候给City一栏中添加了DEEAULT("四川")，所以我们在添加数据的时候如果不给它添加数据的话，他就会直接添加我们的给的默认值：

![1576658103700](C:\Users\15749\Desktop\typora图片\1576658103700.png)

![1576658669121](C:\Users\15749\Desktop\typora图片\1576658669121.png)

![1576658643216](C:\Users\15749\Desktop\typora图片\1576658643216.png)

默认值的使用可以大大减低我们的工作量。知道了这些主键以后，我们围绕外键约束给大家说一下连接符号的使用

在我们上面所说的约束中我们知道了外键约束的作用，当很多时候需要多个表一起查询时，就需要使用到连接符号，顾名思义连接符就是讲我们两个表中的数据在一个集合中显示出来。引入一个新的函数：JOIN——这个函数的作用是将我们的多表联合查询，他有三种方式查询：

INNER JOIN （内联或者等值连接）：获取两个表中字段匹配（父子）的关系记录，比如我们第一张表是记录的客户名字和他们对应的第二张表是记录我们客户进行贸易的表，我们想要知道某一个人的交易记录就联合两个表来进行查找，先建两个表：![1576669748131](C:\Users\15749\Desktop\typora图片\1576669748131.png)


