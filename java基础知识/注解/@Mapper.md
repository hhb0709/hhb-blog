### @Mapper
```
@Documented  
@Inherited  
@Retention(RetentionPolicy.RUNTIME)  
@Target({ElementType.TYPE, ElementType.METHOD, ElementType.FIELD, ElementType.PARAMETER})  
public @interface Mapper {  
}
```


在接口类上添加了@Mapper，在编译之后会生成相应的接口实现类

如果想要每个接口都要变成实现类，那么需要在每个接口类上加上@Mapper注解，比较麻烦，解决这个问题用[[@MapperScan]]