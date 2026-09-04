#day3
#胡言胡语：
 md，刚刚更新day2的时候忘记打‘git commit -m "xxx"’了，导致一大堆麻烦，烦
 最近倒是刷到了不少“java已死”的言论，感觉现在已经是四九年入国军——麻烦大了，谢谢，反正将学就学，上了大一尝试同时学学Python，看我降维  打击（doge）

#命令
 1.Scanner
 (就是一个输入数据的一个程序，但是竟然需要三行代码，比Python麻烦。。。)
   //导包，写在类定义的上面
	import java.util.Scanner;
	public class Demo
 {
    	public static void main(String[] args) 
    {
   //创建对象：表示我现在要用scanner这个类
        Scanner scanner = new Scanner(System.in);
        System.out.println("请输入一个整数：");

   //接收数据
        int i = scanner.nextInt();
	（值得注意的是这里除了‘i’即变量名能改，其他都不能改）
        System.out.println(i);
    }
}
