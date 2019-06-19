# 推文实习生面试题

### 说明：

- <span style="color:red">以下题目都是编程题，答题时间为24小时，你可以上网、看书、问任何你能问的人；程序和运行**结果截图**，发到  **hr@babelchain.org** 或者微信发给HR小姐姐。</span>

- **<span style="color:red">邮件里只有代码文件和截图，不要发生成的数据文件，excel，word，pdf等。</span>**

- **<span style="color:red">题目不需要全部都做，使用你擅长的编程语言做你会做的题目。</span>**



### 编程问题


 1. 写一个程序，统计一下 C 盘下面有多少个 .dll 文件；如果你是 Mac 或者 Linux 系统，统计一下 /usr 目录下有多少个 .so 文件. 
 **注意不能使用 walkFileTree, os.walk 这类直接遍历所有目录的方法，而是要你自己实现它。** 


 2. mkdate 是一个用不同语言写的（Java，C++，Bash，Python，JavaScript），生成随机日期的程序，下载mkdate，完成下面的任务。mkdate 下载链接
https://gitee.com/yangbigrm/interview_of_twitter_interns/tree/master/mkdate

- 2.1 编译并运行 mkdate 程序，生成10万条数据 `./mkdate 10 > date10.txt`（5种语言里选你会的，注意 Java 应编译为jar）
- 2.2 文件的每一行是一个日期，但是这些日期并不都是正确的，你需要修复这些日期。修复采取就近修复的原则；例如：`2010-2-30 6:5:13`，没有2月30日，就近修复到 `2010-3-1 6:5:13`
- 2.3 把文件中所有恰好是星期日的数据（例如2010-1-31是星期日），存到一个 excel 文件中。注意日期要排序。
- 2.4 生成500万条数据，存到文件 `./mkdate 500 > date500.txt`，取出时间离今天时间最近的1000条，存到 Excel 文件中。
- 2.5 500万条数据，程序运行得很慢，有没有优化的方法？



### 算法

第1题 已知一个二叉树的每个节点为 Node {leftChild, rightChild, data}

```
先序遍历的结果为: A B D E I J K C F G H
后序遍历的结果为: B D E I J K C F G H A
```
请写代码重建这个二叉树
<br>
   

第2题 写一个程序，计算下面数列的结果；在屏幕上打印出的要求是精确结果

   $f(n) = f(n-1)+f(n-2)+f(n-3)+1$

   $f(0)=f(1)=f(2)=0$

a. f(100)<br>
b. f(100,000)<br>
c. f(20,000,000)<br>
<br>

第3题 已知$x,y,n$都是整数，满足下面的这个方程：

   ### $\frac{1}{x}+\frac{1}{y}=\frac{1}{n}$

   例如 $n=6$ 的时候，这个方程有5组不同的解：

   $\frac{1}{7} + \frac{1}{42} = \frac{1}{6}$

   $\frac{1}{8} + \frac{1}{24} = \frac{1}{6}$

   $\frac{1}{9} + \frac{1}{18} = \frac{1}{6}$

   $\frac{1}{10} + \frac{1}{15} = \frac{1}{6}$

   $\frac{1}{12} + \frac{1}{12} = \frac{1}{6}​$

   编程求解问题：

   a. n**最小**等于多少的时候，这个方程恰好有100组不同的解<br>
   b. n**最小**等于多少的时候，这个方程恰好有1000组不同的解<br>
   c. n**最小**等于多少的时候，这个方程恰好有100万组不同的解<br>


### 策略

第1题 桌子上放了1000张卡片，上面分别写了数字1到1000，甲乙两个人轮流拿卡片，从数字1开始拿。如果一个人拿了数字x，那么另外一个人必须拿数字2x或者x+1；谁先拿到数字1000谁获胜。

   例如 若甲拿了2，乙只能拿3或者4；若甲拿了500，乙可以拿1000，乙获胜。

   问：甲先拿卡片，请问甲有没有必胜的策略？

第2题 桌子上放了1000张卡片，上面分别写了数字1到1000，甲乙两个人轮流拿卡片，如果一个人拿了数字x，另外一个人必须拿x的倍数或者因数；如果某个人没有卡片可以拿了，那么他就输了。

   例如 若甲拿了50，乙能拿2、5、25、100、200、1000中的任意一个数字，只要是50的因数或者倍数都可以；若甲拿了1，乙拿997，这个时候甲没有数字可以拿了，甲就输了。

   问：甲先拿卡片，请问甲有没有必胜的策略？

第3题 以上两个问题，对于N张卡片的情况，可否一般化，写成一个算法。



### 自然语言处理

一部小说文学作品中，通常会有数以百计的人物。根据下面的链接，下载指定的文本文件《放开那个女巫.txt》，完成2个任务：</br>
a.提取文本的主要人物，b.对人物的性别进行分类。</br>
程序运行输出结果是一个表格(csv, excel, txt 任意你方便的格式)。不限定你用什么算法、模型，但是需要简要说明一下你用到的算法和模型思路，并简单评估一下准确率。

| 人物     | 性别   |
| -------- | ------ |
| 罗兰     | male   |
| 夜莺     | female |
| 安娜     | female |
| 嘉西亚   | male   |
| 海克佐德 | male   |
| 瓦基里丝 | female |
|          |        |

链接:https://pan.baidu.com/s/1Uz7DXMekO7JIt9w_PJryqg  密码:whfy



