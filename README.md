> 一个帮你在Hyperf开发时快速重启服务的小工具
### 安装
```shell
composer requried daodao97/hyperf-watch dev-master
```
### 修改`composer.json`
```json
{
  "scripts": {
    "watch": [
      "Composer\\Config::disableProcessTimeout",
      "./vendor/bin/watch"
    ]
  }
}
```
`Composer\\Config::disableProcessTimeout` 帮助解除`composer`命令超时问题

`./vendor/bin/watch` 默认扫描根目录下除`vendor`外的`php`文件

`./vendor/bin/watch vender/***` 也可追加其他目录
