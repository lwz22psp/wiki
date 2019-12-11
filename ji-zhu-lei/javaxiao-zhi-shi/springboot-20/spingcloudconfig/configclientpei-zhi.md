pom配置

```
        <dependency>
            <groupId>org.springframework.cloud</groupId>
            <artifactId>spring-cloud-starter-config</artifactId>
        </dependency>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-actuator</artifactId>
        </dependency>
```

bootstrap.properties配置

```
# 远程仓库的分支
spring.cloud.config.label=master
# dev 开发环境配置文件 |  test 测试环境  |  pro 正式环境
# 和git里的文件名对应
spring.cloud.config.profile=uat

# 指明配置服务中心的网址
spring.cloud.config.uri= 


# spring cloud refresh
management.endpoints.web.exposure.include=*
```

java调用

```
@Value("${regis.code}")
private String env;
```

配置值更新后刷新现有值

```
/actuator/refresh
```



