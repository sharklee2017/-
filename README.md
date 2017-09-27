# note
记录日常学习记录，及笔试题目记录

2017-09-18
-------------------------------------------------------------------

小米笔试题：杨辉三角相关，回文数相关（已更新）。<br> 
学习java基础之匿名内部类创建多线程。定时器的了解。Timer类 TimerTask类<br> 

2017-09-19
-----------------------------------------------------------------------------

复习了集合部分的知识。<br> 
#### Collection<br>
#### List 有序,可重复 <br> 
1.  ArrayList <br> 
     底层数据结构是数组，查询快，增删慢.<br> 
     线程不安全，效率高 .<br> 
2.  Vector<br> 
     底层数据结构是数组，查询快，增删慢 .<br> 
     线程安全，效率低 .<br> 
3. LinkedList<br> 
     底层数据结构是链表，查询慢，增删快.<br> 
     线程不安全，效率高.<br> 
      
#### Set 无序,唯一 <br> 
1.  HashSet<br> 
    底层数据结构是哈希表.<br> 
    如何保证元素唯一性的呢?<br> 
    依赖两个方法:hashCode()和equals();<br> 
2. LinkedHashSet(输入顺序和输出顺序一样)<br> 
     底层数据结构是链表和哈希表:<br> 
     由链表保证元素有序.<br> 
     由哈希表保证元素唯一. <br> 
   
#### TreeSet<br> 
1. 底层数据结构是红黑树。 <br> 
     如何保证元素排序的呢。  <br> 
    	自然排序 比较器排序 <br> 
 2. 如何保证元素唯一性的呢。 <br> 
     根据比较的返回值是否是0来决定<br> 

#### tip.
复习过程发现LinkedHashSet底层为链表结构，输入输出顺序一致。那之前遇到的输入去重复且输入相对位置不变就有了下面的解决办法：<br> 
元素添加到list，然后用linkedhashset去重复，在转换为arraylist。<br> 
 ```java
List<String> listWithoutDup = new ArrayList<String>(new LinkedHashSet<String>(list));
```
        
2017-09-20
--------------------------------------------------------------------------------------

 ### 复习构造方法的混淆点:<br>
 1. 调用子类的构造方法，默认情况下，会先调用父类的无参构造，即super();有参构造，需要自己添加，如果父类的有参构造，子类也是有参构造，传递进来，需要<br> 使用super(参数)；<br> 
   
2. Arrays.binarySearch(a[]);a此时为已排序的数组，不然返回的值是错误的。<br> 
 ```java
 String.valueOf(number):int-String
 Integer.toSting(number):int-String
 Integer.parseInt(str):String-int
 Integer.valueOf(str):String-int 
 ```
### 学习单例模式，饿汉式、懒汉式。<br> 
        单例模式思想：保证类在内存中只有一个对象。开发常用饿汉式。懒汉式会出现线程安全问题。
        
2017-09-21
--------------------------------------------------------------------------------------
#### 工具类的易忘点
1. ArrayList 的  E     remove（int index）返回index移除的元素<br> 
               boolean remove(object o)   返回移除成功与否（传递进来的是对象，不是元素，可以new出来的对象）<br> 
``` java            
2. Arrays.fill(dp[],Integer.MAX_VALUE);//填充数组为最大值
   String.tirm();//去除两端空格
   //StringBuilder insert
   insert(index,char);
```
3.如果想要删除字符串中的指定某个字符，可以用substring(start,end)+substring(start,end);去除掉想要删除的字符。
  或者转换成StringBulider，使用方法setCharAt（index，'char'）;
#### 正则表达式总结
     新建了文件
2017-09-26
--------------------------------------------------------------------------------------
### N皇后问题
   递归和非递归<br> 
### 网络编程socket
   收发数据<br>
2017-09-27
--------------------------------------------------------------------------------------------
![github](/res/drawable-hdpi/ic_launcher.png) 
