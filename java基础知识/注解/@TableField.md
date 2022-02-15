``` Java
@Documented  
@Retention(RetentionPolicy.RUNTIME)  
@Target({ElementType.FIELD, ElementType.ANNOTATION_TYPE})  
public @interface TableField {  
    String value() default "";  
  
 boolean exist() default true;  
  
 String condition() default "";  
  
 String update() default "";  
  
 FieldStrategy insertStrategy() default FieldStrategy.DEFAULT;  
  
 FieldStrategy updateStrategy() default FieldStrategy.DEFAULT;  
  
 FieldStrategy whereStrategy() default FieldStrategy.DEFAULT;  
  
 FieldFill fill() default FieldFill.DEFAULT;  
  
 boolean select() default true;  
  
 boolean keepGlobalFormat() default false;  
  
 String property() default "";  
  
 JdbcType jdbcType() default JdbcType.UNDEFINED;  
  
 Class<? extends TypeHandler> typeHandler() default UnknownTypeHandler.class;  
  
 boolean javaType() default false;  
  
 String numericScale() default "";  
}
```


- exist: 字段是否存在

