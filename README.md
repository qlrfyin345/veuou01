[![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/qlrfyin345/veuou01.git)

## Workers 反向代理
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
## 注意

 1. **请勿滥用本专案，类似 Heroku 的免费服务少之又少，且用且珍惜**
