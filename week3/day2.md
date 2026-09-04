#day2
#碎碎念：本来想着说学完面向对象应该就差不多了，这样就能确保在一周就能完成java基础，看了看估计还要学到学生系统去，啊啊啊，根本学不完啊，没时间学python了，qwq，没多久就要开学了，www

#今天是循环的一天

    #for格式：
       for (初始化语句;条件判断语句;条件控制语句) {
            循环体
        }
    
    for循环的执行流程:
        1.初始化语句
        2.条件判断语句(若为true则执行循环体,若为false则退出循环)
        3.循环体
        4.条件控制语句
        5.条件判断语句

        获取一个范围的每一个数据时，也用到循环
        用来累加
        int a = 0;
        for (int i = 1; i <= 5; i++) {
            a= a+i;
        }
        System.out.println(a);


        变量不能定义在循环里面，因为变量只所属的大括号中有效
        如果把定义的变量定义在循环里面，那么当前变量只能在本次循环有效
        当本次循环结束之后，变量就无效了
        第二次循环的时候，又会重新定义一个新的变量
        for (int i = 1; i <= 5; i++) {
            int b = 0;
            b = b + i;
            System.out.println(b);
        }

        
        统计变量，用于统计满足条件的数字个数
        int a = 0;
        for(int i = start; i <= end; i++) {
            if (i % 3 == 0 && i% 5 == 0) {
                a= a+1;
            }
        }
        System.out.println(a);

    #while格式：
        while (条件判断句) {
            循环体语句
            条件控制语句
        }

        int i = 1;
        while (i <= 100) {
            System.out.println(i);
            i++;
        }

        for和while的区别
        for：知道循环次数or循环的范围
        while：不知道循环次数，只知道循环结束条件
    
    #dowhile格式：
           初始化语句
        do{
          循环体语句
          条件控制语句
        }while(条件判断句)
     
        先执行，后判断，至少执行一次



    #示例：
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入一个整数：");
        int x  = sc.nextInt();
        int temp = x;//定义一个临时变量，来记录x的值，下文的循环会改变x的值
        int num = 0;
        while (x != 0) {
            int ge = x % 10;//获取最后一位数
            num = num * 10 + ge;//追加到结果末尾
            x = x / 10;//去掉最后一位数
        }
        if(num == temp)
            System.out.println("是回文数");
        else
            System.out.println("不是回文数");


    #无限循环
     for格式
        for(;;){
        循环语句体
        }
         
     while格式
        while(true){
        循环语句体
        }
        
     do while格式
        do {
        循环语句体
        }while(true)


    跳转循环
      1.continue
        for(int i = 1; i <=5; i++){
            if(i == 3){
                continue; //结束本次循环，继续下次循环
            }
        System.out.println("吃第"+ i +"个包子");}

      2.break
        for(int i = 1; i <=5; i++){
            if(i == 3){
                break;//结束整个循环
            }
        System.out.println("吃第"+ i +"个包子");}

    #示例
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        //标记思想
        //标记这x是一个质数
        //true表示x是质数, false表示x不是质数
        boolean flag = true;
        for (int i =2; i < x; i++){
            if (x % i == 0) {
                flag = false;
                break;
            }
        }
        if(flag) {
            System.out.println("yes");
        }else{
            System.out.println("no");

    简化思路
    如果在一个小于等于它的平方根的数中，所以数字都不能被它整除，那么这个数就是质数
        int num = 100;
        for (int i = 2; i <= Math.sqrt(num); i++) {
        if (num % i == 0) {
            System.out.println("不是质数");
            break;
            }
        }


    #完全得学
import java.util.Random;//导包，类似于scanner，导入随机数类
import java.util.Scanner;
public class test6 {
    public static void main(String[] args) {
        //获取随机数
        Random r = new Random();
        //生成随机数
        //在小括号内，书写的是随机生成数的范围，固定从0开始，到这个数-1
        //口诀：包头不包尾，包左不包右
        int num = r.nextInt(100) + 1;//生成1到100之间的随机数
        Scanner sc = new Scanner(System.in);
        //扩展保底机制
        int count = 0;
        while (count < 10) {
            System.out.println("请输入一个1到100之间的数字：");
            int guess = sc.nextInt();//需要"每轮都变化的量"，就必须放在循环体内
            count ++;
            if(count ==10)
                System.out.println("猜对了");
            if(guess > num) {
                System.out.println("你猜的数字太大了！");
            } else if (guess < num) {
                System.out.println("你猜的数字太小了！");
            } else {
                System.out.println("恭喜你，猜对了！");
                break;
            }


            //范围秘诀：生成任意数到任意数之间的随机数 7~15
            //1.让这个范围的头尾都减去一个值，让这个范围从0开始 -7
            //2.尾巴加1  8+1=9
            //3.最终结果，再加上第一步减去的值
            //int num2 = r.nextInt(15-7+1)+7;
        }
    }
}

    #胡言胡语：好累！！！！！！！！！！！！！！！



