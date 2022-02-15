测试的时候，需要在Main方法中执行一些代码，打成jar包时需要将第三方jar的也打进目标jar包。

``` xml
<plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-jar-plugin</artifactId>
                <version>2.4</version>
                <configuration>
                    <archive>
                        <manifest>
                            <useUniqueVersions>false</useUniqueVersions>
                            <addClasspath>true</addClasspath>
                            <classpathPrefix>lib/</classpathPrefix>
                            <mainClass>com.wyz.Main</mainClass>
                        </manifest>
                    </archive>
                </configuration>
</plugin>
```

### 把第三方jar包下载到lib目录

``` xml
<plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-dependency-plugin</artifactId>
                <executions>
                    <execution>
                        <id>copy-dependencies</id>
                        <phase>package</phase>
                        <goals>
                            <goal>copy-dependencies</goal>
                        </goals>
                        <configuration>
                            <!-- 拷贝项目依赖包到lib/目录下 -->
                            <outputDirectory>${project.build.directory}/lib</outputDirectory>
                            <!-- 间接依赖也拷贝 -->
                            <excludeTransitive>false</excludeTransitive>
                            <!-- 带上版本号 -->
                            <stripVersion>false</stripVersion>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
```


### 把依赖也打进jar包：mainClass是jar包的main方法入口
``` xml
<build>
        <plugins>
            <plugin>
                <artifactId>maven-assembly-plugin</artifactId>
                <configuration>
                    <archive>
                        <manifest>
                            <mainClass>com.wyz.Main</mainClass>
                        </manifest>
                    </archive>
                    <descriptorRefs>
                        <descriptorRef>jar-with-dependencies</descriptorRef>
                    </descriptorRefs>
                </configuration>
            </plugin>
        </plugins>
    </build>
```

![[Pasted image 20220119113605.png]]