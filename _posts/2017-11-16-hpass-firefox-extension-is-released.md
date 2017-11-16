---
layout: post
title: hPass Firefox extension is released
---

[Install ➡️](https://addons.mozilla.org/zh-CN/firefox/addon/hpass/)

**hPass** is HMAC-based **password derivation tool**.

You can derivate a unique per-site password from a master password and the site domain.

The algorithm is 

```
PASSWORD = HTML_SAFE_BASE64( HMAC256( KEY, DOMAIN ) ).SUBSTRING(0, 16)
```

It's `WebExtensions` compatible, so you can use it for Chrome as well.

## Warnnings⚠️

Remember, this **IS** a password derivation tool, this **IS NOT** a key derivation tool.

You **CAN** used the derivated password for your online account, because nearly all websites protect your account from brutal-force attacks.

You **SHALL NEVER** use the derivated password as a encryption key, because it IS **NOT** strong enough.

## Source Code

[View on Github ➡️](https://github.com/yuki93/hpass), MIT Licensed
