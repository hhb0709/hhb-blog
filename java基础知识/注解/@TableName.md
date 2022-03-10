### @TableName

``` java
@Documented  
@Retention(RetentionPolicy.RUNTIME)  
@Target({ElementType.TYPE, ElementType.ANNOTATION_TYPE})  
public @interface TableName {  

 String value() default "";  
  
 String schema() default "";  
  
 boolean keepGlobalPrefix() default false;  
  
 String resultMap() default "";  
  
 boolean autoResultMap() default false;  
  
 String[] excludeProperty() default {};  
}

```


表名注解，标识实体类对应的表

