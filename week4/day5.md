#day5
#循环学一半就累了兄弟，直接放弃明天再学

#match
    a =float(input("a"))
    b =float(input("b"))
    yunsuan =input("yunsuan")
    match yunsuan:
        case "+":
            print(a+b)
        case "-":
            print(a-b)
        case "*":
            print(a*b)
        case "/" if b !=0:
            print(a/b)
        case _:         //表示其他情况
            print("sjbssm")

        #还有case a | b :
        #| 表示或，与java相同


while
格式：
while 条件表达式：(true循环，false结束循环)
    循环语句体1
    循环语句体2
    ...
else:（可有可无）
    语句体

for
结构:
for 元素 in 待处理数据集
    循环体代码（对元素进行处理）
else：
    循环结束时，执行代码 //可选

区别：
    for：遍历一个已知的数据集
    while：只知道循环开始和结束的条件



range语句
作用：生成指定规则的数据序列

1.range（end） -> 从0开始 到end结束 （不包含end）
2.range（start，end） -> 从start开始 到end结束 （不包含end）
3.range（start，end，step） -> 从start开始 到end结束，step为步长 （不包含end）



#胡言胡语：
除了range的出现让我比较意外，其他都是比较简单的，没什么压力。。。




