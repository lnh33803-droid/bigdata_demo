#day1
#碎碎念：
 也是正式开启了大学生活啊，也是成功体验了两节体验感截然不同的水课，没话说，但是越学越觉得编程好难啊，坚持不下去一点，明天就要上大学第一节
 python课了，其实前面学的一点python也全都忘光就是了，www已老实

#也是又写了一个学生管理系统的雏形好吧，感觉挺难的wwww



package test8;

public class Student {
    private int id;
    private String name;
    private int age;

    public Student() {
    }

    public Student(int id, String name, int age) {
        this.id = id;
        this.name = name;
        this.age = age;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}

package test8;

public class test {
    public static void main(String[] args) {
        Student[] arr = new Student[3];

        Student p1 = new Student(1, "小红", 12);
        Student p2 = new Student(2, "heima002", 18);
        Student p3 = new Student(3, "小明", 18);

        //录入至数组（总是忘）
        arr[0]= p1;
        arr[1]= p2;
        arr[2]= p3;

        //创建一个新对象
        Student p4 = new Student(4,"xd",3);

        //对学号唯一性进行判断
        boolean flag= contains(arr, p4.getId());
        if(flag){
            System.out.println("学号重复");
        }else{
            //添加到数组
            //判断数组是否满了
            int count = getCount(arr);
            //旧数组已经满了
            if(count == arr.length){
                //创造一个新的数组来记录数据
                Student[] newArr = creatArr(arr);
                newArr[count] = p4;
                //遍历获取所有学生信息
                print(newArr);
            }else {
                //旧数组未满
                arr[count]=p4;
                //遍历获取所有学生信息
                print(arr);
            }
        }
    }


    //要输出一个是否重复的判断，故返回值是boolean
    public static boolean contains(Student[]arr, int id){
        for (int i = 0; i < arr.length; i++) {
            Student stu = arr[i];
            //获取学生数组中的id
            int sid=stu.getId();
            if(sid == id){
                return true;
            }
        }
        return false;
    }
    public static int getCount(Student[] arr){
        int count =0;
        for (int i = 0; i < arr.length; i++) {
            if(arr[i] != null){
                count++;
            }
        }
        return count;
    }
    //创建一个新的数组,并拷贝数据
    public static Student[] creatArr(Student[] arr){
        Student[] newArr = new Student[arr.length+1];
        for (int i = 0; i < arr.length; i++) {
            newArr[i]=arr[i];
        }
        return newArr;
    }

    public static void print(Student[] arr){
        for (int i = 0; i < arr.length; i++) {
            Student stu = arr[i];
            if(arr[i] != null ){
                System.out.println(stu.getId()+","+stu.getName()+","+stu.getAge());
            }
        }

    }
}



package test8;

public class test2 {
    public static void main(String[] args) {
        Student[] arr = new Student[3];

        Student p1 = new Student(1, "小红", 12);
        Student p2 = new Student(2, "heima002", 18);

        //录入至数组（总是忘）
        arr[0] = p1;
        arr[1] = p2;

        //通过id删除学生
        //即删除id对应的索引，将其变为null
        //获取对应Id的索引
        int index = getIndex(arr, 2);
        if (index >= 0) {
            arr[index] = null;
            print(arr);
        } else {
            //没有这个id，删除失败
            System.out.println("id不存在，删除失败");
        }

    }


    public static void print(Student[] arr) {
        for (int i = 0; i < arr.length; i++) {
            Student stu = arr[i];
            if (arr[i] != null) {
                System.out.println(stu.getId() + "," + stu.getName() + "," + stu.getAge());
            }
        }
    }

    public static int getIndex(Student[] arr, int id) {
        for (int i = 0; i < arr.length; i++) {
            Student stu = arr[i];
            if (stu != null) {
                int sid = stu.getId();
                if (sid == id) {
                    return i;
                }
            }
        }
        return -1;
    }


}


package test8;

public class test3 {
    public static void main(String[] args) {
        Student[] arr = new Student[3];

        Student p1 = new Student(1, "小红", 12);
        Student p2 = new Student(2, "heima002", 18);
        Student p3 = new Student(3, "小明", 18);
        //录入至数组（总是忘）
        arr[0] = p1;
        arr[1] = p2;
        arr[2] = p3;

        //查询id 将Id为2 的年龄+1
        int index = getIndex(arr, 4);
        if (index >= 0) {
            //找到了id为2的索引
            //获取数组里的数据
            Student stu = arr[index];
            int newAge = stu.getAge()+1;
            stu.setAge(newAge);
            print(arr);
        } else {
            //没有这个id，删除失败
            System.out.println("id不存在");
        }

    }


    public static void print(Student[] arr) {
        for (int i = 0; i < arr.length; i++) {
            Student stu = arr[i];
            if (arr[i] != null) {
                System.out.println(stu.getId() + "," + stu.getName() + "," + stu.getAge());
            }
        }
    }

    public static int getIndex(Student[] arr, int id) {
        for (int i = 0; i < arr.length; i++) {
            Student stu = arr[i];
            if (stu != null) {
                int sid = stu.getId();
                if (sid == id) {
                    return i;
                }
            }
        }
        return -1;
    }


}


#胡言胡语：
    就这样吧 累了




