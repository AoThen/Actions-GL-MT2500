# Actions-GL-MT2500
📌GL-MT2500自用固件定制

![GL-MT2500](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET.yml/badge.svg)

固件版本OpenWrt 21.02

内核版本5.4.211

# 编译包
- 因为固件自带adguardhome的原因就不额外编译了   [**(路由器地址)**](http://192.168.8.1/#/adguardhome)
- luci-theme-argon主题 **(和istore不同时存在)**
- openclash **(旁路由成功)**
- helloworld **(旁路由最推荐,接口控制不绑定)**
- aliyundrive-webdav
- luci-app-alist **（GL-MT2500是21.02，需要改golang版本，目前挂载Webdav有问题）**
- istore **(自选)**
- luci-app-broadbandacc
- luci-app-serverchan
- docker和luci-lib-dockerman
- netspeedtest **(和istore冲突)**
- 以下插件试验中
- passwall **(旁路由没成功,待测试正常路由模式)**
- 

# Todo

- 修改默认IP
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