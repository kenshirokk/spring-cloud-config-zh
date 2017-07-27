# 快速开始

启动服务器

```shell
$ cd spring-cloud-config-server
$ ../mvnw spring-boot:run
```

这个服务也是一个Springboot项目,所以如果你愿意,你也可以在你的IDE种直接运行(main class是ConfigServerApplication).然后实验一个客户端.

```shell
$ curl localhost:8888/foo/development
{"name":"development","label":"master","propertySources":[
  {"name":"https://github.com/scratches/config-repo/foo-development.properties","source":{"bar":"spam"}},
  {"name":"https://github.com/scratches/config-repo/foo.properties","source":{"foo":"bar"}}
]}
```

定位属性源的默认策略是克隆一个git仓库(通过spring.cloud.config.server.git.uri指定), 然后用它初始化一个迷你的SpringApplication. 这个迷你的SpringApplication的环境用语枚举属性源并通过一个JSON终端发布出来.

拥有资源的HTTP服务通过下面形式

```shell
/{application}/{profile}[/{label}]
/{application}-{profile}.yml
/{label}/{application}-{profile}.yml
/{application}-{profile}.properties
/{label}/{application}-{profile}.properties
```

