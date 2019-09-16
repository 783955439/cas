## Homework-3

---

## 理论部分

1. 请用自己的话说明什么是标识符并说说命名标识符需要注意哪些问题。

   ```
   标识符即为变量，函数，数组，指针等的名字
   
   1.所有的标识符必须以字母或下划线开头，不能使用数字或符号作为开头
   2.英文字母的大小写代表不同的标识符
   3.标识符不能是关键字。
   4.标识符最好具有特定的含义
   5.标识符可以是任意长度，但外部名必须至少能由前8个字符唯一的区分
   ```

   

2. int，long，float和double的分别表示的数据范围是（）。

   ```
   int: 		-2^31 ~ (2^31 - 1)
   long: 		-2^31 ~ (2^31 - 1) 
   float:		-3.4E + 38 ~ 3.4E + 38
   double: 	负值取值范围为 -1.7976E+308 到 -4.94065645841246544E-324
   	    	正值取值范围为 4.94065645841246544E-324 到 1.797693E+308
   ```

   

3. c语言中运算符可分为（）种，分别为（）。

   ```
   10 
   1.算数运算符
   2.关系运算符
   3.逻辑运算符
   4.位操作运算符
   5.赋值运算符
   6.条件运算符
   7.逗号运算符
   8.指针运算符
   9.求字节数运算符
   10.特殊运算符
   ```

   

4. 请说出c语言类型转换规则

   ```mermaid
   graph TD;
   	char --> int;
   	short --> int;
   	int --> unsigned;
   	unsigned --> long;
   	long --> double;
   	float --> double;
   ```

5. 格式字符共有哪几种，其含义分别代表什么？输入与输出的格式字符有哪些相同点和不同点。

   详见[printf](https://baike.baidu.com/item/printf/7467706)与[scanf](https://baike.baidu.com/item/scanf/10773316)

   ## 实践部分

   - 动手写一个C程序计算一元一次方程 $ax + b = 0$的值。采用scanf输入a，b 的数据。输出精确到小数点后两位。

   - ```c
     #include <stdio.h>
     
     int main() {
         double a;
         double b;
         
         printf("Please enter a and b:(a can't be zero)\n");
         scanf("%lf%lf", &a ,&b);
         
         if (a == 0) {
             printf("Error");
             return -1;
         } else {
             printf("x = %.2f", -b/a);
         }
         
         return 0;
     }数学部分
     ```

   ## 数学部分

   - 请将129转换为二进制数，写出详细计算过程

   - ![1568561771096](C:\Users\AbeliaNymph\AppData\Roaming\Typora\typora-user-images\1568561771096.png)

     

     