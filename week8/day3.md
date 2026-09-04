#day3

#碎碎念：
 java和python还是太累了QWQ，明天就国庆就回家了，好舒服呀~~~

 
 #python
    列表常见方法
    append()在尾部追加元素 s.append(10086)
    insert() 在指定索引前，插入元素
    remove() 移除到第一个匹配到的值
    pop()  删除列表中指定索引的元素（若未指定索引，默认删除最后一个）（会返回删除掉的元素）
    sort() 对列表进行排序（要求类型一致）
    reverse() 反转列表元素

    import numbers

    #定义列表
    num_list = []

    #循环输入十次数字录入列表中
    for i in range(10):
        num = int(input("输入数字"))
        num_list.append(num)

    #打印列表
    print(num_list)

    #排序
    num_list.sort()
    print(num_list)

    #打印最小和最大和平均值
    #sum()  求和      len() 获取列表长度  max()取最大值   min()取最小值
    
    print("最小值",num_list[0])
    print("最大值",num_list[-1])
    print("平均值",sum(num_list)/len(num_list))


 #拼接列表
    num_list1 = [1,2,3,4,5,6,7,8,9]
    num_list2 = [1,332,455,6,43,77,34]

    #拼接列表
    #for num in num_list2:
    #    num_list1.append(num)
    #print("拼接后的列表",num_list1)

    #用加号拼接列表
    num_list3 = num_list2 + num_list1
    print(num_list3)

    #用解包拼接列表
    #解包：将列表这一容器拆成一个一个元素
    #组包：多个值合并到一个容器
    num_list4 = [*num_list1,*num_list2]
    print(num_list4)


    #记录去重后的列表
    num_list = []
    for num in num_list1:
        if num not in num_list:
            num_list.append(num)

    num_list.sort()
    #print(num_list)



#java
    static void main(String[] args) {
        //用stringJoiner创建一个对象，并制定间隔符号
        //间隔符号，开始，结尾
        StringJoiner sj = new StringJoiner("---","[","]");

        //添加元素
        sj.add("aaa").add("bbb").add("ccc");

        //打印结果
        System.out.println(sj);

        //打印长度
        int len = sj.length();
        System.out.println(len);

        //变成字符串
        String str = sj.toString();
        System.out.println(str);

        //也可以看成是个可变的操作字符串的容器
        // 适用拼接字符串 JDK8版本
    }


 #字符串原理
    1.内存原理：
     直接赋值会复用字符串常量池中的
     new出来不会复用，而是开辟一个新的空间

     2. == 比什么
      基本数据类型比较数据值
      引用数据类型比较地址值

     3.字符串拼接的底层逻辑
      没有变量参与：字符串直接相加，编译之后就是拼接之后的结果，会复用串池中的字符串
      有变量参与： 会创建新的字符串，浪费内存

     4.StringBuilder提高效率原理图
      所有拼接的内容都会在Stringbuilder中放，不会创造许多无用空间，节约内存

     5.StringBuilder源码分析
      创建一个长度为16的字节容器
      添加内容长度小于16，直接存
      添加内容大于16会扩容（原来的容量*2+2）
      之后还不够，以实际长度为准



#胡言胡语：
 也是巧妙的，发现这java和python的方法竟然有些是相似的，没话说，学一通百好吧
