# Alpine Linux

## 地址

<https://mirrors.ustc.edu.cn/alpine/>

## 说明

Alpine Linux 软件源

## 收录架构与版本

收录 Alpine 所有架构的仍然受到支持的版本。

## 使用说明

一般情况下，将 `/etc/apk/repositories`
文件中 Alpine 默认的源地址 `http://dl-cdn.alpinelinux.org/` 替换为
`http://mirrors.ustc.edu.cn/` 即可。

可以使用如下命令：

```shell
sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories
```

也可以直接编辑 `/etc/apk/repositories` 文件。以下是 v3.20 版本的参考配置：

```text
https://mirrors.ustc.edu.cn/alpine/v3.20/main
https://mirrors.ustc.edu.cn/alpine/v3.20/community
```

也可以使用 `latest-stable` 指向最新的稳定版本：

```text
https://mirrors.ustc.edu.cn/alpine/latest-stable/main
https://mirrors.ustc.edu.cn/alpine/latest-stable/community
```

更改完 `/etc/apk/repositories` 文件后请运行 `apk update` 更新索引以生效。

!!! tip

    使用 HTTPS 可以有效避免国内运营商的缓存劫持。

## 相关链接

官方主页

:   <https://www.alpinelinux.org/>

邮件列表

:   <https://lists.alpinelinux.org/>

论坛

:   <https://forum.alpinelinux.org/forum>

Wiki

:   <https://wiki.alpinelinux.org/>
