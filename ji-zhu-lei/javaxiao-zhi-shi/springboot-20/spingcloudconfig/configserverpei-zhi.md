pom依赖

```XML
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-config-server</artifactId>
        </dependency>
```

启动类注解

```java
@SpringBootApplication
@EnableConfigServer
public class ConfigserverApplication {
    public static void main(String[] args) {
        SpringApplication.run(ConfigserverApplication.class, args);
    }

}
```

application.properties配置

```
# 配置git仓库地址
spring.cloud.config.server.git.uri=
# 配置仓库路径
spring.cloud.config.server.git.search-paths=/
# 配置仓库的分支
spring.cloud.config.label=master

# 访问git仓库的用户名
spring.cloud.config.server.git.username=
# 访问git仓库的用户密码 如果Git仓库为公开仓库，可以不填写用户名和密码，如果是私有仓库需要填写
spring.cloud.config.server.git.password=

```



