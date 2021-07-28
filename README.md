# luci-app-ttnode

一个运行在 openwrt 下的甜糖星愿自动采集插件。

### 介绍

脚本参考网友 Tom Dog 的 Python 版自动采集插件，使用 LUA 重写，基于 LUCI 的实现。

### 如何使用

假设你的 lean openwrt（最新版本 19.07） 在 lede 目录下

```
cd lede
echo 'src-git xepher https://github.com/jerrykuku/luci-app-ttnode.git'>>feeds.conf.default
rm -rf tmp/

./scripts/feeds update -a
./scripts/feeds install -a -p jerrykuku

make menuconfig #Check LUCI->Applications->luci-app-ttnode
make -j1 V=s
```

### 如何安装

🛑 [点击这里去下载最新的版本](https://github.com/jerrykuku/luci-app-ttnode/releases)

1.先安装依赖

```
opkg update
opkg install luasocket lua-md5 lua-cjson luasec
```

1.将 luci-app-ttnode.ipk 上传到路由器，并执行 opkg install /你上传的路径/luci-app-ttnode\*.ipk

### 源自@jerrykuku大佬的源码，小改自用
