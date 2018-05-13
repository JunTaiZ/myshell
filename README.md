# myshell

## 简介

>用C语言实现的一个简易的shell，能够接受用户输入的命令并执行操作，支持多重管道及重定向 
>程序运行后，会模拟shell用绿色字体显示当前的用户名、主机名和路径，等待用户输入命令。程序逐次读取用户输入的指令后，将指令按空格拆分成多个字符串命令，然后判断该命令的类型。若命令有误，则用红色字体打印出错误信息

>* 若为exit，则调用自定义的exit函数，向该程序进程发送terminal信号结束该进程
>* 若为cd，则判断参数，调用chdir()函数修改当前的路径，并返回相应的结果。若修改成功，则使用getcwd()函数更新当前路径
>* 若为其它命令，则先判断命令是否存在，然后再判断是否有合法的管道。若命令合法，则再执行命令，执行命令时先判断命令是否有重定向，再执行相应的操作。管道使用递归执行，支持多重管道。

## 功能

>- [x] 显示当前用户名、主机名和工作路径
>- [x] exit命令
>- [x] cd命令
>- [x] 判断命令是否存在
>- [x] 执行外部命令
>- [x] 实现输入、输出重定向
>- [x] 递归实现多重管道

## 博客

> 本项目的具体讲解、演示已写在[博客](https://blog.csdn.net/feng964497595/article/details/80297318)中，欢迎大家一起探讨学习。