# IOS14的微信小程序上传Bug准备的demo
对应问题：
[ios14小程序内嵌h5，上传文件会导致路由方法无法使用](https://developers.weixin.qq.com/community/develop/doc/000ecaf75702a85b8d1b5b7fe51000?fromCreate=0)

# 本地运行
```js
npm install
npm run dev
```
启动完以后，在小程序代码片段的pageA页面，把webview的src改为该服务的地址即可，比如我本地的是`http://10.242.217.245:8082/`

用IOS14的手机扫码预览小程序，打开调试模式；

第一步，进入Home页；

第二步，点击进入PageA页；

第三步，点击PageA页面的上传按钮，然后出现系统自带的上传选择浮层，不进行选择，点击其它区域让其消失；

第四步，返回上一页，也就是Home页，然后神奇的事情发生了，Home不管怎么点击PageA、PageB或PageC都无法跳转过去。调试模式的console也没有任何报错信息。

