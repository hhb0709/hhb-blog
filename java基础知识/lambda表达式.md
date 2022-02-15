>lambda表达式就是一个代码块，以及必须传入代码的变量规范

使用lambda表达式的重点是 **延迟执行**（deferred execution）

> 如果设计你自己的[[接口]]，其中只有一个抽象方法，可以用 @FunctionalInterface 注解来标记[[接口]]，这样做有两个有点。
> （1）如果无意增加了另一个非抽象的方法，编译器会产生一个错误信息；
> （2）javadoc页会指出你的[[接口]]是一个函数式的[[接口]]；
> 并不是所有的函数式[[接口]]都需要这个注解，任何**只有一个抽象方法**的[[接口]]都是函数式[[接口]]。



``` java
ActionListener listener = event -> {  
    System.out.println(event.getActionCommand());  
};
```

``` java
String[] str = new String[]{"123","456"};

Arrays.sort(str, (s1, s2) -> {  
    return s1.length() - s2.length();  
});

```

#### 函数式[[接口]]（functional interface）
>对于**只有一个抽象方法**的[[接口]]，需要这种[[接口]]对象时，就可以提供一个lambda表达式

``` 
## [[[[[[[[接口]]]]]]]]
public interface SendSuccess {  
    public void isSuccess(boolean isSuccess);  
}
```

```
public class MailSyncer {  
    public void sync(SendSuccess sendSuccess) {  
        sendSuccess.isSuccess(false);  
 }  
}	
```

```
new MailSyncer().sync(s->{  
    if(s){  
        System.out.println(s);  
 }  
});
```

### 方法引用
```
Timer t1 = new javax.swing.Timer(1000, event -> System.out.println(event));  
Timer t2 = new javax.swing.Timer(1000, System.out::println);
```
以上两种写法是等价的

方法引用的三种写法
- object::instanceMethod
- Class:staticMethod
- Class:instanceMethod

### 构造器引用
