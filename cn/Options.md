# Options

!> 切换版本之前，或者使用`@latest`版本的时候，在大更新之前，关注一下 [更新日志](https://minivaline.js.org/docs/en/#/CHANGELOG) 。

## Mode

!> 注意下面是可选的模式组合，默认是minivaline和leancloud组合都支持的，而minivaline前端和waline后端要都支持的选项才能起作用，有一个不支持的，可能会发生未知错误。

<iframe src="./assets/mode.cn.html" width="200" height="600"></iframe>

!> minivaline前端直接连接leancloud组合存在高危安全漏洞，该组合仅为开发者用作测试桩程序，不推荐用于线上部署。推荐使用具有服务端中间层的组合。


## Mount Options

!> 注意一些插件不需要添加Mount Options（挂载选项），直接看底下的基础选项和样式选项

> 一些插件可能事先写在实现逻辑里面了，不需要再添加这项，如果再添加可能导致错误, 
>
> 比如 [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) **不要**添加这个选项

| Option       | type     | Required or Default          | description                      | Minivaline<br />前端版本 | Waline    <br />后端版本 |
| ------------ | -------- | ---------------------------- | -------------------------------- | ------------------------ | ------------------------ |
| **el**       | `String` | **Required**.                | [object HTMLDivElement] 挂载在哪 | `1.x~latest`             | `0.8.6~latest`           |
| **pathname** | `String` | Default: `location.pathname` | 文章路径，详见表格底下备注       | `1.x~latest`             | `0.8.6~latest`           |

### **el** `String`

+ **Required**. [object HTMLDivElement]

+ > 即挂载在什么地方，可以在 [**Install**](https://minivaline.js.org/docs/cn/#/Install) 找到例子
  >

### **pathname** `String`

+ Default: `location.pathname`

+ The pathname of the page

+ > 即 文章路径 ，可以在 [**Install**](https://minivaline.js.org/docs/cn/#/Install) 找到例子
  >
  > 注意如果开发一个主题或插件，有些场景不用加引号，因为本身是变量，加了引号变成常字符串了。[detail](https://github.com/MiniValine/MiniValine/issues/250)



## Base Options

| Option          | type           | Default         | description                                                  | Minivaline<br />前端版本 | Waline    <br />后端版本 |
| --------------- | -------------- | --------------- | ------------------------------------------------------------ | ------------------------ | ------------------------ |
| **appId**       | `String`       | `null`          | 注意**leancloud后端**这个**必须要有的**，你的 App ID 详见 [Advance](https://minivaline.js.org/docs/cn/#/Options?id=get-app-idapp-key) | `1.x~latest`             | :x:                      |
| **appKey**      | `String`       | `null`          | 注意**leancloud后端**这个**必须要有的**，你的 App Key,详见 [Advance](https://minivaline.js.org/docs/cn/#/Options?id=get-app-idapp-key) | `1.x~latest`             | :x:                      |
| **mode**        | `String`       | `xCss`          | 样式模式                                                     | `2.x~latest`             | `0.8.6~latest`           |
| **placeholder** | `String`       | `null`          | 输入框占位符                                                 | `1.x~latest`             | `0.8.6~latest`           |
| **math**        | `Boolean`      | `false`         | 支持数学公式                                                 | `1.x~latest`             | :x:                      |
| **md**          | `Boolean`      | `false`         | 内置markdown                                                 | `1.x~latest`             | :x:                      |
| **dark**        | `Boolean`      | `false`         | 黑暗模式                                                     | `3.x~latest`             | `0.8.6~latest`           |
| **lang**        | `String`       | 用户目前语言    | 语言                                                         | `1.x~latest`             | `0.8.6~latest`           |
| **emoticonUrl** | `String Array` | 内置表情        | 自定义表情链接                                               | `1.x~latest`             | `0.8.6~latest`           |
| **NoRecordIP**  | `Boolean`      | `false`         | 不记录评论者IP                                               | `1.x~4.x`                | :x:                      |
| **RecordIP**    | `Boolean`      | `false`         | 记录评论者IP                                                 | `5.x~latest`             | :x:                      |
| **maxNest**     | `Number`       | `6`             | 评论引用最大深度                                             | `1.x~latest`             | `0.8.6~latest`           |
| **pageSize**    | `Number`       | `6`             | Pagination size.                                             | `1.x~latest`             | `0.8.6~latest`           |
| **visitor**     | `Boolean`      | `true`          | 仅提供“文章阅读访问统计”和“整个站点访问统计”。               | `2.x~latest`             | `0.8.6~latest`           |
| **serverURLs**  | `String`       | leancloud国际版 | 后端具体地址                                                 | `1.x~latest`             | `0.8.6~latest`           |
| **barrager**    | `Number`       | `0`             | 弹幕                                                         | `3.x~latest`             | `0.8.6~latest`           |
| **role**        | `String`       | `admin`         | 角色                                                         | `3.x~latest`             | :x:                      |
| **closeCSS**    | `Boolean`      | `false`         | 关闭CSS样式                                                  | `4.x~latest`             | `0.8.6~latest`           |
| **backend**     | `String`       | `lc`            | 后端类型                                                     | `5.x~latest`             | `0.8.6~latest`           |
| **enableQQ**    | `Boolean`      | `false`         | **Deleted**  详见表格底下备注,和faq                          | `2.x~3.x`                | :x:                      |



### **mode** `String`

- Default: `xCss`
- Options: 

  - `DesertsP` DesertsP 样式. [demo](https://minivaline.js.org/DesertsP.html)
  - `xCss`  xCss 样式. [demo](https://minivaline.js.org/xCss.html)

### **Math** `Boolean`: 

+ `false` Close MathJax.

+ `true`  Support MathJax@3 initialization.

+ > The above is the initialization operation of integrating MathJax in MiniValine.
  > If MathJax is loaded on the page, MiniValine will use the MathJax version on the page.

### **lang** `String`:

- Default: `navigator.language || navigator.userLanguage`.

- Localization language key, en and zh-CN are currently available.
  - More i18n info: 
  - [How to Add or Improve translation?](https://minivaline.js.org/docs/cn/#/Contribute?id=how-to-add-or-improve-translation)
  

### **emoticonUrl** `String Array`

- Default:`['https://cdn.jsdelivr.net/npm/alus@latest']`

- 注意json和yaml之间的差异

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

- 自定义表情.

  - [如何自定义表情?](https://minivaline.js.org/docs/cn/#/Options?id=how-to-customize-emoticons)



### **serverURLs** `String`

+ Default: `http[s]://[tab/us].avoscloud.com` 即

+ Option
  
  + 默认
    
    + 国际版Leancloud服务地址，将自动检测海外版本（使用国际版**无需**手动填写）。
    
  + 国内版自己绑定域名地址
  
    + 此配置适用于国内自定义域名用户
  
  + cloudflare中间安全处理地址
  
    + [Try to use cloudflare workers edge computing to improve the security](https://minivaline.js.org/docs/en/#/FAQ?id=how-to-improve-the-security-of-minivaline)
  
  + 使用自定义后端的后端地址
  
    + [how-to-add-backend](https://minivaline.js.org/docs/en/#/Options?id=how-to-add-backend-)
  
    + > 目前只支持waline，你可以加入我们一起开发更多类型～

### **barrager** `Number`

+ Default: `0`
+ Options: 
  + `0`  Close Comment barrage.
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

  + `lc`  Leancloud无后端应用模式.
  + `waline`  使用 [waline](https://github.com/lizheming/waline) 作为后端程序.

+ > **serverURLs**需要修改为 Waline 的服务端地址 参考 [Demo 配置](https://github.com/MiniValine/MiniValine.github.io/blob/master/waline.html#L46).
  >
  > waline 后端配置请参考：https://github.com/lizheming/waline



## Style Options

### DesertsP Style mode Options

| Option            | type     | Default | description                                | Minivaline<br />前端版本 | Waline    <br />后端版本 |
| ----------------- | -------- | ------- | ------------------------------------------ | ------------------------ | ------------------------ |
| **adminEmailMd5** | `String` | `null`  | The MD5 of Admin Email to show Admin Flag. | `1.x~latest`             | :white_check_mark:       |



### xCss Style mode Options



| Option         | type           | Default | description                                                  | Minivaline<br />前端版本 | Waline    <br />后端版本 |
| -------------- | -------------- | ------- | ------------------------------------------------------------ | ------------------------ | ------------------------ |
|                |                |         | 下面是访客标识配置                                           |                          |                          |
| **closeFlag**  | `Boolean`      | `false` | 关闭访客标识                                                 | `3.x~4.x`                | :x:                      |
| **enableFlag** | `Boolean`      | `false` | 开启访客标识                                                 | 5.x~latest`              | `0.8.6~latest`           |
|                |                |         | 下面是本地访客标识配置(写在配置里的那种)                     |                          |                          |
| **master**     | `String Array` | `[]`    | 管理员邮箱md5将显示管理员标识                                | `2.x~latest`             | `0.8.6~latest`           |
| **friends**    | `String Array` | `[]`    | 管朋友邮箱md5将显示朋友标识                                  | `2.x~latest`             | `0.8.6~latest`           |
| **tagMeta**    | `String Array` | `[]`    | 朋友标识类型（仅支持三项）例如: `tagMeta: ["Master", "Friend", "Visitor"]` | `2.x~latest`             | `0.8.6~latest`           |
|                |                |         | 下面是云端访客标识配置(写在leancloud配置里的那种)            |                          |                          |
| **cloudflag**  | `Boolean`      | `false` | 云标识，具体看表后和FAQ                                      | `3.x~latest`             | :x:                      |
|                |                |         | xCss 样式的其他选项                                          |                          |                          |
| **region**     | `Boolean`      | `false` | 现实地区                                                     | `3.x~latest`             | :x:                      |
| **closeUA**    | `Boolean`      | `false` | 关闭UA                                                       | `3.x~4.x`                | :x:                      |
| **enableUA**   | `Boolean`      | `false` | 开启UA                                                       | `5.x~latest`             | `0.8.6~latest`           |



#### **cloudflag** `Boolean`

+ Default: `false`
  
  + If `cloudflag` is turned on, the setting of `Visitor Flag Local Options` is invalid.
  
+ How to Set Visitor Flag Cloud Option For xCss Style mode? 见下面Advance高级设置
  
#### **region** `Boolean`

+ Default: `false`
  
  + According to IP output area.
  
  + Note: Currently only Chinese API is available and NoRecordIP: `false`.





## Advance

### Get `App ID`/`App Key`

#### Get `App ID`/`App Key` from LeanCloud

+ [Click here](https://console.leancloud.app/login.html#/signup) 注册或登录 `LeanCloud`. （这是国际版教程，国内版类似）
+ [Click here](https://console.leancloud.app/applist.html#/newapp) 注册一个 `LeanCloud` 应用, 按照下面获取 `appId`/`appKey`.

![image.png](https://upimage.alexhchu.com/2020/10/31/65b007f83f814.png)



#### Add Security URL

添加安全域名，就是要使用minivaline的地址，

可以是https://yourname.github.io,也可以是自己的域名记得加上https或者http

![image.png](https://upimage.alexhchu.com/2020/10/31/9de6ae76f83c1.png)





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

> 如何添加后端？

支持waline后端，配置waline后端请参考 : https://github.com/lizheming/waline

> 注意
>
> 一些选项可能不支持waline后端，在选项表都标明了

