# Homework-2 Answer Key

## 理论部分

1. 一个正确的算法应该具有那些特性？

   ```
   1.有穷性
   2.确定性
   3.可行性
   4.输入
   5.输出
   ```

2. 一个程序有()种基本结构，分别是()。

   ```
   三种 顺序结构 选择结构（也称分支结构）循环结构
   ```

3. C语言的数据类型可分为哪几种？

   ```
   数据类型
   	|——基本数据类型
   	|	|——整型（int）
   	|	|——实形（浮点型）
   	|	|	|——单精度型（float）
   	|	|	|——双精度型（double）
   	|	|——字符型（char）
   	|	|——枚举型（enum）
   	|——构造类型
   	|	|——数组
   	|	|——结构体（struct）
   	|	|——共用体（union）
   	|——指针类型
   	|——空类型（void）
   ```

4. 分别列出循环语句并用自己的话说说它们之间的区别。

   ```
   循环语句有三种 for，  while，  do...while。
   
   for的语法如下
   for (expression1; expression2; expresssion3) {
   	statement
   }
   for循环是最常用的循环， 事实上for循环是while循环的一种极为常见的语句组合形式的简写法。
   
   expression1为初始化部分，只在循环开始时执行一次
   expression2为条件部分，循环体每次执行前都要执行一次
   expression3为初始化部分，循环体执行完毕，在条件部分将要执行前执行一次
   
   while的语法如下
   while （expression） {
   	statement
   }
   while的表达式将会在循环开始前判断，表达式为假，则跳过循环。
   
   do...while的语法如下
   do {
   	statement
   }while (expression);
   do...while循环与while循环很相似， 但是do...while的条件部分会在循环体后执行，这意味着循环体至少执行一次。
   ```

## 实践部分

- 请编写一个程序， 能够输出你自己的姓名，性别，学号，班级。

  - 样例输出：王离 女 19715104 宗教二班

  ```c
  #include <stdio.h>
  
  int main() {
      printf("王离 女 19715104 宗教二班");
      return 0;
  }
  ```

### 加分题

- 请编写一个程序，提示用户输入自己的姓名与班级， 并在换行后输出。

  - 样例输入： 王离 宗教二班
  - 样例输出： 王离 宗教二班
  - 提示：该程序越完善越好， 例如对错误的输入有相应的处理等
  - 对输入无检查版本

  ```c
  //头文件， 有了这个才能用scanf和printf函数
  #include <stdio.h>
  //主函数，程序的入口
  int main() {
      //打印提示信息
      printf("Please enter your id and name:\n");
      //声明变量，用来存储学生信息
      char id[10];
      char name[10];
      //等待用户输入
      scanf("%s%s", &id, &name);
      //输出信息
      printf("%s %s", id, name);
      //结束程序
      return 0;
  }
  ```
   - 对输入有检查版本
  
  ```c
  //头文件， 有了这个才能用scanf和printf函数
  #include <stdio.h>
  //头文件， 为C语言提供了布尔型（bool）的变量
  #include <stdbool.h>
  //头文件， 提供了&& 与 || 的更有可读性的用法
  #include <iso646.h>
  //头文件， 有了这个就能使用memset函数了
  #include <string.h>
  //使用const关键字， 定义整型（int）常量，表示name可接受的最大长度
  const int MAX_NAME_LENGTH = 15;
  //创建一个检查id是否合法的函数，如果id合法返回true否则返回false
  bool id_valid(char* id) {
      if (id[0] == '1' and id[1] == '9') {
          return true;
      } else {
          return false;
      }
  }
  //创建一个检查name是否合法的函数，如果id合法返回true否则返回false
  bool name_valid(char* name) {
      //计数器， 用来记录name的位数
      int counter = 0;
      for (int index = 0; index < 30; index ++) {
          //c语言中一般以‘\0’代表字符串末尾，可以用来判断字符串位数
          if (name[index] != '\0') {
              counter += 1;
          }
      }
  
      if (counter < MAX_NAME_LENGTH) {
          return true;
      } else {
          return false;
      }
  }
  
  //主函数，程序的入口
  int main() {
      //打印提示信息
      printf("Please enter your id and name:\n");
  
      //声明变量，用来存储学生信息
      char id[10];
      char name[30];
      //循环， 当用户输入不合法时要求重新输入， 直至合法未知
      do {
          printf("Id's header is 19 and name must be less than 15 letters.\n");
          //清空数组
          memset(id, 0, sizeof(id));
          memset(name, 0, sizeof(name));
          //等待用户输入
          scanf("%s%s", &id, &name);
          //任意一项不合法，就要求用户重新输入
      } while (!id_valid(id) or !name_valid(name));
  
      //输出信息
      printf("%s %s", id, name);
      //结束程序
      return 0;
  }
  ```
  
  
## 数学部分

- （公式实在是太多了，什么倍角， 半角， 和差化积， 积化和差等等。搜索引擎上一搜便知）
- 这里还是给出一个[链接](https://zhuanlan.zhihu.com/p/20102140)

## 英语部分

- 每个人翻译的水准，对文章的理解不同， 都会产生不一样的感受与结论，这里之作阅读要求，无需翻译。