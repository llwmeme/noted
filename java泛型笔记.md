# 泛型
## 普通泛型
```java
// String类型集合
List<String> stringList = new ArrayList<>();
// User 类型集合
List<User> userList = new ArrayList<>();
```
> 这个没什么花头 只是类型固定提高java工作效率,增加代码可读性，减少bug作用。
## 泛型 T E K V
> 这几个泛型本质上没有什么区别

> 主要用处是见名知意

|泛型|英文|中文|
|-------|--------|----------|
|T|type|类型|
|E|Entity|实体类|
|K|key|键|
|V|value|值|
```java
public class Test<T> {    
  private T t;
  public void set(T t){
    this.t = t;
  }
   public static void main(String[] args) {
        Test<String> test = new Test<String>();
        // 上方Test被声明成了一个字符串类型test里就可以传递字符串的值
        test.set("hello");
    }}
}
```
> 泛型也可以为多个比如
```java
public class Test<T1,T2,T3> {
   public void print(T1 t1,T2 t2,T3 t3){
        System.out.println(t1.getClass());
        System.out.println(t2.getClass());
        System.out.println(t3.getClass());
    }
}
```
> 泛型也可以为关联的两个类
```java
// T以及T的子类
List<T extends ?> list = new ArrayList<>();
// T或者T的父类
List<T super ?> list = new ArrayList<>();
```

