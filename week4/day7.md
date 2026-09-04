#day7
#碎碎念：写个java的练习写得我道心破碎，这些题目会不会太难了点qwq

 #二维数组(用于数组需要分组管理)
 public static void main(String[] args) {

        //静态初始化
        数据类型[][] 数组名 =new 数据类型[][] {{元素1,元素2,元素3},
                                                {元素4,元素5,元素6}};
        数据类型[][] 数组名 = {{元素1,元素2,元素3},
                                 {元素4,元素5,元素6}};
        
        int[][] arr = {{1,2,3},{4,5,6},{7,8,9}};


        //获取数组
        //arr[0]表示获取二维数组中第一个数组的地址值
        //arr[0][0]表示获取二维数组中第一个数组的的第一个元素
        System.out.println(arr[0][0]);

        //二维数组的遍历
        //思路：先遍历二维数组的元素（一维数组），在遍历一维数组
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr[i].length; j++) {
                System.out.print(arr[i][j] + " ");
            }
            System.out.println();

        }
    }



    二维数组动态初始化
    格式：数据类型[][] 数组名 = new 数据类型[m][n];
            m表示行数（一维数组的个数），n表示列数（一维数组的长度）
        public static void main(String[] args) {
        int[][] arr = new int[3][4];
        int[][] arr1 = new int[3][];
        arr1[0] = new int[]{1,2,3};
        arr1[1] = new int[]{4,5,6,7};
        arr1[2] = new int[]{8,9,10,11,12};



 #附上一道写的剧恶心的题，无敌了,双色球彩票
 
 import java.util.Random;
 import java.util.Scanner;

 public class test10 {

    public static void main(String[] args) {
        int[] arr = getNum();
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        int[] userarr = userNum();
        int redcount = 0;
        int bluecount = 0;
        for (int i = 0; i < arr.length - 1; i++) {
            for (int j = 0; j < userarr.length - 1; j++) {
                if (arr[i] == userarr[j]) {
                    redcount++;
                }
            }
        }
        if (arr[arr.length - 1] == userarr[userarr.length - 1]) {
            bluecount++;
        }

        //判断金额
        if (redcount == 6 && bluecount == 1)
            System.out.println("1000万");
        else if (redcount == 6 && bluecount == 0)
            System.out.println("500万");
        else if (redcount == 5 && bluecount == 1)
            System.out.println("300");
        else if ((redcount == 5 && bluecount == 0) || (redcount == 4 && bluecount == 1))
            System.out.println("200");
        else if ((redcount == 4 && bluecount == 0) || (redcount == 3 && bluecount == 1))
            System.out.println("10");
        else if ((redcount == 2 && bluecount == 1) || (redcount == 1 && bluecount == 1) || (redcount == 0 && bluecount == 1))
            System.out.println("5");
        else System.out.println("未中奖");
    }


    //生成随机数的方法
    public static int[] getNum() {
        int[] arr = new int[7];
        Random r = new Random();
        for (int i = 0; i < 6; ) {
            //红球范围1~33
            int rednum = r.nextInt(33) + 1;
            //判断是否重复，排除重复数字
            boolean flag = check(arr, rednum);
            if (!flag) {
                arr[i] = rednum;
                i++;
                //记录到了一个全新数字再结束循环
            }
        }
        //蓝球范围1~16
        arr[arr.length - 1] = r.nextInt(16) + 1;
        return arr;
    }


    //判断新引入数字是否与数组内现有数字重复
    public static boolean check(int[] arr, int rednum) {
        for (int i = 0; i < arr.length; i++) {
            if (rednum == arr[i]) {
                return true;
            }
        }
        return false;
    }


    //录入用户的彩票号码
    public static int[] userNum() {
        int[] arr = new int[7];
        for (int i = 0; i < 6; ) {
            Scanner sc = new Scanner(System.in);
            System.out.println("请输入第" + (i + 1) + "个红球号码：");
            int rednum = sc.nextInt();
            boolean flag = check(arr, rednum);
            //判断范围
            if (rednum >= 1 && rednum <= 33) {
                //判断重复
                if (!flag) {
                    arr[i] = rednum;
                    i++;
                } else {
                    System.out.println("输入的号码重复，请重新输入");
                }
            } else {
                System.out.println("输入的号码超出范围，请重新输入");
            }
        }
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入蓝球号码：");
        int blue = sc.nextInt();
        if (blue >= 1 && blue <= 16) {
            arr[arr.length - 1] = blue;
        } else {
            System.out.println("输入的蓝球号码超出范围，请重新输入");
        }
        return arr;
    }
}




#胡言胡语：明天要军训了，不要啊，wwwwwwwwwww
