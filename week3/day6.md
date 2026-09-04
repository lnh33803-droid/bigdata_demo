#day6
#碎碎念：
 又是花了两天把方法给学完了，从今天开始我就要放弃java了。狗才学java，我不学，我要去学python了，我爱python

#方法：
    程序中的最小执行单位
       重复的代码，具有独立功能的代码可以抽取到方法中

     好处：
        提高代码的复用性
        可以提高代码的可维护性

    方法的定义格式
      最简单的定义方法的格式：
        public static void 方法名(){
            方法体（就是打包起来的代码）;
        }
  
      带参数的方法定义
        格式：
        public static void 方法名(参数列表){
            方法体（就是打包起来的代码)
        }


      带返回值的方法定义
        格式：
        public static 返回值类型 方法名(参数列表){
        方法体（就是打包起来的代码）;
        return 返回值;
        }
        


   方法调用：
        1.直接调用 方法名（实参）
        2.赋值调用： 整数类型 变量名 = 方法名（实参）
        3.输出调用： System.out.println(方法名（实参）)
       
        public static void main(String[] args) {
        直接调用
        add(1,2,3,4);

        赋值调用
        int result = add(1,2,3,4);
        System.out.println(result);

        输出调用
        System.out.println(add(1,2,3,4));
        }
        public static int add(int a, int b, int c, int d) {
        int sum = a + b + c + d;
        return sum;

        //用到调用处要根据方法的结果，去编写另外一段代码时，用到有返回值的方法
        }


  方法的重载：方法名相同，参数列表（个数，类型，顺序不同）不同。与返回值类型无关。
        好处：调用方便，简化方法命名

        public static void main(String[] args) {
        sum(10, 20);
        // 调用 int a, int b 的 sum 方法
        sum((short) 10, (short) 20);    
        // 调用 short a, short b 的 sum 方法
        sum((byte) 10, (byte) 20); 
        // 调用 byte a, byte b 的 sum 方法
        sum((long) 10, (long) 20); 
        // 调用 long a, long b 的 sum 方法
        }
        public static void sum(int a, int b) {
        System.out.println(a == b);
        }    
        public static void sum(short a, short b) {
        System.out.println(a == b);
        } 
        public static void sum(byte a, byte b) {
        System.out.println(a == b);
        } 
        public static void sum(long a, long b) {
        System.out.println(a == b);
        }   


      方法调用基本内存原理
        方法调用时，先被调用的方法会先进入栈内存，等待被调用的方法执行完毕，才会执行被调用的方法

      基本数据类型
        栈内存中储存的真实存在的数据类型，栈内存中存储的是数据类型的具体值
         
      引用数据类型
        栈内存中存储的是引用数据类型的地址，堆内存中存储的是引用数据类型的具体内容

      方法传递
        方法传递参数时，基本数据类型是值传递，形参的修改不会影响实际参数
        引用数据类型是地址传递，形参的修改会影响实际参数
        
   
  
    return :与循环无关，跟方法有关，表示1结束方法，2返回结果
            如果执行到了return，整个方法都结束

    break 与方法无关，与结束循环和switch有关



#胡言胡语：
 java的学习进程就告一段落了，但是python这玩意，额。。。后天就开学了，一点学的欲望都没有怎么办，qwq



