# PicACG Web App

<div align="center">

Deploy With Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FHanze-C%2FPicaComicNow&demo-title=PicACG%20Web%20App&demo-url=https%3A%2F%2Fpica-comic-now-zh.vercel.app)

本项目支持Vercel一键部署
部署前请根据以下文档更换部分链接

</div>

## CloudFlare Worker 反向代理

如果您的网络环境无法连接至PicACG官方网站，请根据以下步骤部署反代

1.将Worker部署到CLoudflare

*由于worker.dev被DNS污染，请为Worker绑定自己的域名

  <p>
    <a href="https://deploy.workers.cloudflare.com/?url=https://github.com/Hanze-C/Proxy-CF">
      <img src="https://deploy.workers.cloudflare.com/button" alt="Deploy to Cloudflare Workers"/>
    </a>
  </p>

2. Fork本仓库后更改api/utils

api/utils.ts (Line 38-47)
---
    // String
    if (typeof val === 'string') {
      if (val.startsWith('https://')) {
        obj[key] = val
          .replace('storage1.picacomic.com', 'proxy.your-domain.com/proxy/s3.picacomic.com')
          .replace('storage-b.picacomic.com', 'proxy.your-domain.com/proxy/s3.picacomic.com')
          .replace('img.picacomic.com', 'proxy.your-domain.com/proxy/s3.picacomic.com')
          .replace('www.picacomic.com', 'pica-pica.wikawika.xyz')
      }
    }
---
将proxy.your-domain.com替换为你的域名

## Attention please

This is a fan made website. We are NOT PicACG official. Please DO NOT share this website anywhere.

这是一个粉丝向网站，我们与 PicACG 官方没有任何关系。请勿在任何地方传播本网站。

---

_For communication and learning only._

**All data & pictures from query:** &copy;PICA & Illusts' authors

> Copyright 2021 FreeNowOrg
>
> Licensed under the Apache License, Version 2.0 (the "License");<br>
> you may not use this file except in compliance with the License.<br>
> You may obtain a copy of the License at
>
> http://www.apache.org/licenses/LICENSE-2.0
>
> Unless required by applicable law or agreed to in writing, software<br>
> distributed under the License is distributed on an "AS IS" BASIS,<br>
> WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.<br>
> See the License for the specific language governing permissions and<br>
> limitations under the License.

