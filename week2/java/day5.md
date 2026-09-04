#day5
#碎碎念：尝试性拾回前两天的学习内容

#运算
    1.算术运算
        +  1. 1.有字符串相加，做拼接操作
           2.没有字符串相加，做数学加法
           3.字符与数字相加，做数学加法（查询ASCII表）
             System.out.Println(1+3+"5")//45
             (a.从左往右 b.有字符串为合并)
           4.转换：
                隐式转换：小+大默认有隐式转换（小->大）
                          short，byte，char->int
                强制转换：
                    格式: 目标数据类型 变量名 = （目标数据类型）被强转的数据
                          byte a = 10;
                          byte b = 20;
                          byte c = (byte)(a + b);因为强制转换的目标是a+b的和
                          System.out.println(b);
                         (ps.强制转换数值太大会发生错误)
    2.自增自减运算符
         ++ 变量的值加1  -- 变量的值减1
                 int a =10;
                 ++a;
                 System.out.println(a);//11
                 a++;
                 System.out.println(a);//12
                 --a;
                 System.out.println(a);//11
                 a--;
                 System.out.println(a);//10
         ++i 先加后用  i++ 先用后加


    3.赋值运算
        += 将左边和右边相加，再把结果赋值给左边
            int a = 10;
            int b = 20;
            a += b;
            System.out.println(b);//20
            System.out.println(a);//30
        -= 将左边和右边相减，再把结果赋值给左边
            int c = 5;
            a -= c;
            System.out.println(a);//25

        += -= /= *= %= 底层都隐藏了强制类型转换
            short s = 1;(把左边和右边相加，在赋值给左边)
            s +=1;(等同于： s = (short)(s + 1));
            System.out.println(s);//2
    4.关系运算符
         == 判断两个值是否相等
            int a = 10;
            int b = 20;
            System.out.println(a == b);//false
         != 判断两个值是否不相等
            System.out.println(a != b);//true
         >  判断左边的值是否大于右边的值
            System.out.println(a > b);//false
         <  判断左边的值是否小于右边的值
            System.out.println(a < b);//true
         >= 判断左边的值是否大于或等于右边的值
            System.out.println(a >= b);//false
         <= 判断左边的值是否小于或等于右边的值
            System.out.println(a <= b);//true

    5.逻辑运算符
      1.& 并且 (两边都是真，结果才是真)
         System.out.println(true & true); // true
         System.out.println(true & false); // false
      2. | 或 (两边都是假，结果才是假)
         System.out.println(false | false); // false
         System.out.println(false | true); // true
      3. ^ 异或 (两边相同结果是假，两边不同结果是真)
         System.out.println(true ^ true); // false
         System.out.println(true ^ false); // true
      4. ! 非 (true 变 false，false 变 true)
         取反的感叹号不要写多次，要么不写，要么只写一次
         System.out.println(!true); // false
         System.out.println(!false); // true
    
    6.短路逻辑运算符
      1. && 短路与
        两边都是真，结果才是真
        运行结果和&一致，效率高
        System.out.println(true && true); // true
        System.out.println(true && false); // false
      2. || 短路或
        两边都是假，结果才是假
        运行结果和|一致，效率高
        System.out.println(false || false); // false
        System.out.println(false || true); // true
      3.短路逻辑运算符具有短路效果
        简单理解：当左边能确定最终的结果时，右边的代码将不再执行
        int a =10;
        int b =10;
        boolean result = ++a<5 && ++b<5;
        System.out.println(result);
        System.out.println(a);//11
        System.out.println(b);//10

#公式：个位数：i%10，
       十位数：i/10%10
       百位数：i/100%10
       .....





#唠叨一下：喵的，终于复制粘贴完了上课的笔记，就大多是ai辅助写的了，也不知道费尽心思总结干嘛用，就当我努力了吧（doge）


