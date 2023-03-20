# Actions-GL-MT2500
📌GL-MT2500自用固件定制

[![Build GL.INET](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET.yml/badge.svg?branch=main)](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET.yml)

固件版本OpenWrt 21.02

内核版本5.4.211

# 编译包
- 因为固件自带adguardhome的原因就不额外编译了   [**(路由器地址)**](http://192.168.8.1/#/adguardhome)
- luci-theme-argon主题 **(和istore不同时存在)**
- openclash **(旁路由成功)**
- helloworld **(旁路由最推荐,接口控制不绑定)**
- passwall **(内存异常,使用前更新全部规则!旁路由测试成功!)**
- aliyundrive-webdav
- luci-app-alist **（GL-MT2500是21.02，需要改golang版本，目前挂载dav有问题）**
- istore **(自选)**
- docker和luci-lib-dockerman  **(自选)**
- luci-app-broadbandacc
- luci-app-serverchan
- netspeedtest **(和istore冲突)**
- ramfree
- 以下插件试验中
- cloudflarespeedtest
- luci-app-vssr **(测试有问题,另外需要`ln -s /usr/libexec/wget-ssl /usr/bin/wget-ssl`修复一下)**

# Todo

- 无法修改默认IP (192.168.8.1),使其进入就默认旁路由
- 

# Thank
> https://github.com/gl-inet/gl-infra-builder
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