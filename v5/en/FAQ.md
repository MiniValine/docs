# <div align="center">MiniValine FAQs</div>

# Common

## Can't load QQ avatar?

Since the QQ avatar API exposes the user's mailbox, the function of QQ avatar is deleted in MiniValine version 4.x.

There is a plan to add QQ avatar in safe way, or use wordpress avatar or use Photo album for visiter.

You can join us for fork this to develop it.

Stay tuned.



## How to get appid and appkey?

Here  <https://minivaline.js.org/docs/v5/en/#/Options?id=get-app-idapp-key>



## It not work?

+ Does some [options](https://minivaline.js.org/docs/v5/en/#/Options), which important or necessary , is `null` in config.
+ The `el` options can't add in some plugins, eg [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline),[docsify-minivaline](https://github.com/MiniValine/docsify-minivaline)



## Add my own Emoji?

+ [Option.emoticonUrl](https://minivaline.js.org/docs/v5/en/#/Options?id=base-options)
+ [how-to-customize-emoticons](https://minivaline.js.org/docs/v5/en/#/Options?id=how-to-customize-emoticons)

## How to join the development of MiniValine?

We welcome you to join the development of MiniValine. Please see [contributing document](https://minivaline.js.org/docs/v5/en/#/Pre-Contribute). 🤗

Also, we welcome Issue or PR to MiniValine.



## How to Add or Improve translation?

-  Go to https://crowdin.com/project/minivaline

-  Create a new account.

-  Submit your request or Get in contact with us.

`
If you do not see your language listed, contact us and we will publish it.
`





## Sponsor？

There are no immediate plans to accept donations,maybe.





# Advance

## How to improve the security of MiniValine?

### Version 5.x

**From version 5. X, MiniValine supports pairing [waline](https://github.com/lizheming/waline) Back end data interaction**

**[WHY](https://github.com/lizheming/waline/blob/master/docs/why.md)**

!> Note that the following are optional mode combinations. By default, both the minivaline and leancloud combinations are supported. The minivaline front-end and waline back-end must both support options to work. If one is not supported, an unknown error may occur.

<iframe src="./assets/mode.en.html" width="200" height="600"></iframe>

!> The minivaline front-end is directly connected to the leancloud combination, which has high-risk security vulnerabilities. This combination is only used as a test post for developers, and is not recommended for online deployment. It is recommended to use the combination with server-side middle layer.


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

**Hiding LC key and LC ID with cloudflare workers**: [CF-LC](https://github.com/MiniValine/MiniValine/tree/master/CF-LC)