#day4
#碎碎念：第一次如此愉快的下雨天，军训直接因为一场雨，下午和晚上都不用军训，太太太爽了!!!!!顺便就可以把javabean的大致内容学完了，嘻~


#就近原则:
 变量在输出时，如果有两个相同名字的变量，一个是成员变量，一个是局部变量，输出时的值是由靠输出语句跟近的变量决定
    private int age；//0，成员变量
    public void method(){
    int age = 10;//局部变量：表示测试类中调用方法传递过来的数据
    sout(age);//10，就近原则：故为10
    sout(this.age)//this.age指代成员变量
 故可以用“this.变量名”来表示成员变量


#构造方法：
 创造对象的时候，虚拟机会自动调用构造方法，作用是给成员变量进行初始化
        
        格式：
        修饰符 类名（参数）{
        方法体
        }
        特点：1.方法名和类名，名字一致
              2.没有返回值类型，无void
              3.没有具体返回值

    两种常用构造：写代码时都应该写
        1.空构造
        public user() {
        }


        2.带全部参数的构造
        public user(String username, String password, String gmail, String gender, int age) {
        this.username = username;
        this.password = password;
        this.gmail = gmail;
        this.gender = gender;
        this.age = age;
        }


package test2;

public class user {
    
    //属性
    private String username;
    private String password;
    private String gmail;
    private String gender;
    private int age;

    //空参构造
    public user() {
    }

    //带全部参数的构造
    public user(String username, String password, String gmail, String gender, int age) {
        this.username = username;
        this.password = password;
        this.gmail = gmail;
        this.gender = gender;
        this.age = age;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public String getGmail() {
        return gmail;
    }

    public void setGmail(String gmail) {
        this.gmail = gmail;
    }

    public String getGender() {
        return gender;
    }

    public void setGender(String gender) {
        this.gender = gender;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}



 #标准的javabean：
    1.类名见名知意，驼峰命名法
    2.成员变量使用private修饰
    3.至少提供两个构造方法：无参构造；带全部参数的构造
    4.成员方法：提供每一个成员变量对应的set和get方法

    

    alt+ins ：一键生成javabean



#胡言胡语：累了，但是发现快捷方法确实很好用啊，现在在用的是12点才拿到的键盘，虽然敲起来很爽，但是本来不熟悉键盘的我，因为这个修改的键盘，打字速度更慢了，QWQ



