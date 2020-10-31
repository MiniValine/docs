# <div align="center">MiniValine FAQs</div>

# Common

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

[@MiniValine/CF-LC](https://github.com/MiniValine/CF-LC)



### Try to be faster.

The author uses a `Python` script to generate `index.json` here. The friends who have the ability can try it.

Modify `FilePath` please.

``` python
#-*- coding: utf-8 -*-
import os

def walkFile(FilePath):
    S='''{"0":['''
    for root, dirs, files in os.walk(FilePath):
        for f in files:
            Path=os.path.join(root, f)
            S+="'"+f+"',"
    S+="]}"
    print("正在写入文件，这通常不会太久...")
    with open("./index.json","wb") as ff:
        ff.write(S.encode("utf-8"))
    print("恭喜，已成功完成")
if __name__=="__main__":
    print("请坐和放宽，我们正帮你搞定一切......")
    FilePath="./alus"
    try:
        walkFile(FilePath)
    except Exception as e:
        print("生成失败！我们都有不顺利的时候.")
        print(e)

```