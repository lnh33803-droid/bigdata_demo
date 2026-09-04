#day2
#碎碎念：进入速通python阶段，还是有很多和java的共同之处的，但是少写好多的;真是人间的一大幸事啊


1.utf-8 万国码，新版python可以不写

2.字符串
三种：
s1 = "hello world"
s2 = 'hello world'
s3 = """
   python
   666  
"""

s4 ='it\'s python'# \ 转义斜线
 同理： \"  
        \n换行 
        \t 缩进一个tab的距离

    字符串的拼接：“+” 只能用来将字符串与字符串拼接
        name = "涛哥"
        age = "18"
        study = "软件工程"
        love = "python、java"
        print("大家好，我是"+name+",今年"+age+",学习的专业是"+study+",爱好"+love)

    字符串格式化，---> %s
        name = "涛哥"
        age = "18"
        study = "软件工程"
        love = "python、java"
        print("大家好，我是%s,今年%s,学习的专业是%s,爱好%s"%(name,age,study,love))


    字符串格式化 ----> f"..{变量名}...."
        print(f"大家好，我是{name},今年{age},学习的专业是{study},爱好{love}")

    
    输入
    变量名 = input("提示")
    name = input("输入你的姓名：")
        money = 10000
        code =input("输入密码：")
        take =input("输入取款金额")

    input输入默认为str ，应该将take转换为int类型，类似于java的强制转换--->int(...)
        print(f"余额：{money - int(take)}")#大括号的占用符内可以写表达式



