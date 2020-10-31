# Options

> 切换版本之前，或者使用`@latest`版本的时候，在大更新之前，关注一下 [更新日志](https://minivaline.js.org/docs/en/#/CHANGELOG) 。
>
> [选项细节](https://minivaline.js.org/docs/cn/#/Options)  |  [发行版本](https://www.npmjs.com/package/minivaline)  | [版本更新日志](https://minivaline.js.org/docs/cn/#/CHANGELOG)

## Base Options

| Option          | type           | Required or Default                                     | description                                                  | Support version |
| --------------- | -------------- | ------------------------------------------------------- | ------------------------------------------------------------ | --------------- |
| **el**          | `String`       | **Required**.                                           | [object HTMLDivElement] 挂载在哪                             | `1.x~latest`    |
| **appId**       | `String`       | **Required**.                                           | 你的 App ID 详见 [Advace](https://minivaline.js.org/docs/cn/#/Options?id=get-app-idapp-key) | `1.x~latest`    |
| **appKey**      | `String`       | **Required**.                                           | 你的 App Key,详见 [Advace](https://minivaline.js.org/docs/cn/#/Options?id=get-app-idapp-key) | `1.x~latest`    |
| **mode**        | `String`       | Default: `DesertsP`                                     | 详见表格底下备注                                             | `2.x~latest`    |
| **placeholder** | `String`       | Default: `null`                                         | 输入框占位符                                                 | `1.x~latest`    |
| **pathname**    | `String`       | Default: `location.pathname`                            | 文章路径，详见表格底下备注                                   | `1.x~latest`    |
| **math**        | `Boolean`      | Default: `true`                                         | 详见表格底下备注                                             | `1.x~latest`    |
| **md**          | `Boolean`      | Default:`true`                                          | 支持markdown                                                 | `1.x~latest`    |
| **dark**        | `Boolean`      | Default: `false`                                        | 黑暗模式                                                     | `3.x~latest`    |
| **lang**        | `String`       | Default: `navigator.language or navigator.userLanguage` | 详见表格底下备注                                             | `1.x~latest`    |
| **emoticonUrl** | `String Array` | Default: `['https://cdn.jsdelivr.net/npm/alus@latest']` | 详见表格底下备注                                             | `1.x~latest`    |
| **NoRecordIP**  | `Boolean`      | Default: `false`                                        | 不记录评论者IP                                               | `1.x~latest`    |
| **maxNest**     | `Number`       | Default: `6`                                            | 评论引用最大深度                                             | `1.x~latest`    |
| **pageSize**    | `Number`       | Default: `6`                                            | Pagination size.                                             | `1.x~latest`    |
| **visitor**     | `Boolean`      | Default: `true`                                         | Only `article reading access statistics`and `whole site access statistics` are provided. | `2.x~latest`    |
| **serverURLs**  | `String`       | Default: `http[s]://[tab/us].avoscloud.com`             | 详见表格底下备注                                             | `1.x~latest`    |
| **barrager**    | `Number`       | Default: `1`                                            | 详见表格底下备注                                             | `3.x~latest`    |
| **role**        | `String`       | Default: `admin`                                        | 详见表格底下备注                                             | `3.x~latest`    |
| **closeCSS**    | `Boolean`      | Default: `false`                                        | 关闭加载动画                                                 | `4.x~latest`    |
| **enableQQ**    | `Boolean`      | Default: `false`                                        | **Deleted**  The details are Under the table                 | `2.x~3.x`       |
|                 |                |                                                         |                                                              |                 |

### **el** `String`

+ **Required**. [object HTMLDivElement]

+ > 即挂载在什么地方，可以在 [**Install**](https://minivaline.js.org/docs/cn/#/Install) 找到例子
  >
  > 一些插件可能事先写在实现逻辑里面了，不需要再添加这项，如果再添加可能导致错误, 
>
  > 比如 [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) **不要**添加这个选项

### **pathname** `String`

+ Default: `location.pathname`

+ The pathname of the page

+ > 即 文章路径 ，可以在 [**Install**](https://minivaline.js.org/docs/cn/#/Install) 找到例子
  >
  > 一些插件可能事先写在实现逻辑里面了，不需要再添加这项，如果再添加可能导致错误, 
  >
  > 比如 [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) **不要**添加这个选项

### **mode** `String`

- Default: `DesertsP`
- Options: 

  - `DesertsP` DesertsP 样式.
  - `xCss`  xCss 样式.

### **Math** `Boolean`: 

+ `false` Close MathJax.

+ `true`  Support MathJax@3 initialization.

+ > The above is the initialization operation of integrating MathJax in MiniValine.
  > If MathJax is loaded on the page, MiniValine will use the MathJax version on the page.

### **lang** `String`:

- Default: `navigator.language || navigator.userLanguage`.

- Localization language key, en and zh-CN are currently available.
  - More i18n info: 
  - [How to Add or Improve translation?](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-add-or-improve-translation)
  

### **emoticonUrl** `String Array`

- Default: `['https://cdn.jsdelivr.net/npm/alus@latest']`
- Expression Url.
- [How to customize emoticons?](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-customize-emoticons)

### **serverURLs** `String`

+ Default: `http[s]://[tab/us].avoscloud.com`
  
+ >  This configuration is suitable for domestic custom domain name users, the overseas version will be automatically detected (no need to fill in manually).
  
+ [Try to use cloudflare workers edge computing to improve the security](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-improve-the-security-of-minivaline)

### **barrager** `Number`

+ Default: `1`

+ Options: 
  + `0`  Close Comment barrage.
  + `1`  Load a round of Comment barrage.
  + `2`  Load all round of Comment barrage
+ Comment barrage. [Load only when the page is ***first*** loaded]

### **role** `String`

+ Default: `admin`

+ Write permissions for the administrator role. 

+ [Valine-Android](https://github.com/yinhanlei/Valine-Android)  [Valine-iOS](https://github.com/xaoxuu/Valine-iOS) 

### **enableQQ** `Boolean`

**deleted!!!**

+ Default: `false`

+ Enable QQ avatar API.

+ > Since the QQ avatar API exposes the user's mailbox, the function of QQ avatar is **deleted** in MiniValine version 4.x.



## Style Options

### DesertsP Style mode Options

| Option            | type     | Required or Default | description                                | Support version |
| ----------------- | -------- | ------------------- | ------------------------------------------ | --------------- |
| **adminEmailMd5** | `String` | Default:`null`      | The MD5 of Admin Email to show Admin Flag. | `1.x~latest`    |
|                   |          |                     |                                            |                 |





### xCss Style mode Options



| Option        | type           | Required or Default | description                                                  | Support version |
| ------------- | -------------- | ------------------- | ------------------------------------------------------------ | --------------- |
|               |                |                     | visitor flag bellow                                          |                 |
| **closeFlag** | `Boolean`      | Default: `false`    | Turn off visitor flag.                                       | `3.x~latest`    |
|               |                |                     | Visitor Flag **Local** Options bellow                        |                 |
| **master**    | `String Array` | Default: `[]`       | The MD5 String Array of master Email to show master Flag.    | `2.x~latest`    |
| **friends**   | `String Array` | Default: `[]`       | The MD5 String Array of friends Email to show friends Flag.  | `2.x~latest`    |
| **tagMeta**   | `String Array` | Default: `[]`       | The String Array of Words to show Flag (only three).For Example: `tagMeta: ["Master", "Friend", "Visitor"]` | `2.x~latest`    |
|               |                |                     | Visitor Flag **Cloud** Option bellow                         |                 |
| **cloudflag** | `Boolean`      | Default: `false`    | 详见表格底下备注                                             | `3.x~latest`    |
|               |                |                     | xCss Style mode **Others Options** bellow                    |                 |
| **region**    | `Boolean`      | Default: `false`    | 详见表格底下备注                                             | `3.x~latest`    |
| **closeUA**   | `Boolean`      | Default: `false`    | Turn off UA detection.                                       | `3.x~latest`    |



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
{"0":['A','B','C']}
```

* Only Replace `A`,`B`,`C` with your emoji picture file name. Note the file extension.

* Please note that commas, colons, brackets, braces, quotes use English half-width.

* Please note that the file name of index.json must be `index.json`.

* For example:

``` json
{"0":['emoticonA.png','emoticonB.gif','emoticonC.jpeg','emoticonD.jpg']}
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





