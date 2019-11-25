援引自 ：https://t.me/unionofcute/14416 ；感谢写脚本的大佬；

### fork 本仓库
fork https://github.com/limbopro/helpless 仓库；不会 Fork ? 参考：[Github 入门- fork 他人仓库](https://limbopro.xyz/archives/3856.html#fork他人仓库)


### 修改 unblockremote.js

1.进入 `fork` 后的`仓库`，找到并修改 `unblockremote.js` 脚本文件；
2.填写你的`设备ID`；（`设备ID`在哪？进入QuantumltX，点击右下角三菱按钮，点击右上角 `...` 更多按钮，滑至底部`关于`，即可找到设备ID）；
3.修改后，点击`commit changes` 以保存此更改；



### 下载 unblockremote.js
0.如果会用WorkingCopy同步仓库到本地就更好，不会则按下面步骤操作；
1.复制并在浏览器中打开进行下载，`https://github.com/你的github用户名/helpless/archive/master.zip`；
2.拷贝/或保存`helpless-master.zip`至`我的iPhone`-`Quantumult X` - `Scripts` 文件夹下；
3.解压缩 `helpless-master.zip`；



### 配置 rewrite_local

编辑QuantumultX 配置文件 ，找到 [rewrite_local]，并在 [rewrite_local] 添加：

```
^https:\/\/(raw.githubusercontent|\w+\.github)\.(com|io)\/.*\.js$ url script-response-body helpless-master/unblockremote.js
```

添加后效果：

```
[rewrite_local]
^https:\/\/(raw.githubusercontent|\w+\.github)\.(com|io)\/.*\.js$ url script-response-body helpless-master/unblockremote.js
```



## 配置 hostname

编辑QuantumultX 配置文件 ，找到 `hostname =`，并在 `hostname =` 后面添加：`raw.githubusercontent.com, *.github.io,`

效果如下：

```
hostname = raw.githubusercontent.com, *.github.io, vsco.co, *.my10api.com, *googlevideo.com, api.termius.com, api*.tiktokv.com, api*.musical.ly, api*.amemv.com, aweme*.snssdk.com, api.weibo.cn, mapi.weibo.com, *.uve.weibo.com, mp.weixin.qq.com, api.bilibili.com, app.bilibili.com, *.zhihu.com, aweme*.snssdk.com, *.kuwo.cn, ios.xiaoxiaoapps.com, api*.tiktokv.com, *.musical.ly, *.amemv.com, mjappaz.yefu365.com, p.du.163.com, getuserinfo.321mh.com, getuserinfo-globalapi.zymk.cn, api-163.biliapi.net, ios.fuliapps.com, vsco.co, api.vnision.com, *.my10api.com, bd.4008109966.net, sp.kaola.com, r.inews.qq.com, apple.fuliapps.com, newdrugs.dxy.cn, bdapp.4008109966.net, app101.avictown.cc, api.hlo.xyz, api.ijo.xyz, www.luqijianggushi.com, account.wps.cn, u.kanghuayun.com, api.gyrosco.pe, api1.dobenge.cn, api.mvmtv.com, mitaoapp.yeduapp.com, origin-prod-phoenix.jibjab.com, www.3ivf.com, pay.guoing.com, p.doras.api.vcinema.cn, api.termius.com, mjappaz.yefu365.com, viva.v21xy.com, dida365.com, ticktick.com
```



### 引用远程JS.conf

1.复制`https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/Js.conf`链接，
2.进入Quantumult X，点击右下角`三菱按钮`，找到`Rewrite`模块-点击` 引用`，粘贴刚刚复制的链接；



### 完事

测试完毕，一切正常；VSCO/Termius/解锁顺滑，Tiktok 顺滑；
