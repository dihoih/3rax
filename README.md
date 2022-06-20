### H.eroku部署V.2ray，  v.less协议类型

### 提醒：刚部署请勿大流量使用，否则容易被封！

[![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/dihoih/3rax.git)  点击紫色按钮开始部署
<p>下面是反代代码:</p>

```js
addEventListener(
    "fetch",event => {
        let url=new URL(event.request.url);
        url.hostname="appname.herokuapp.com";
        let request=new Request(url,event.request);
        event. respondWith(
            fetch(request)
        )
    }
)
```
