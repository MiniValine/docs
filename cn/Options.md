## Base Options

| Option          | type           | Required or Default                                     | description                                                  | Support version |
| --------------- | -------------- | ------------------------------------------------------- | ------------------------------------------------------------ | --------------- |
| **el**          | `String`       | **Required**.                                           | [object HTMLDivElement] 挂载在哪                             |                 |
| **appId**       | `String`       | **Required**.                                           | 你的 App ID 详见 **Advance**                                 |                 |
| **appKey**      | `String`       | **Required**.                                           | 你的 App Key,详见 **Advance**                                |                 |
| **mode**        | `String`       | Default: `DesertsP`                                     | 详见表格底下备注                                             |                 |
| **placeholder** | `String`       | Default: `null`                                         | 输入框占位符                                                 |                 |
| **pathname**    | `String`       | Default: `location.pathname`                            | 文章路径                                                     |                 |
| **math**        | `Boolean`      | Default: `true`                                         | 详见表格底下备注                                             |                 |
| **md**          | `Boolean`      | Default:`true`                                          | 支持markdown                                                 |                 |
| **dark**        | `Boolean`      | Default: `false`                                        | 黑暗模式                                                     |                 |
| **lang**        | `String`       | Default: `navigator.language || navigator.userLanguage` | 详见表格底下备注                                             |                 |
| **emoticonUrl** | `String Array` | Default: `['https://cdn.jsdelivr.net/npm/alus@latest']` | 详见表格底下备注                                             |                 |
| **NoRecordIP**  | `Boolean`      | Default: `false`                                        | 不记录评论者IP                                               |                 |
| **maxNest**     | `Number`       | Default: `6`                                            | 评论引用最大深度                                             |                 |
| **pageSize**    | `Number`       | Default: `6`                                            | Pagination size.                                             |                 |
| **visitor**     | `Boolean`      | Default: `true`                                         | Only `article reading access statistics`and `whole site access statistics` are provided. |                 |
| **serverURLs**  | `String`       | Default: `http[s]://[tab/us].avoscloud.com`             | 详见表格底下备注                                             |                 |
| **barrager**    | `Number`       | Default: `1`                                            | 详见表格底下备注                                             |                 |
| **role**        | `String`       | Default: `admin`                                        | 详见表格底下备注                                             |                 |
| **closeCSS**    | `Boolean`      | Default: `false`                                        | 关闭加载动画                                                 |                 |
|                 |                |                                                         |                                                              |                 |

+ **el** `String`

  + **Required**. [object HTMLDivElement]
  
+ > 即挂载在什么地方，可以在 **Install** 找到例子
    >
    > 一些插件可能事先写在实现逻辑里面了，不需要再添加这项，如果再添加可能导致错误, 比如 [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) 

+ **mode** `String`

  - Default: `DesertsP`
  - Options: 

    - `DesertsP` DesertsP 样式.
    - `xCss`  xCss 样式.

+ **Math** `Boolean`: 

  + `false` Close MathJax.

  + `true`  Support MathJax@3 initialization.

  + > The above is the initialization operation of integrating MathJax in MiniValine.
    > If MathJax is loaded on the page, MiniValine will use the MathJax version on the page.

- **lang** `String`:

  - Default: `navigator.language || navigator.userLanguage`.
- Localization language key, en and zh-CN are currently available.
  - More i18n info: 
  - [How to Add or Improve translation?](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-add-or-improve-translation)
  
- **emoticonUrl** `String Array`

  - Default: `['https://cdn.jsdelivr.net/npm/alus@latest']`
  - Expression Url.
  - [How to customize emoticons?](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-customize-emoticons)
  
- **serverURLs** `String`

  + Default: `http[s]://[tab/us].avoscloud.com`
    
  + >  This configuration is suitable for domestic custom domain name users, the overseas version will be automatically detected (no need to fill in manually).
    
  + [Try to use cloudflare workers edge computing to improve the security](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-improve-the-security-of-minivaline)


