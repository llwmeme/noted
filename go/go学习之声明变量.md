# go---------变量，常亮,枚举
 >一.声明变量

1.普通声明变量
 ```go
 // 声明变量 类型可自动推断
var param string = 10;
var param = 10；
//:= 可以省略var的写法 但是这种写法必须赋初始值 并且只能定义在func中
param := 10;
```
2.go可以同时声明多个变量
```go
var(
    a = 10
    b = “param”
    c = true
)
// 也可以写成
var a,b,c = 10,"param",true
```
> 二.变量类型

|名称|英语|
|------|--------|
|布尔|bool|
|字符串|string|
|整数|int|
|指针|uintptr|
|字节|byte|
|字符|rune|
|浮点|float|
|负数浮点|complex|

>三.类型转换

1.go只有强制类型转换不会隐式类型转换

>四.常量

>1.常量用const关键字
```go
// 常量 value不可更改 ,同样可以不声明类型
const username string = 'liulewei'
const param1,param2 = "参数1","参数2"
```

>五.枚举

1.最普通的一个枚举
```go
func enums(){
    c = 0 
    java = 1
    c++ = 2
    python = 3
    go = 4
}
```

2.自增枚举使用iota关键字

```go
func enums(){
    c = iota
    java 
    c++ 
    python 
    go 
}
```







