# Actions-GL-MT2500
📌GL-MT2500自用固件定制

![GL-MT2500](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET.yml/badge.svg)

固件版本OpenWrt 21.02

内核版本5.4.211

# 编译包
- 因为固件自带adguardhome的原因就不额外编译了   [**(路由器地址)**](http://192.168.8.1/#/adguardhome)
- luci-theme-argon主题
- openclash **(旁路由成功)**
- helloworld **(旁路由最好用,接口控制不绑定)**
- aliyundrive-webdav
- luci-app-alist **（GL-MT2500是21.02，需要改golang版本，目前挂载有问题）**
- istore **(自选)**
- luci-app-broadbandacc
- luci-app-serverchan
- 以下插件测试中
- netspeedtest
- passwall **(旁路由没成功,有问题)**
- ~~luci-lib-dockerman~~
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