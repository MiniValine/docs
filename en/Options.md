# Options

!> When you change version, care about [CHANGELOG](https://minivaline.js.org/docs/en/#/CHANGELOG) before.



## Mode

!> Note that the following are optional mode combinations. By default, both the minivaline and leancloud combinations are supported. The minivaline front-end and waline back-end must both support options to work. If one is not supported, an unknown error may occur.

<iframe src="./assets/mode.en.html" width="200" height="600"></iframe>



## Mount Options

!> Some plugins,which has been installed before, may not be required,  **DO NOT** ADD Mount Options, eg  [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) 

| Option       | type     | Required or Default          | Minivaline version<br />front-end | Waline    version<br />[back-end](https://www.npmjs.com/package/@waline/vercel) |
| ------------ | -------- | ---------------------------- | --------------------------------- | ------------------------------------------------------------ |
| **el**       | `String` | **Required**.                | `1.x~latest`                      | `0.8.6~latest`                                               |
| **pathname** | `String` | Default: `location.pathname` | `1.x~latest`                      | `0.8.6~latest`                                               |

### **el** `String`

+ **Required**. [object HTMLDivElement]

+ > You can find example at [**Install**](https://minivaline.js.org/docs/en/#/Install)

### **pathname** `String`

+ Default: `location.pathname`

+ The pathname of the page.

+ > You can find example at [**Install**](https://minivaline.js.org/docs/en/#/Install)
  >
  > Note that sometimes quotation marks are not needed as a variable.[detail](https://github.com/MiniValine/MiniValine/issues/250)



## Base Options

| Option          | type           | Default                         | description                                                  | minivaline version<br />front-end | Waline   version<br />[back-end](https://www.npmjs.com/package/@waline/vercel) |
| --------------- | -------------- | ------------------------------- | ------------------------------------------------------------ | --------------------------------- | ------------------------------------------------------------ |
| **appId**       | `String`       | `null`                          | **Leancloud back-end Required**.<br />Your App ID, detail from [Advance](https://minivaline.js.org/docs/en/#/Options?id=get-app-idapp-key) | `1.x~latest`                      | :x:                                                          |
| **appKey**      | `String`       | null                            | **Leancloud back-end Required**.<br /><br />Your App Key,detail from [Advance](https://minivaline.js.org/docs/en/#/Options?id=get-app-idapp-key) | `1.x~latest`                      | :x:                                                          |
| **mode**        | `String`       | `DesertsP`                      | choose Style mode, The details are Under the table           | `2.x~latest`                      | `0.8.6~latest`                                               |
| **placeholder** | `String`       | `null`                          | Input Placeholder                                            | `1.x~latest`                      | `0.8.6~latest`                                               |
| **math**        | `Boolean`      | `true`                          | Support MathJax, details below.                              | `1.x~latest`                      | `0.8.6~latest`                                               |
| **md**          | `Boolean`      | `true`                          | Support Markdown.                                            | `1.x~latest`                      | :x:                                                          |
| **dark**        | `Boolean`      | `false`                         | [Dark model.](https://minivaline.js.org/docs/en/#/Options?id=how-to-add-dark-mode) | `3.x~latest`                      | `0.8.6~latest`                                               |
| **lang**        | `String`       | navigator userLanguage          | support i18n,details below.                                  | `1.x~latest`                      | `0.8.6~latest`                                               |
| **emoticonUrl** | `String Array` | built-in emoticon               | yourself emoticonUrl, details below.                         | `1.x~latest`                      | `0.8.6~latest`                                               |
| **NoRecordIP**  | `Boolean`      | `false`                         | Do not record commenter IP.                                  | `1.x~latest`                      | :x:                                                          |
| **maxNest**     | `Number`       | `6`                             | Sub-comment maximum nesting depth.                           | `1.x~latest`                      | `0.8.6~latest`                                               |
| **pageSize**    | `Number`       | `6`                             | Pagination size.                                             | `1.x~latest`                      | `0.8.6~latest`                                               |
| **visitor**     | `Boolean`      | `true`                          | Only **article reading access statistics**and <br />**whole site access statistics** are provided. | `2.x~latest`                      | `0.8.6~latest`                                               |
| **serverURLs**  | `String`       | Leancloud International Edition | choose backend URL, details below.                           | `1.x~latest`                      | `0.8.6~latest`                                               |
| **barrager**    | `Number`       | `true`                          | Load or close Comment, details below.                        | `3.x~latest`                      | `0.8.6~latest`                                               |
| **role**        | `String`       | `admin`                         | administrator role, details below.                           | `3.x~latest`                      | :x:                                                          |
| **closeCSS**    | `Boolean`      | `false`                         | Turn off loading CSS.                                        | `4.x~latest`                      | `0.8.6~latest`                                               |
| **enableQQ**    | `Boolean`      | `false`                         | **Deleted**  The details are Under the table                 | `2.x~3.x`                         | :x:                                                          |
| **backend**     | `String`       | `lc`                            | If not leancloud need choose backend , details below.        | `5.x~latest`                      | `0.8.6~latest`                                               |




### **mode** `String`

- Default: `DesertsP`
- Options: 

  - `DesertsP` DesertsP Style mode. [demo](https://minivaline.js.org/DesertsP.html)
  - `xCss`  xCss Style mode. [demo](https://minivaline.js.org/xCss.html)

### **Math** `Boolean`: 

+ `false` Close MathJax.

+ `true`  Support MathJax@3 initialization.

+ > The above is the initialization operation of integrating MathJax in MiniValine.
  > If MathJax is loaded on the page, MiniValine will use the MathJax version on the page.

### **lang** `String`:

- Default: `navigator.language || navigator.userLanguage`.

- Localization language key, en and zh-CN are currently available.
  - More i18n info: 
  - [How to Add or Improve translation?](https://minivaline.js.org/docs/en/#/Contribute?id=how-to-add-or-improve-translation)
  

### **emoticonUrl** `String Array`

- Default:`['https://cdn.jsdelivr.net/npm/alus@latest']`

- PAY ATTENTION

  - json style 

    - ```yaml
      {
      	"emoticonUrl": [
      		"https://cdn.jsdelivr.net/npm/alus@latest",
      		"https://cdn.jsdelivr.net/gh/MiniValine/qq@latest",
      		"https://cdn.jsdelivr.net/gh/MiniValine/Bilibilis@latest",
      		"https://cdn.jsdelivr.net/gh/MiniValine/tieba@latest",
      		"https://cdn.jsdelivr.net/gh/MiniValine/twemoji@latest",
      		"https://cdn.jsdelivr.net/gh/MiniValine/weibo@latest"
      	]
      }
      ```

  - yaml style

    - ```yml
        emoticonUrl:
          - https://cdn.jsdelivr.net/npm/alus@latest
          - https://cdn.jsdelivr.net/gh/MiniValine/qq@latest
          - https://cdn.jsdelivr.net/gh/MiniValine/Bilibilis@latest
          - https://cdn.jsdelivr.net/gh/MiniValine/tieba@latest
          - https://cdn.jsdelivr.net/gh/MiniValine/twemoji@latest
          - https://cdn.jsdelivr.net/gh/MiniValine/weibo@latest
      ```

- Personality Expression Url.

  - [How to customize emoticons?](https://minivaline.js.org/docs/en/#/Options?id=how-to-customize-emoticons)


### **serverURLs** `String`

+ Default: `http[s]://[tab/us].avoscloud.com`
  
+ Options：
  
  + default
    
    + > The overseas version will be automatically detected (**no need** to fill in manually).
    
  + Your URL (domestic custom domain name users)
  
    + >  This configuration is suitable for domestic custom domain name users.
  
  + Cloudflare Middleware
  
    + [Try to use cloudflare workers edge computing to improve the security](https://minivaline.js.org/docs/en/#/FAQ?id=how-to-improve-the-security-of-minivaline)
  
  + Your back-end url
  
    + [how-to-add-backend](https://minivaline.js.org/docs/en/#/Options?id=how-to-add-backend-)
  
      + > Now only support waline.

### **barrager** `Number`

+ Default: `1`

+ Options: 
  + `0`  Close Comment barrager.
  + `1`  Load a round of Comment barrager.
  + `2`  Load all round of Comment barrager.
+ Comment barrager. [Load only when the page is ***first*** loaded]

### **role** `String`

+ Default: `admin`

+ Write permissions for the administrator role. 

+ [Valine-Android](https://github.com/yinhanlei/Valine-Android)  [Valine-iOS](https://github.com/xaoxuu/Valine-iOS) 

### **enableQQ** `Boolean`

**deleted!!!**

+ Default: `false`

+ Enable QQ avatar API.

+ > Since the QQ avatar API exposes the user's mailbox, the function of QQ avatar is **deleted** in MiniValine version 4.x.

### **backend** `String`

+ Default: `lc`

+ Options: 

  + `lc`  Leancloud no back end application mode.
  + `waline`  Use [waline](https://github.com/lizheming/waline) As the back-end program

+ >  **serverURLs ** needs to be changed to the server address of waline. Refer to [demo configuration](https://github.com/MiniValine/MiniValine.github.io/blob/master/waline.html#L46).
  >
  > For the backend configuration of waline, please refer to : https://github.com/lizheming/waline




## Style Options

### DesertsP Style mode Options

| Option            | type     | Default | description                                | minivaline version | Waline    valine |
| ----------------- | -------- | ------- | ------------------------------------------ | ------------------ | ---------------- |
| **adminEmailMd5** | `String` | `null`  | The MD5 of Admin Email to show Admin Flag. | `1.x~latest`       | `0.8.6~latest`   |





### xCss Style mode Options



| Option        | type           | Default | description                                                  | minivaline version | Waline    version |
| ------------- | -------------- | ------- | ------------------------------------------------------------ | ------------------ | ----------------- |
|               |                |         | visitor flag bellow                                          |                    |                   |
| **closeFlag** | `Boolean`      | `false` | Turn off visitor flag.                                       | `3.x~latest`       | `0.8.6~latest`    |
|               |                |         | Visitor Flag **Local** Options bellow                        |                    |                   |
| **master**    | `String Array` | `[]`    | The MD5 String Array of master Email to show master Flag.    | `2.x~latest`       | `0.8.6~latest`    |
| **friends**   | `String Array` | `[]`    | The MD5 String Array of friends Email to show friends Flag.  | `2.x~latest`       | `0.8.6~latest`    |
| **tagMeta**   | `String Array` | `[]`    | The String Array of Words to show Flag (only three).<br />For Example: `tagMeta: ["Master", "Friend", "Visitor"]` | `2.x~latest`       | `0.8.6~latest`    |
|               |                |         | Visitor Flag **Cloud** Option bellow                         |                    |                   |
| **cloudflag** | `Boolean`      | `false` | The details are Under the table                              | `3.x~latest`       | :x:               |
|               |                |         | xCss Style mode **Others Options** bellow                    |                    |                   |
| **region**    | `Boolean`      | `false` | The details are Under the table                              | `3.x~latest`       | :x:               |
| **closeUA**   | `Boolean`      | `false` | Turn off UA detection.                                       | `3.x~latest`       | `0.8.6~latest`    |



#### **cloudflag** `Boolean`

+ Default: `false`

+ If `cloudflag` is turned on, the setting of `Visitor Flag Local Options` is invalid.

+ How to Set Visitor Flag Cloud Option For xCss Style mode? [**Advance below** please](https://minivaline.js.org/docs/en/#/Options?id=how-to-set-visitor-flag-cloud-option-for-xcss-style-mode)

#### **region** `Boolean`

+ Default: `false`

+ According to IP output area.

+ Note: Currently only Chinese API is available and NoRecordIP: `false`.





## Advance

### Get `App ID`/`App Key`

#### Get `App ID`/`App Key` from LeanCloud

+ [Click here](https://console.leancloud.app/login.html#/signup) to register or login in `LeanCloud`. 
+ [Click here](https://console.leancloud.app/applist.html#/newapp) Create new application in `LeanCloud`, and you will get `appId`/`appKey`.

![image.png](https://upimage.alexhchu.com/2020/10/31/35aad44a146f8.png)

#### Add Security URL

![image.png](https://upimage.alexhchu.com/2020/10/31/d3a5e64db9e98.png)





### How to Set Visitor Flag Cloud Option For xCss Style mode?

cloudflag : true

If `cloudflag` is turned on, the setting of [Visitor Flag Local Options](https://github.com/MiniValine/MiniValine#visitor-flag-local-options) is invalid.

Create Class `Roles` and `Users`.

![](https://cdn.jsdelivr.net/gh/MiniValine/MiniValine@master/.github/img/v1.png)

Create column `name` , `nick` , `color` in `Roles`.

![](https://cdn.jsdelivr.net/gh/MiniValine/MiniValine@master/.github/img/v2.png)

Create column `emailhash` , `role` in `Users`.

![](https://cdn.jsdelivr.net/gh/MiniValine/MiniValine@master/.github/img/v3.png)

Notice the correspondence between `name` in `Roles` and `role` in `Users`.







### How to Add Dark Mode?

Assume that the trigger class of Dark Mode is `.darkmode`

Just add the following style：

```
.darkmode .commentTrigger{
	background-color: #403e3e !important;
  }
.darkmode .MiniValine .vpage .more{
	background: #21232F
}
.darkmode img{
      filter: brightness(30%)
}
.darkmode .MiniValine .vlist .vcard .vcomment-body .text-wrapper .vcomment.expand:before{
	background: linear-gradient(180deg, rgba(246,246,246,0), rgba(0,0,0,0.9))
}
.darkmode .MiniValine .vlist .vcard .vcomment-body .text-wrapper .vcomment.expand:after{
	background: rgba(0,0,0,0.9)
}
.darkmode .MiniValine .vlist .vcard .vcomment-body .text-wrapper .vcomment pre{
	background: #282c34
	border: 1px solid #282c34
}
.darkmode .MiniValine .vinputs-area .vextra-area .vsmile-icons{
	background: transparent;
}
```



### How to customize emoticons?

For example:

[alus](https://github.com/MiniValine/alus): MiniValine's default emoji.

 1.Create a GitHub repository named [alus](https://github.com/MiniValine/alus).

 2.Add custom emoji picture files in GitHub Repository.

 3.The most important is that you need to add [index.json](https://github.com/MiniValine/alus/blob/master/index.json) in the root directory.

[index.json](https://github.com/MiniValine/alus/blob/master/index.json) must obey such rules:

``` json
{"0":["A","B","C"]}
```

* Only Replace `A`,`B`,`C` with your emoji picture file name. Note the file extension.

* Please note that commas, colons, brackets, braces, quotes use English half-width.

* Please note that the file name of index.json must be `index.json`.

* For example:

``` json
{"0":["emoticonA.png","emoticonB.gif","emoticonC.jpeg","emoticonD.jpg"]}
```

 4.Get CDN link

jsdelivr CDN link : https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[GitHubRepositoryName]

Be careful not to have `/` at the end of the URL

For example:

```
https://cdn.jsdelivr.net/gh/MiniValine/alus
```

 5.Modify MiniValine configuration item `emoticonUrl`


```
  new MiniValine({
      el: '.comment',
      appId: 'Your App ID',
      appKey: 'Your Key',
      placeholder: 'Write a Comment',
      emoticonUrl: ['https://cdn.jsdelivr.net/gh/MiniValine/alus']
  });

```

or

```
  new MiniValine({
      el: '.comment',
      appId: 'Your App ID',
      appKey: 'Your Key',
      placeholder: 'Write a Comment',
      emoticonUrl: ['https://cdn.jsdelivr.net/gh/MiniValine/Bilibilis@master','https://cdn.jsdelivr.net/npm/alus']
  });

```


 6.Try to be faster.

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
            S+='"'+f+'",'
    S+="]}"
    S=S.replace(",]}", "]}")
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

### How to add backend ?

For the backend configuration of waline, please refer to : https://github.com/lizheming/waline

> PAY ATTENTION!
>
> Some Options not support for waline



