# 新建Symfony4项目

1. 我使用symfony只是来做API接口开发, 所以选择skeleton而不是web-sketon.
```
$ composer create-project symfony/skeleton my-project
```

# 本地快捷开发

### 直接php内置的webserver进行开发
```
$ php -S localhost -t public
```

### 使用symfony提供的web-server-bundler进行开发

1. 安装
```
$ composer require server --dev
```

2. 运行
```
# 本地环境运行, 默认8000端口
$ php bin/console server:run
# 如果是虚拟机上运行，可以指定IP
$ php bin/console server:run 0.0.0.0:8000
```

3. 其他命令
```
# 后台运行服务(守护进程), 需要安装php的pcntl扩展库
# pcntl库无法在非Unix系统上安装(如Windows)
$ php bin/console server:start
# 停止服务
$ php bin/console server:stop
# 查看服务状态
$ php bin/console server:status
```
