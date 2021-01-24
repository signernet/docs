# 微信登录

## 根据 jsCode 获取用户 session 信息
登录凭证校验。小程序通过 wx.login 接口获得临时登录凭证 code 后传到开发者服务器调用此方法获取当前的登录用户的openid 与 session_key，并完成登录。


API:

```php
$app->auth->session(string $code);
```

#### Response:
- 成功：['session_key'=>'xxxx', 'openid'=> 'xxxxx']
- 失败(例)：['errcode'=> 40029, errmsg: 'invalid code, hints: [ req_id: kfLaZ44ce-m3ygeA ]']
- 说明：errorcode 参考 <a href="https://developers.weixin.qq.com/miniprogram/dev/api-backend/open-api/login/auth.code2Session.html">微信小程序文档</a>
  
