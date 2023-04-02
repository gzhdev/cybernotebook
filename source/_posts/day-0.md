---
title: day 0
date: 2023-04-01 01:52:25
tags: 
    - [其他]
categories: 
    - [其他]
top: 1
---

# 博客的第一天

先不管其他的，来段测试段落先。

```python
import httpx
r = httpx.get('https://www.example.org/')
r.status_code

r.headers['content-type']

r.text

```

```java
package com.java2nb.novel;

import lombok.extern.slf4j.Slf4j;
import org.mybatis.spring.annotation.MapperScan;
import org.springframework.boot.CommandLineRunner;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.boot.web.servlet.ServletComponentScan;
import org.springframework.cache.annotation.EnableCaching;
import org.springframework.context.ApplicationContext;
import org.springframework.context.annotation.Bean;
import org.springframework.scheduling.annotation.EnableScheduling;

import java.net.InetAddress;

/**
 * @author Administrator
 */
@SpringBootApplication
@EnableCaching
@EnableScheduling
@ServletComponentScan
@MapperScan(basePackages = {"com.java2nb.novel.mapper"})
@Slf4j
public class CrawlNovelApplication {

    public static void main(String[] args) {
        SpringApplication.run(CrawlNovelApplication.class);
    }

    @Bean
    public CommandLineRunner commandLineRunner(ApplicationContext ctx) {
        return args -> {
            log.info("项目启动啦，访问路径：{}", "http://" + InetAddress.getLocalHost().getHostAddress() + ":" + ctx.getEnvironment().getProperty("server.port"));
        };
    }


}
```