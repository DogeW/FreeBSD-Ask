# 第5.7节 安装 QQ

## Linux QQ 3.x（electron）【可选：基于 ArchLinux 兼容层】

请看第 30 章 Linux 兼容层的 ArchLinux 兼容层部分。

```
# chroot /compat/arch/ /bin/bash #进入 Arch兼容层
# su test # 此时位于 Arch 兼容层！切换到普通用户才能使用 aur，第 30 章已经创建过该用户了！
$ yay -S linuxqq # 此时位于 Arch 兼容层！此时用户为 test
# exit # 此时位于 Arch 兼容层！此时用户恢复为 root
````

```
# export LANG=zh_CN.UTF-8 # 此时位于 Arch 兼容层！
# export LC_ALL=zh_CN.UTF-8 # 此时位于 Arch 兼容层！如果不添加环境变量，则中文输入法无法使用。如果设置失败请重启一次 FreeBSD 主机。此时位于 Arch 兼容层！
# /user/bin/qq --no-sandbox --no-zygote --in-process-gpu # 此时位于 Arch 兼容层！
```

## Linux QQ 3.x（Electron）【可选：基于 Ubuntu 兼容层】

> 请先安装 Ubuntu 兼容层，具体请看第 30 章。

```
# chroot /compat/ubuntu/ /bin/bash #进入 Ubuntu 兼容层
# wget https://dldir1.qq.com/qqfile/qq/QQNT/2355235c/linuxqq_3.1.1-11223_amd64.deb #此时位于 Ubuntu 兼容层
```

```
# apt install ./linuxqq_3.1.0-9572_amd64.deb  #此时位于 Ubuntu 兼容层
```

安装依赖文件和字体：

```
# apt install libgbm-dev libasound2-dev fonts-wqy-microhei  fonts-wqy-zenhei language-pack-zh-hans #此时位于 Ubuntu 兼容层
# ldconfig #此时位于 Ubuntu 兼容层
```

启动 QQ：

```
# export LANG=zh_CN.UTF-8 # 此时位于 Ubuntu 兼容层
# export LC_ALL=zh_CN.UTF-8 # 如果不添加则中文输入法无法使用。此时位于 Ubuntu 兼容层
# /bin/qq --no-sandbox --no-zygote --in-process-gpu #此时位于 Ubuntu 兼容层
```

![](../.gitbook/assets/qq3.0.jpg)


> **注意**
>
>**如果退出后进不去，请加参数 `--in-process-gpu` 执行之即可，即 `/bin/qq --in-process-gpu`**。
