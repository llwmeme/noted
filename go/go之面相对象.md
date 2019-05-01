# 面相对象
> go的面相对象是由结构体struct实现的

```go
// 这是一个go的结构体
type student struct {
	age , height int 
	weight float64
	name string
}
```

>举个例子新建一个链表
```go 
// 双向链表类型
type treeNode struct {
	left *treeNode
	right *treeNode
	value string
}
```
> 声明这个链表

```go
// 对象的声明
var node treeNode = treeNode{value : "3"}
	node.left = &treeNode{value:"2"}
	node.right =new(treeNode)
```