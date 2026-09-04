#day7
#碎碎念：现在是2026年9月28日20:34:54，写这个主要是给上周收个尾，并非没学，只是都忙着写练习了，也没什么时间写笔记


#String

 #字符串遍历
    str.length().fori
    遍历字符串内每一个字符

 #字符串的键盘录入
    String str = sc.next();

 #反向遍历数组
    str.length().forr
    for (int i = str.length()-1; i >= 0; i--) {//i表示是索引，从0开始，故str.length需要减1
            result =result + str.charAt(i);
        }
 #提取字符串内的字符
    char c = str.charAt(i);
    提取位于i索引的字符

 #用字符串中的数字进行计算可以借助ASCII法表
    String id = "440513200302083210";
        String year = id.substring(6, 10);
        String month = id.substring(10, 12);
        String day = id.substring(12, 14);
        System.out.println(year + "年" + month + "月" + day + "日");

        char genderNumber = id.charAt(16);
        //用ascii法表
        /*0 ---> 48
          1 ---> 49
          ...
         */
        int num = genderNumber - 48;
        if(num %2 == 0){
            System.out.println("女");
        }else{
            System.out.println("男");
        }

 #替换字符
    str = str.replace(a,b);
    用b替换a


#发现写了个笔记就累了，不想学了


