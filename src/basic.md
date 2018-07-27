1.	标识符：Java对各种变量、方法和类等要素命名时使用的字符序列称为标识符
（1）	标识符由字母、数字、下划线”_”、美元符号”$”组成，首字母不能是数字。
（2）	不能使用Java关键字作为标识符
（3）	标识符没有长度限制
（4）	标识符对大小写敏感
2.	变量和方法的命名，第一个单词应以小写字母开头，后面每个单词要以大写字母开头，如setName
3.	类名的命名，第一个单词的首字母需要大写，如HelloWorld;
4.	变量是一段有名字的连续存储空间。
5.	在Java中，利用final关键字来定义Java常量，其本质为不可变的变量。
6.	Java基本数据类型：byte、short、int、long、float、double 、char、boolean
引用数据类型：类（class）、接口（interface）、数组（array）
7.	成员变量和局部变量
成员变量：作用域从变量定义开始到类结束
局部变量：作用域从变量定义开始到方法结束
8.	Java运算符
++i 先自增再运算   i++先运算再自增
--I  先自减再运算   --I先运算再自减
运算符顺序：() [] . ! + - ~ ++ -- * / %
9.	If语句
if(表达式){
Scanner input=new Scanner(Systen.in);
	 代码块
}else{
代码块
}
10.	Switch语句
switch(表达式){
  case:常量一;
		break;
	 case:常量二;
		 break;
default:
  代码块X;
   break;
}
Switch表达式的值只允许是byte、short、int、char类型（JDK7.0中可以是String）;
Default表示当前表达式的实际值没有匹配到前面对应的任何case常量，default后面的代码块会被执行。
11.	while语句
while(循环条件){
循环代码块
}
While是先判断循环条件再执行循环代码块;
12.	do….while语句
do{
  循环代码块
}while(循环条件);
Do…while先执行代码块再判断循环条件，所以do..while至少会被执行一次。
13.	for循环
for(表达式1;表达式2;表达式3){
  循环代码块
}
表达式1通常为赋值语句，是循环语句的初始化部分，为循环参数赋值
表达式2通常为条件语句，即循环条件（表达式2可省略，变成死循环）
表达式3通常为赋值语句，当一次循环代码块执行完后，程序执行表达式3，然后再去判断表达式2 是否满足 （也可省略，循环代码块中添加循环参数即可）
Example：求100之间的和。
 public class Test05 {
    public static void main(String[] args) {
        int sum=0;
        for (int i =0;i<=100;i++){
            sum=sum+i;
        }
        System.out.println(sum);
    }
}
14.	break和continue的区别：
break是跳出循环执行循环之后 的代码；
continue是终止本次循环继续下一次循环
15.	递归调用
求10的阶乘
 public class Test06 {
    static long factorial(int n){
        if (n==1){      //判断条件，一旦满足条件不再递归，逐层返回
            return 1;
        }
        long sum=factorial(n-1);   //递归调用
        return sum*n;     //，逐层返回求阶乘
    }

    public static void main(String[] args) {
        System.out.println(factorial(10));
}
}
16.	数组
一维数组：int name[]=new int[5];  或int[] name=new int[5]   //5表示数组的长度

