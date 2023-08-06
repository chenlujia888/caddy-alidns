# caddy-alidns
集成了alidns插件的caddy镜像。
## 安装

### 获取阿里云accesskey

- 从阿里云中创建RAM帐户，并获取AccessKeyID和AccessKeySecret。
- 将RAM帐户授权AliyunDNSFullAccess权限
- 将AccessKey和AccessKeySecret填入.env文件中

### 修改Caddyfile
将Caddyfile中的域名替换为自己的域名

### 构建镜像
```
docker compose build
```

### 从dockerhub拉取镜像

镜像地址为
```
registry.cn-hangzhou.aliyuncs.com/hxtech/caddy-alidns:alpine
```

将docker-compose.yaml中
```
    build: .
    # image: registry.cn-hangzhou.aliyuncs.com/hxtech/caddy-alidns:alpine
```
`build .`注释掉，将`image: registry.cn-hangzhou.aliyuncs.com/hxtech/caddy-alidns:alpine`取消注释。

### 运行镜像
```
docker compose up -d
```