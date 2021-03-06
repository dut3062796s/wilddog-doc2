title: 验证码短信
---

本篇文档介绍如何发送验证码短信。


## 创建应用
首先，你需要在控制面板中创建应用。请参考 [控制面板-创建应用](/console/creat.html)。


## 账户充值
为防止滥用，短信服务需帐户余额大于 5 元才能使用。

如余额不足，请进入 [控制面板-财务-充值](https://www.wilddog.com/pay/recharge) 进行充值：

![](/images/recharge.png)

<blockquote class="notice">
  <p><strong>提示：</strong></p>
  每个帐号免费赠送 10 条短信(包括通知类和验证码短信)，在 控制面板-短信-资源统计 中领取，可将 10 条免费短信一次性分配给当前应用。
</blockquote>

 
## 配置短信

验证码短信由两部分构成: 签名、模版。

### 配置签名

签名出现在你下发短信的开头，可以是你的公司简称，品牌名，或网站名。通过控制面板-短信-签名 配置短信签名，操作如下：

![](/images/sign.png)

<blockquote class="notice">
  <p><strong>提示：</strong></p>
  <li>短信签名默认为【野狗试用】。</li>
  <li>签名提交后需审核，在审核期间可以使用旧的签名发送短信。</li>
  <li>每一个应用只能创建一个短信签名。</li>
  <li>更改签名需要在 控制面板-短信-签名 页面中提交相关资质。</li>
</blockquote>


### 选择模版

目前验证码短信暂不提供模版配置，只可使用野狗默认模版。默认模版分为 `验证手机号码` 和 `重置密码` 。模板由固定内容和一个验证码组成，验证码由野狗生成，无需自己制定验证码生成规则。使用过程如下：

![](/images/vertiprocess.jpg)


<blockquote class="notice">
  <p><strong>提示：</strong></p>
  <li>验证码模版需要调用短信模板 id。</li>
  <li>验证码有效时间默认为10分钟。</li>
</blockquote>


#### 验证码模版及使用场景

![](/images/smsmode.png)

- 注册时发送验证码短信
- 登录时发送验证码短信
- 找回/修改密码时发送验证码短信
- 绑定银行/实名认证时发送验证码短信等。


## 调用接口

- 需生成 [数字签名](/guide/sms/signature.html#生成数字签名的方法) 及调用接口，请参考 [接口文档](/api/sms/sendcode.html)。
- 如需校验验证码和查询短信发送状态，请参考 [校验验证码](/api/sms/checkcode.html) 、[查询模板短信发送状态](/api/sms/sendcode.html)。