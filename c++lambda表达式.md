## 格式
\[ 包含内容 ] ( 参数 ) { 函数体 };
<br>
其中包\[ ]含内容可以为:<br>
- *=:所有变量按值传递*
- *&:所有变量按引用传递valName:传指定变量的值*
- *&valName:传指定变量的引用*
***
执行lambda表达式的话,在后面加一个"()"<br>
lambda表达式可以有返回值,格式如下:<br>
`int i = [=]()->int{return 1;}();`
***
当按值传递时,必须加上mutable才能修改值
[=]()mutable{++val;}();


lambda表达式可以和函数指针一起用
```
int(*func)(int a)= [](int a)->int {return a; };
std::cout<<func(a);
```
但是\[ ]里不能有内容
  
