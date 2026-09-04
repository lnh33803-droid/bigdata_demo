#day1
#碎碎念：最近发现假期快结束了，加速进入java学习阶段，学完基础就赶紧去学python基础了，好忙，有点害怕上了大学然后坚持不下去，md，不努力是找不到工作的lh，服了

#java
    1.if （貌似和python相似）
     格式：if(关系表达式){
           语句体1
             }else{
            语句体2
             }

        对布尔类型的数据进行判断，建议不要用==
        括号内是true就执行if语句块，false就执行else语句块，else语句块可以省略
        boolean a = true;
        if(a) {
            System.out.println("True");
        }else{
            System.out.println("false");
             }


    2.switch
     格式：
            switch(表达式){
            case 值1:{
            语句1;
            break;
            }
            case 值2:{
            语句2;
            break;
            }
            default:{
            语句3;
            break;
            }
        }

        default的位置和省略
            default的位置：可以写在任意位置，但是习惯最后
            default可以省略，不建议
         

        case的穿透
            如果case执行完毕没有遇到break，就会继续执行下一个case，直到遇到break为止
            使用场景：
            如果多个case语句体重复了，可以考虑用case穿透去简化

        switch的简化
            switch (week){
            case 1,2,3,4,5 ->System.out.println("工作日");
            case 6,7 ->System.out.println("休息日");
            default->System.out.println("输入错误");
        }


    #区分
        if  多用于对范围的判断
        switch 用于有限个数据一一列举




#胡言胡语：明天学循环了，www，一定要起的来啊







