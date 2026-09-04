#day2

#python
    #数据容器
    #可以容纳多个数据的数据类型（容器），容器中每一份数据叫做元素，每一个元素都可以是任意类型的数据
    """
    列表（list）
    字符串(str)
    元组（tuple）
    集合（set）
    字典（dict）
    """

    #定义，列表名称 = [元素1，元素 2，...]同一列表可以存储不同类型元素
    #索引从0开始
    #反向索引，倒数第一个元素为-1索引，倒数第二为-2....

    s = [30,90,90,"ABC",True,"无敌了"]

    #查看s类型
    print(type(s))

    #索引
    print(s[0])#30
    print(s[-6])#30

    #修改
    s[3]= 60
    print(s[3])

    #删除del
    del s[1]

    print(s)

    #遍历
    for item in s:
        print(item)

    #切片操作 s[开始索引（默认为0）：结束索引（不包括）；步长(默认为1)]
    print(s[0:4:1])
    print(s[:4:1])
    print(s[:4:])
    print(s[:-2:])




#java
    api
    JDk提供的各种功能的类
    scanner random 都是api


    String
    //String是jdk中自带的类，不需要导包

    //字符串不可改变，它们的值在创造后不可改变

        //赋值方法：
        //1.直接赋值
        String s1 = "super 猪猪侠";

        //空参构造
        String s2 = new String();
        System.out.println("@"+s2+"!");//@!

        //传递一个字符数组，用来构造字符串
        //用来修改字符串
        //abc ---> {'a','b','c'}--->{'Q','b','c'}
        char[] chs = {'a','c','b','d'};
        String s3 = new String(chs);
        System.out.println(s3);//acbd

        //传递一个字节数组，用来构造字符串
        //应用场景：玩网络当中传递的数据其实都是字节信息
        //我们一般把字节信息进行转换，转成字符串，这时候就会用到这个构造
        byte[] bytes= {97,98,99,100};
        String s4= new String(bytes);
        System.out.println(s4);//abcd

        //内存图
        //直接赋值会检查字符串是否相同，相同的话，两个变量会共用一个地址值
        //传递赋值每new一次都会在堆内存上开辟一个空间，不管字符串是否相同



#胡言胡语：
 累了  
