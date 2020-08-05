---
title: 'node请求代理'
excerpt: '记录了老家翻新装修过程的点点滴滴：构思，沟通，实现。一开始按时间线记录，后续说不定会整理成专题的形式'
date: '2020-07-30'
---

我现在的博客的静态内容是挂载在github仓库下，每次加载博文时都会向[https://raw.githubusercontent.com](https://raw.githubusercontent.com)发送请求。但因为国内网络原因，这个必须通过代理服务去请求才能保持稳定。看上去很简单的一个需求。没想到坑也挺多的。换了几个方案，最后还是选择了使用[`node-fetch`](https://github.com/node-fetch/node-fetch)来发送请求，同时配合[`proxy-agent`](https://github.com/TooTallNate/node-proxy-agent)来生成代理配置。有两点考虑：

- 库足够精简，符合Do one thing, and do it well的原则
- 都只是对标准的实现，并没有黑魔法： `PROXY-AGENT`用的[HTTP.aGENT](HTTPS://NODEJS.ORG/API/HTTP.HTML#HTTP_CLASS_HTTP_AGENT)，`NODE-FETCH`用的[fETCH](HTTPS://DEVELOPER.MOZILLA.ORG/EN-us/DOCS/wEB/api/fETCH_api)

但其实我一开始并不是用的这个方案，而是选择了`request`
https://github.com/request/request/issues/3142
https://github.com/request/request#proxies



axios https的请求必须使用https的代理
https://github.com/axios/axios/issues/658

npm的代理设置并不影响nodejs，nodejs使用的系统变量http_proxy
https://gist.github.com/alienlebarge/10260853

为什么fetch返回的是stream而不是string?


https://github.com/node-fetch/node-fetch#options
https://github.com/TooTallNate/node-proxy-agent