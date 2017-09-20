# note
记录日常学习记录，及笔试题目记录

2017-09-18
--------------
小米笔试题：杨辉三角相关，回文数相关，还有一道分析类型的。
学习java基础之匿名内部类创建多线程。定时器的了解。Timer类 TimerTask类

2017-09-19
---------------
复习了集合部分的知识。
Collection
        |--List    有序,可重复
            |--ArrayList
                底层数据结构是数组，查询快，增删慢。
                线程不安全，效率高
            |--Vector
                底层数据结构是数组，查询快，增删慢。
                线程安全，效率低
            |--LinkedList
                底层数据结构是链表，查询慢，增删快。
                线程不安全，效率高
        |--Set    无序,唯一
            |--HashSet
                底层数据结构是哈希表。
                如何保证元素唯一性的呢?
                    依赖两个方法：hashCode()和equals()
                    开发中自动生成这两个方法即可
                |--LinkedHashSet（输入顺序和输出顺序一样，只是去重复了，因为底层链表）
                    底层数据结构是链表和哈希表
                    由链表保证元素有序
                    由哈希表保证元素唯一
            |--TreeSet
                底层数据结构是红黑树。
                如何保证元素排序的呢?
                    自然排序
                    比较器排序
                如何保证元素唯一性的呢?
                    根据比较的返回值是否是0来决定
复习过程发现LinkedHashSet底层为链表结构，输入输出顺序一致。那之前遇到的输入去重复且输入相对位置不变就有了下面的解决办法：
元素添加到list，然后用linkedhashset去重复，在转换为arraylist。
List<String> listWithoutDup = new ArrayList<String>(new LinkedHashSet<String>(list));
2017-09-20
---------------
复习构造方法的混淆点：调用子类的构造方法，默认情况下，会先调用父类的无参构造，即super();有参构造，需要自己添加，如果父类的有参构造，子类也是有参构造，传递进来，需要使用super(参数)；
Arrays.binarySearch(a[]);a此时为已排序的数组，不然返回的值是错误的。
        String.valueOf(number):int-String
        Integer.toSting(number):int-String
        Integer.parseInt(str):String-Int
        Integer.valueOf(str):String-Int
