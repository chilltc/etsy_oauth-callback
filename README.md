# etsy_oauth-callback

Etsy OAuth 授权回调页，给店主自用的本机店铺看板用。

- 静态网页，不保存、不上传任何东西。
- 只做一件事：把 Etsy 返回的授权码交回本机看板 `http://localhost:8770/oauth/redirect`。
- 单独拿到授权码没用：换令牌要用 PKCE 验证串，它只在店主电脑上。
- 页面的安全策略禁止加载外部文件、禁止向任何地址发请求，并且不发送 Referer。

源文件在 etsy_new 仓库的 `12_Etsy工作台/callback/`。改那里，再复制到这个仓库。