- **barrager** `Number`

  + Default: `1`
  
  + Options: 
  + `0`  Close Comment barrage.
    + `1`  Load a round of Comment barrage.
    + `2`  Load all round of Comment barrage
  

Comment barrage. [Load only when the page is ***first*** loaded]

- **role** `String`

  + Default: `admin`
  
  + Write permissions for the administrator role. 
  
  + [Valine-Android](https://github.com/yinhanlei/Valine-Android)  [Valine-iOS](https://github.com/xaoxuu/Valine-iOS) 



## Style Options

### DesertsP Style mode Options

| Option            | type     | Required or Default | description                                | Support version |
| ----------------- | -------- | ------------------- | ------------------------------------------ | --------------- |
| **adminEmailMd5** | `String` | Default:`null`      | The MD5 of Admin Email to show Admin Flag. |                 |
|                   |          |                     |                                            |                 |





### xCss Style mode Options



| Option        | type           | Required or Default | description                                                  | Support version |
| ------------- | -------------- | ------------------- | ------------------------------------------------------------ | --------------- |
|               |                |                     | visitor flag bellow                                          |                 |
| **closeFlag** | `Boolean`      | Default: `false`    | Turn off visitor flag.                                       |                 |
|               |                |                     | Visitor Flag **Local** Options bellow                        |                 |
| **master**    | `String Array` | Default: `[]`       | The MD5 String Array of master Email to show master Flag.    |                 |
| **friends**   | `String Array` | Default: `[]`       | The MD5 String Array of friends Email to show friends Flag.  |                 |
| **tagMeta**   | `String Array` | Default: `[]`       | The String Array of Words to show Flag (only three).For Example: `tagMeta: ["Master", "Friend", "Visitor"]` |                 |
|               |                |                     | Visitor Flag **Cloud** Option bellow                         |                 |
| **cloudflag** | `Boolean`      | Default: `false`    | 详见表格底下备注                                             |                 |
|               |                |                     | xCss Style mode **Others Options** bellow                    |                 |
| **region**    | `Boolean`      | Default: `false`    | 详见表格底下备注                                             |                 |
| **closeUA**   | `Boolean`      | Default: `false`    | Turn off UA detection.                                       |                 |



- **cloudflag** `Boolean`

  + Default: `false`
  
  + If `cloudflag` is turned on, the setting of `Visitor Flag Local Options` is invalid.

  + [How to Set Visitor Flag Cloud Option For xCss Style mode?](https://github.com/MiniValine/MiniValine/blob/master/.github/FAQ.md#how-to-set-visitor-flag-cloud-option-for-xcss-style-mode)

- **region** `Boolean`

  + Default: `false`
  
  + According to IP output area.
  
  + Note: Currently only Chinese API is available and NoRecordIP: `false`.





## Advance

### Get `App ID`/`App Key`

**Get `App ID`/`App Key` from LeanCloud**  
[Click here](https://console.leancloud.app/login.html#/signup) to register or login in `LeanCloud`.  
[Click here](https://console.leancloud.app/applist.html#/newapp) Create new application in `LeanCloud`, and you will get `appId`/`appKey`.





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

#### 1.Create a GitHub repository named [alus](https://github.com/MiniValine/alus).

#### 2.Add custom emoji picture files in GitHub Repository.

#### 3.The most important is that you need to add [index.json](https://github.com/MiniValine/alus/blob/master/index.json) in the root directory.

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

#### 4.Get CDN link

jsdelivr CDN link : https://cdn.jsdelivr.net/gh/[YourGitHubUsername]/[GitHubRepositoryName]

Be careful not to have `/` at the end of the URL

For example:

```
https://cdn.jsdelivr.net/gh/MiniValine/alus
```

#### 5.Modify MiniValine configuration item `emoticonUrl`


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





