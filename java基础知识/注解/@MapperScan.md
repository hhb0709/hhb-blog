## @MaperScan

用于设置Mapper扫描路径，spring boot将从这些路径下读取Mapper类。

在这种情况下，不需要给每个 [[接口]] 添加 [[@Mapper]] [[注解]]


``` java
@SpringBootApplication   
@MapperScan({"com.kfit.*.mapper","org.kfit.*.mapper"})   
public class App {   
 public static void main(String[] args) {   
 SpringApplication.run(App.class, args);   
 }   
}
```

包扫描程序回去这些包下，查找Mapper文件，并放入对象容器中。