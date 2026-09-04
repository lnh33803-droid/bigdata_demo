day1
#碎碎念：好累

#StringBuilder
 #创建一个容器，用来对字符串进行操作

        //创建对象
        StringBuilder sb = new StringBuilder("abc");

        //添加元素
        sb.append(1);
        sb.append(2.3);

        //反转
        sb.reverse();

        //获取长度
        int len = sb.length();
        System.out.println(len);

        //StringBuilder是java提前写好的类
        //做了特殊处理，打印对象时不是地址值而是属性

        System.out.println(sb);

        //再把StringBuilder变回字符串
        String str = sb.toString();
        System.out.println(str);



 #链式编程
        //在调用一个方法时，可以继续调用其他方法
        int len = getString().substring(1).replace("A","Q").length();
        System.out.println(len);
        }

        public static String getString(){
        Scanner sc = new Scanner(System.in);
        System.out.println("字符串");
        String str = sc.next();
        return str;


    static void main(String[] args) {
        int[] arr = {1, 2, 3};
        String result = reverseString(arr);
        System.out.println(result);

         }

         public static String reverseString(int[] arr) {
        StringBuilder sb = new StringBuilder();
        sb.append("[");
        for (int i = 0; i < arr.length; i++) {
            if(i == arr.length-1){
                sb.append(arr[i]);
            }else{
                sb.append(arr[i]+",");
            }
        }
        sb.append("]");
        return sb.toString();
    }


  #使用场景
    1.字符串的拼接
    2.字符串的反转



#胡言胡语：
  不想学了啊，好累！！！！！1！1
