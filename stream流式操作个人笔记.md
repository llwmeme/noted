# stream 流式操作
## filter()
 >filter()  主要用来存放过滤条件 

>filter(a -> a.getName.equals('刘乐玮'))
## map()  
> map()主要用来存放需要收集的条件

> 比如map(a->a.getId())

 ## 常用工具
 > Collection.toList()
 
 >将流的结果返回为一个集合

 > Collection.joining("||")

 > 将流的结果返回为一个字符串并用joining的入参拼接

