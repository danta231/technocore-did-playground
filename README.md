# Technocore DID 交互式演示

这是一个面向 Technocore / `$FLOP` 中文社区的教学页面。它会在浏览器本地生成 Ed25519 密钥，并把 `did:key` 的推导过程逐字节展示出来；页面也包含真实的消息签名、验签和可复制的 JavaScript 实现。

## 使用方式

- 直接双击 `index.html`，用现代浏览器打开。
- 或将整个 `did-demo` 目录放到任意静态托管服务（如 GitHub Pages、Cloudflare Pages、Netlify、Vercel 静态站点或普通 Nginx）中。
- 也可以在本目录运行 `python3 -m http.server 8000`，然后访问 `http://localhost:8000`。

页面是单个自包含 HTML 文件：CSS 与 JavaScript 均已内联，不依赖 CDN、第三方包或构建步骤。建议使用最新版 Chrome、Edge、Firefox，或 Safari 17+；浏览器必须支持 Web Crypto Ed25519。

所有密钥生成、DID 推导、签名与验证都只在浏览器内存中完成。页面不发出网络请求，不上传数据，也不会保存或导出私钥；刷新后本次生成的身份即消失。
