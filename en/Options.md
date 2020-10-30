## Base Options

| Option          | type           | Required or Default                                     | description                                                  | Support version |
| --------------- | -------------- | ------------------------------------------------------- | ------------------------------------------------------------ | --------------- |
| **el**          | `String`       | **Required**.                                           | The details are Under the table                              | `>=4.x`         |
| **appId**       | `String`       | **Required**.                                           | Your App ID, detail from **Advace**                          | `>=4.x`         |
| **appKey**      | `String`       | **Required**.                                           | Your App Key,detail from **Advance**                         | `>=4.x`         |
| **mode**        | `String`       | Default: `DesertsP`                                     | The details are Under the table                              | `>=4.x`         |
| **placeholder** | `String`       | Default: `null`                                         | Input Placeholder                                            | `>=4.x`         |
| **pathname**    | `String`       | Default: `location.pathname`                            | The pathname of the page.                                    | `>=4.x`         |
| **math**        | `Boolean`      | Default: `true`                                         | The details are Under the table                              | `>=4.x`         |
| **md**          | `Boolean`      | Default:`true`                                          | Support Markdown.                                            | `>=4.x`         |
| **dark**        | `Boolean`      | Default: `false`                                        | Dark model.                                                  | `>=4.x`         |
| **lang**        | `String`       | Default: `navigator.language or navigator.userLanguage` | The details are Under the table                              | `>=4.x`         |
| **emoticonUrl** | `String Array` | Default: `['https://cdn.jsdelivr.net/npm/alus@latest']` | The details are Under the table                              | `>=4.x`         |
| **NoRecordIP**  | `Boolean`      | Default: `false`                                        | Do not record commenter IP.                                  | `>=4.x`         |
| **maxNest**     | `Number`       | Default: `6`                                            | Sub-comment maximum nesting depth.                           | `>=4.x`         |
| **pageSize**    | `Number`       | Default: `6`                                            | Pagination size.                                             | `>=4.x`         |
| **visitor**     | `Boolean`      | Default: `true`                                         | Only `article reading access statistics`and `whole site access statistics` are provided. | `>=4.x`         |
| **serverURLs**  | `String`       | Default: `http[s]://[tab/us].avoscloud.com`             | The details are Under the table                              | `>=4.x`         |
| **barrager**    | `Number`       | Default: `1`                                            | The details are Under the table                              | `>=4.x`         |
| **role**        | `String`       | Default: `admin`                                        | The details are Under the table                              | `>=4.x`         |
| **closeCSS**    | `Boolean`      | Default: `false`                                        | Turn off loading CSS.                                        | `>=4.x`         |
| **enableQQ**    | `Boolean`      | Default: `false`                                        | **Deleted**  The details are Under the table                 | `<=3.x`         |
|                 |                |                                                         |                                                              |                 |

+ **el** `String`

  + **Required**. [object HTMLDivElement]
  
+ > You can find example at **Install**
    >
    > Some plugins, which has been installed before, may not be required, eg [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) 

+ **mode** `String`

  - Default: `DesertsP`
  - Options: 

    - `DesertsP` DesertsP Style mode.
    - `xCss`  xCss Style mode.

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
  + Comment barrage. [Load only when the page is ***first*** loaded]
  

- **role** `String`

  + Default: `admin`
  
  + Write permissions for the administrator role. 
  
  + [Valine-Android](https://github.com/yinhanlei/Valine-Android)  [Valine-iOS](https://github.com/xaoxuu/Valine-iOS) 

+ **enableQQ** `Boolean` | **deleted!!!**

  + Default: `false`

  + Enable QQ avatar API.

  + > Since the QQ avatar API exposes the user's mailbox, the function of QQ avatar is **deleted** in MiniValine version 4.x.




## Style Options

### DesertsP Style mode Options

| Option            | type     | Required or Default | description                                | Support version |
| ----------------- | -------- | ------------------- | ------------------------------------------ | --------------- |
| **adminEmailMd5** | `String` | Default:`null`      | The MD5 of Admin Email to show Admin Flag. | `>=4.x`         |
|                   |          |                     |                                            |                 |





### xCss Style mode Options



| Option        | type           | Required or Default | description                                                  | Support version |
| ------------- | -------------- | ------------------- | ------------------------------------------------------------ | --------------- |
|               |                |                     | visitor flag bellow                                          | `>=4.x`         |
| **closeFlag** | `Boolean`      | Default: `false`    | Turn off visitor flag.                                       | `>=4.x`         |
|               |                |                     | Visitor Flag **Local** Options bellow                        | `>=4.x`         |
| **master**    | `String Array` | Default: `[]`       | The MD5 String Array of master Email to show master Flag.    | `>=4.x`         |
| **friends**   | `String Array` | Default: `[]`       | The MD5 String Array of friends Email to show friends Flag.  | `>=4.x`         |
| **tagMeta**   | `String Array` | Default: `[]`       | The String Array of Words to show Flag (only three).For Example: `tagMeta: ["Master", "Friend", "Visitor"]` | `>=4.x`         |
|               |                |                     | Visitor Flag **Cloud** Option bellow                         | `>=4.x`         |
| **cloudflag** | `Boolean`      | Default: `false`    | The details are Under the table                              | `>=4.x`         |
|               |                |                     | xCss Style mode **Others Options** bellow                    | `>=4.x`         |
| **region**    | `Boolean`      | Default: `false`    | The details are Under the table                              | `>=4.x`         |
| **closeUA**   | `Boolean`      | Default: `false`    | Turn off UA detection.                                       | `>=4.x`         |



- **cloudflag** `Boolean`

  + Default: `false`
  
  + If `cloudflag` is turned on, the setting of `Visitor Flag Local Options` is invalid.

  + How to Set Visitor Flag Cloud Option For xCss Style mode? **Advance below** please

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


