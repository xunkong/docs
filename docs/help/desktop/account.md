# 添加米游社账号

::: tip 提示
寻空的很多功能需要使用米游社的账号
:::

## 通过 Cookie 添加账号

- 把右侧的文字拖入浏览器书签栏 <a href="javascript:(()=>{if(location.host.includes('bbs.mihoyo.com')){var cookie=document.cookie;if(cookie.includes('cookie_token')&&cookie.includes('account_id')){navigator.clipboard.writeText(cookie);alert('Cookie 已复制到剪贴板')}else{alert('没有找到 cookie_token 和 account_id，请重新登录')}}else{alert('当前网页不为米游社页面')}})();">获取米游社 Cookie</a>
- 使用浏览器的**无痕模式**打开 [米游社·原神](https://bbs.mihoyo.com/ys/)页面
- 登录您需要添加到寻空中的账号
- 点击之前添加的书签，此时 Cookie 已被复制到剪贴板
- 在寻空中点击 **添加账号 > 输入 Cookie**，粘贴上述过程中复制的内容并点击确认

## 签到

0.1.7.0 版本开始，启动应用时会自动签到，签到失败有横幅提醒，若已签到则不会重复签到。

## 常见问题

### 支不支持国际服

不支持，寻空仅支持国服米游社。

### 如何添加多个账号

使用**无痕模式**打开**新的** [米游社·原神](https://bbs.mihoyo.com/ys/) 页面，重复上述步骤。

### 出现 HoyolabException (-100) 错误

有两种可能的原因：
- Cookie 中没有 `cookie_token` 和 `account_id`
- 该账号已退出登录

在任意端退出登录米游社账号均会导致当前 Cookie 失效，非必要不点击退出登录按键。

## 书签内容

``` js
javascript: (() => {
    if (location.host.includes('bbs.mihoyo.com')) {
        var cookie = document.cookie;
        if (cookie.includes('cookie_token') && cookie.includes('account_id')) {
            navigator.clipboard.writeText(cookie);
            alert('Cookie 已复制到剪贴板');
        } else {
            alert('没有找到 cookie_token 和 account_id，请重新登录');
        }
    } else {
        alert('当前网页不为米游社页面');
    }
})();
```
