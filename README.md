# Actions-GL-MT2500
📌GL-MT2500自用固件定制

[![Build GL.INET MT2500](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET_Lite.yml/badge.svg)](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET_Lite.yml)

固件版本OpenWrt 21.02

内核版本5.4.211

4.2.0 package

# 编译包
- 因为固件自带adguardhome的原因就不额外编译了   [**(路由器地址)**](http://192.168.8.1/#/adguardhome)
- luci-theme-argon主题和设置
- openclash **(旁路由成功)**
- helloworld **(旁路由成功,经常网络波动,疑似自动切换节点检测导致)**
- passwall **(旁路由成功,内存异常,使用前务必更新全部规则!)**
- aliyundrive-webdav
- luci-app-alist **(开放外网访问)**
- ~~luci-app-broadbandacc~~
- luci-app-serverchan
- netspeedtest **(和istore冲突)**
- ramfree
- 以下插件试验中
- cloudflarespeedtest
- istore **(自选)**
- docker和luci-lib-dockerman  **(自选)**
- ~~luci-app-vssr **(测试有问题,且和SSR重复,不纳入)**~~


# Todo

- 无法修改默认IP (192.168.8.1),使其进入就默认旁路由
- 
# 旁路由

官方界面自带设置即可


# Thank
> https://github.com/gl-inet/gl-infra-builder
>
> https://github.com/gl-inet/glinet4.x
> 
> https://github.com/JiaY-shi/build-gl.inet
> 
> https://github.com/luochongjun/gl-sdk-action
> 
> [P3TERX](https://p3terx.com)
>
> https://github.com/ecrasy/BuildOpenWrt
> 
> https://github.com/draco-china/Draco-OpenWrt-GL-AX1800
>
> https://github.com/AoThen/Openwrt-Packages.git
>
> https://github.com/kenzok8/small-package
>
> https://github.com/kiddin9/openwrt-packages
> 