# 数组
> 直接上代码吧
```go
    var arr1 [5]int
	arr2 := [3]int{1,2,3}
	// 编译器会判断长度
    arr3 :=[...]int{2,4,5,64,5,4,5}
    // 二维数组
    var grid [3][4]bool
```
>打印数组的方法
```go
// i代表下表 v代表值
// range关键字 便利的循环数组
for i,v:=range arr3{
		fmt.Println(i,v)
	}
```

# 切片
> 不声明数组的长度那么他就是一个切片
> 切片是引用传递，且会修改原数组
```go
	arr4 :=[...]int{0,1,2,3,4,5,6,7,8,9,0}
	// 切片的几种写法
	fmt.Println(arr4[2:6])
	fmt.Println(arr4[:6])
	fmt.Println(arr4[1:])
```

```go
    arr :=[...]int{0,1,2,3,4,5,6,7,8}
    // 声明一个arr的切片长度为2
    s :=arr[2,3];
    // 虽然s长度只有2 不存在下表2和下表3 ,但是其实s 有记录这个arr数组 如果s1请求的下标越界了就会去向原数组向后扩展
    // s1 的值 会是 4,5
    // 但是s1 不发向s前扩展
    s1 :=s[2,3];
```

> go语言删除/ 增加
```go
// go语言插入
arr :=[...]int{0,1,2,3,4,5,6,7,8,9}
s := arr[0:6]
// 向s后面添加一个元素
fmt.Println(s)
s = append(s,2);
fmt.Println(s)
// 移除第一个元素
s = s[1:]
fmt.Println(s)
// 移除最后一个元素
s = s[:len(s)-1]
fmt.Println(s)
// 移除一个中间元素  ...的意思是把切片里的值全都拿出来
s = append(s[0:2],s[3:5]...)
fmt.Println(s)
```





