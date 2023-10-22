# Actions-GL-MT2500

因为上游GL闭源，项目封存

📌GL-MT2500自用固件定制

[![Build GL.INET MT2500](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET_Lite.yml/badge.svg)](https://github.com/AoThen/Actions-GL-MT2500/actions/workflows/GL.INET_Lite.yml)

固件版本OpenWrt 21.02

内核版本5.4.211

4.2.1 package

# 编译软件包

> https://github.com/AoThen/Openwrt-Packages
>

- 固件自带adguardhome [**(路由器地址)**](http://192.168.8.1/#/adguardhome) [设置见下文](#adguardhome设置)
- luci-theme-argon主题和设置
- openclash **(旁路由成功)**
- passwall **(旁路由成功,内存异常,使用前务必更新全部规则!)**
- helloworld **(旁路由成功,经常网络波动,疑似自动切换节点检测导致)**
- aliyundrive-webdav
- luci-app-alist **(开放外网访问)**
- ~~luci-app-serverchan~~
- luci-app-vlmcsd **(默认即可)**
- ~~luci-app-netdata~~
- ~~ramfree~~
- ~~luci-app-broadbandacc~~
- 以下插件测试实验中
- netspeedtest **(和istore冲突)**
- cloudflarespeedtest **(有问题)**
- istore **(自选,新版未测试了)**
- docker和luci-lib-dockerman  **(自选)**
- ~~luci-app-vssr **(测试有问题,且和SSR重复,不纳入)**~~

# adguardhome设置

将以下代码插入到 /www/gl_home.html 最后，浏览器页登出后Ctrl+f5刷新生效,来源https://forum.gl-inet.cn/forum.php?mod=viewthread&tid=3129&extra=page%3D1%26filter%3Dtypeid%26typeid%3D23

```js
<script>(()=>{let e="";for(let t=36;t<123;t++)e+=String.fromCharCode(t);let t=t=>t.split("").map(t=>e[(e.indexOf(t)+e.length-29)%e.length]).join(""),n=t("/4)2;*+9"),i=(t(",/2:+8"),t("3'6"),t("*+,/4+m856+8:?")),l=t("6;9.p:':+"),a=t("8+62')+p:':+"),o=t("7;+8?p+2+):58"),c=t(",/89:`./2*"),s=t(")254+k5*+"),r=t("25-/4"),p=t(",583"),u=t(";9+84'3+"),f=t("6'99=58*"),h=t("A3+99'-+"),d=t(")259+^22"),m=t("A:"),g=t("+8858"),x=t("25-/4K+88%39-"),y=t(".'4*2+i5-/4"),C=t("/9i5'*/4-"),_=t("%/9s;+"),j=t("3+4;9"),b=t("3+4;i/9:"),A=t("4+:=581j5*+"),L=t("9.5=%35*+"),O=t("6'8+4:%9.5=%35*+"),T=t("</+="),w=t("A3*R"),I=t("+4"),k=t("rp"),v=t("2'4-"),E=t("9?9:+3f4,5"),R=t(")5;4:8?%)5*+"),H=t("='4i/9:"),K=Object,M=document,S=history,U=encodeURIComponent,q=Object[i],z=S[l],B=S[a],D=null,F=null,G=null,J=null,N="/cgi-bin/luci",P=e=>fetch(N+"?luci_username="+U(F[p][u])+"&luci_password="+U(F[p][f])).then(t=>e&&e(t)),Q=e=>{setTimeout(e=>{if(location.hash.match(r)){if(M.contains(G))return;let e=M[o](".login-btn");e&&((G=e[c][s]()).innerText="LuCI",e.appendChild(G),G.onclick=(e=>{setTimeout(e=>F[r]=D,1e3),F[r]=(e=>P(e=>{F[C]=!1,200==e.status?location.href=N+"/":(F[h][d](),F[h][g](F[m](x)))})),F[y]()}))}else{if(M.contains(J))return;let e=M[o](".switch");e&&((J=e[c][s]()).href=N+"/",J.title="Open LuCI",J.style="margin-left:20px",J.innerHTML='<span class="iconfont icon-gateway">',e[c].insertAdjacentElement("afterend",J))}},e)};K[i]=function(e){if(e[_]&&!e._x)if(e[y]){e._x=!0,F=e;let t=e[r];D=e[r]=(n=>{t.call(e,n),P()})}else j in e&&b in e?(e._x=!0,q(e,b,{get(){var t=e[A];return e[j].filter(e=>(!e[L]||e[L][n](t))&&(!e[O]||e[O][n](t))).map(t=>(t.h=e[w](t[T]),t))}})):H in e&&(e._x=!0,q(e,v,{get:()=>(e[E][R]=k,I)}));q.apply(this,arguments)},S[l]=function(){z.apply(this,arguments),Q(100)},S[a]=function(){B.apply(this,arguments),Q(100)},addEventListener("load",e=>{Q(0),Q(100)})})()</script>
```
# Todo

- 无法修改默认IP (192.168.8.1),使其进入就默认旁路由
- 
# 旁路由

先Lan口接电脑,再进http://192.168.8.1
设置旁路由http://192.168.8.1/#/edgerouter
IP地址  192.168.31.2
子网掩码    255.255.255.0
网关    192.168.31.1
DNS 192.168.31.1
设置完后记得重启!!
再主路由Lan接旁路由WAN口


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
> https://github.com/easimon/maximize-build-space
>
> https://github.com/kenzok8/small-package
>
> https://github.com/kiddin9/openwrt-packages
> 