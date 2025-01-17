# 第3.3节 gitup 的用法

> FreeBSD 14.0 已经删除了 portsnap，转而使用 git，如本文所述可以使用 gitup 替代之。

```
# pkg install gitup #安装 gitup
# gitup ports #获取 ports
# gitup release #获取 release 版本的源代码
```

## 境内 Git 镜像站

<https://git.freebsd.cn>

使用说明：

```
# ee /usr/local/etc/gitup.conf
```

将
```
                "host"           : "git.freebsd.org",
```

中的 `org` 改为 `cn` 即可：

```
                "host"           : "git.freebsd.cn",
```

拉取 ports：

```
# gitup ports
```

## 故障排除：速度太慢（若不使用 freebsd.cn 镜像站）

设置 HTTP 代理

`gitup` 的代理不取决于系统代理，而是由其配置文件单独决定。

`# ee /usr/local/etc/gitup.conf`

示例（先删去前边的 # 再改）

```
"proxy_host" : "192.168.27.1",
"proxy_port" : 7890,
```

参考链接：

[https://www.freebsd.org/cgi/man.cgi?query=gitup\&sektion=1\&manpath=freebsd-release-ports](https://www.freebsd.org/cgi/man.cgi?query=gitup\&sektion=1\&manpath=freebsd-release-ports)

[https://www.freshports.org/net/gitup](https://www.freshports.org/net/gitup)

[https://github.com/johnmehr/gitup](https://github.com/johnmehr/gitup)
