# <div align="center">MiniValine FAQs</div>

# Common

## Can't load QQ avatar?

无法加载QQ头像？

在3.x版本的minivaline可以用，但是api会暴露访客邮箱，这是不安全的。

我仍然想用？可以使用3.x版本，任何隐私泄露行为我们无法保证，或者可以尝试在4.x修改添加，但是我们不赞成这样做。

我们尝试以一种更安全的方法加载QQ头像，在以后的某个版本可能以访客头像可选的形式出现，如可以是QQ头像、wordpress头像或者自定义相册头像。

你可以加入我们，或者fork这个仓库并提交。

敬请期待！



## How to get appid and appkey?

Here  <https://minivaline.js.org/docs/en/#/Options?id=get-app-idapp-key>



## It not work?

+ Does some [options](https://minivaline.js.org/docs/en/#/Options), which important or necessary , is `null` in config.
+ The `el` options can't add in some plugins, eg [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline),[docsify-minivaline](https://github.com/MiniValine/docsify-minivaline)



## Add my own Emoji?

+ [Option.emoticonUrl](https://minivaline.js.org/docs/en/#/Options?id=base-options)
+ [how-to-customize-emoticons](https://minivaline.js.org/docs/en/#/Options?id=how-to-customize-emoticons)



## Sponsor？

There are no immediate plans to accept donations,maybe.



## How to join the development of MiniValine?

We welcome you to join the development of MiniValine. Please see [contributing document](https://minivaline.js.org/docs/en/#/Pre-Contribute). 🤗

Also, we welcome Issue or PR to MiniValine.



## How to Add or Improve translation?

-  Go to https://crowdin.com/project/minivaline

-  Create a new account.

-  Submit your request or Get in contact with us.

`
If you do not see your language listed, contact us and we will publish it.
`



# Advance

## How to improve the security of MiniValine?

### Version 5.x

**从5.x版本起MiniValine支持适配对[waline](https://github.com/lizheming/waline)后端数据交互.**

**[WHY](https://github.com/lizheming/waline/blob/master/docs/why.md)**

### Version 4.x

MiniValine version 4.x makes incompatible modification on the basis of MiniValine version 3.x to improve the security of MiniValine.

Since the QQ avatar API exposes the user's mailbox, the function of QQ avatar is deleted in MiniValine version 4.x.

Thanks to the idea of [imaegoo](https://github.com/imaegoo), [it](https://github.com/imaegoo/Valine) enhances the protection of users' privacy.

MiniValine version 4.x adds a visible field (mailmd5) to store mail MD5.

Here I offer an idea:

**Try to use cloudflare workers edge computing to improve the security of MiniValine.**

Since **appid** and **appkey** are required to call the database API:

![](https://cdn.jsdelivr.net/gh/MHuiG/imgbed/data/2020831194318.png)

However, it is a security risk to write them directly on the front-end page. Therefore, the author directly writes the database API key in cloudflare worker.

Insert a Fake API key into the front page to confusion.  The figure below shows that it is a Fake Key. 

![](https://cdn.jsdelivr.net/gh/MHuiG/imgbed/data/2020831194331.png)

We intercept user requests at the edge of the network and judge the validity of the requests. Edge computing is used to dynamically change the request header and replace it with the real API key to forward the request to the back-end database to hide the API key during data interaction.

Specific implementation can refer to [related documents](https://developers.cloudflare.com/workers/runtime-apis/request)

You can implement your own security policy by running JavaScript at the edge with [Cloudflare Workers](https://workers.cloudflare.com).

**使用 Cloudflare Workers 隐藏LC-Key和LC-Id**: [CF-LC](https://github.com/MiniValine/MiniValine/tree/master/CF-LC)

