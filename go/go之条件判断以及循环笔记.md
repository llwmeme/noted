# go之条件判断以及循环笔记
## if else 
```go
const filename  = "abc.txt"
    // go 的逻辑判断不用写括号 go的if之前如果有分号那么分号前面的数据作用域为这个if语句
	if contents,err :=ioutil.ReadFile(filename);err != nil {
    	fmt.Println(err)
	}else{
		fmt.Printf("%s\n",contents)
	}
```
## case when
> go语言的 switch case 无需break ，语言会自动break ,如果没进case 会自动进入else

> fallthrough 可以使程序不进行break操作

> switch 后也可以不加变量如果不加 那么case 后加入条件表达式即可

```go
func testswitch() {
	 const flag = 1
	switch flag {
	case 0:
		print(0)
	case 1:
		println(1)
	case 2:
		print(2)
	case 3:
		// 意思是这条语句走完不进行break操作
        fallthrough
    case flag == 4
         print("如果这么写那么switch后面可以不加入flag变量")
	default:
		print(3)
	}
}
```

##for
> 同样for 也不需要括号 用
```go
// 转换10进制到2进制的算法
func bytetotwo(param int) string  {
    result  :=""
	for ;param>0;param/=2{
		lsb :=param%2;
   	result = strconv.Itoa(lsb) + result
   }
	return result
}
```

> 如果for 后面 只跟了一个表达式那么代表这个for 相当于一个while语句

> 如果一个for 后面什么都没跟 那么代表这个for 是一个死循环
```go
for{
		print("我是一个死循环")
	}
	i := 0
	for scanner.Scan() {
		print("我是一个while")
	}
```

