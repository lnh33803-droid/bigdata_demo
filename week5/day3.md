#day3
#碎碎念：
 军训会不会有点太折磨了，右脚快要残废了，一点学习的欲望都没有，无敌了，都是把网课当做催眠工具用，直接好评好吧！


#封装：
    对象代表了什么，就得封装对应的数据，并提供数据对应的行为
    eg.人关门。门关这一属性应该是门的，而非人的行为


package test1;

public class GirlFriend2 {
   #private将成员变量私有化
    private String name;
    private int age;
    private String gender;

    //对于每个私有化的变量，都要提供对应的set和get方法

    //set方法：给成员变量赋值
    public void setName(String n) {
        name = n;
    }


    //get方法：对外提供成员变量的值
    public String getName() {
        return name;
    }

    public void setAge(int a) {
        if (a >= 18 && a <= 50) {
            age = a;
        } else {
            System.out.println("非法数据");
        }
    }

    public int getAge() {
        return age;
    }


    public void setGender(String n) {
        gender = n;
    }

    public String getGender() {
        return gender;
    }

    //行为
    public void study() {
        System.out.println("学习");
    }

    public void eat() {
        System.out.println("吃");
    }
}



package test1;

public class GirlFriendTest2 {
    public static void main() {
        GirlFriend2 l = new GirlFriend2();
        //引用set方法
        l.setName("l");
        l.setAge(18);
        l.setGender("女");


        //引用get方法；也可以写成（a=getName;  sout(a);）
        System.out.println(l.getName());
        System.out.println(l.getAge());
        System.out.println(l.getGender());
        l.eat();
        l.study();


        System.out.println("=======================");

        GirlFriend2 y = new GirlFriend2();
        y.setName("l");
        y.setAge(-18);
        y.setGender("女");

        System.out.println(y.getName());
        System.out.println(y.getAge());//0；非法数据
        System.out.println(y.getGender());
        l.eat();
        l.study();
    }
}




