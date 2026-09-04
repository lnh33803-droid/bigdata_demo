#day4
#碎碎念：
 python的循环和java还是有共同之处的，但是还是增加了一些新奇的东西

格式
    if 要判断的条件：（判断的结果必须是布尔类型）
        条件成立时（即true），要执行的操作
    else：
        条件不成立，执行操作
   
    #ps：tab缩进范围内的都是循环的执行语句

 进阶（有点像elseif）
 if ...elif...else

    if 要判断的条件1：
        条件成立时，执行对应操作
    elif 条件2 ：
        成立时，执行操作
    else：
        不成立时，执行操作



    a =int(input("bian"))
    b =int(input("bian"))
    c=int(input("bian"))
    if a+b > c and b+c > a and c+a > b:
        if a==b and b==c:
            print("等边")
        elif a==b or b==c or a==c:
            print("等腰")
        else:
            print("普通")
        #pass空语句，起到一个语法占位作用,后面删除在补写
    else:
        print("fail")

#注意缩进


#胡言胡语：python的循环还是有点难处的，没有大括号的存在，导致tab的缩进尤为重要，但是美观简洁方面无可挑剔




