# 声明函数

> 声明方法

```go
// 普通的一个方法 规格和java差不多
// func:方法标识 simplefunction：函数名 (str string):string类型入参 string：返回值
func simplefunction(str string) string {
	return str
}
// 接收者(个人认为如果叫调用者更为形象)
// 这种写法可以使用(tree treeNode)中的tree作为调用者 也就是调用者模式
func (tree treeNode) simplefunction2() string{
    fmt.Println(tree.value)
    return ""
}
```

> 调用区别
```go
fmt.Println(simplefunction(""))
node.simplefunction2();
```

