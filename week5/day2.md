#day2

#碎碎念：终于学到了面向对象了。。。

 #面向对象
    类：是对象的设计图，共同特征的描述
    对象：是类的实例，具体特征的描述

    如何得到对象
        1.创建类
        public class 类名{
          成员变量（表属性）
          成员方法（表行为）
            }

        2.创建对象
         类名 对象名 = new 类名();

        拿到对象之后
        对象.成员方法() 调用对象的方法
        对象.成员变量 获取对象的属性


        注意事项：
        表述一类事务的类：javabean，不写main方法
        编写main方法的类叫测试类
        




public class GirlFriend {
    //属性
    String name;
    int age;
    String gender;



    //行为
    public void study(){
        System.out.println("学习");
    }
    public void eat(){
        System.out.println("吃");
    }
}


public class GirlFriendTest {
    public static void main() {
        GirlFriend l = new GirlFriend();
        l.name = "l";
        l.age =18;
        l.gender = "women";

        System.out.println(l.age);
        System.out.println(l.gender);
        System.out.println(l.name);
        l.eat();
        l.study();


        GirlFriend y = new GirlFriend();
        y.name = "y";
        y.age = 19;
        y.gender ="girl";

        System.out.println(y.age);
        System.out.println(y.gender);
        System.out.println(y.name);

        y.eat();
        y.study();
    }
}





#就这酱紫~
