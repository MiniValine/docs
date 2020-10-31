# Options

> When you change version, care about [CHANGELOG](https://minivaline.js.org/docs/en/#/CHANGELOG) before.
>
> [Option Detail](https://minivaline.js.org/docs/en/#/Options)  |  [Release Version](https://www.npmjs.com/package/minivaline)  | [Version ChangeLog](https://minivaline.js.org/docs/en/#/CHANGELOG)

## Base Options

| Option          | type           | Required or Default                                     | description                                                  | Support version |
| --------------- | -------------- | ------------------------------------------------------- | ------------------------------------------------------------ | --------------- |
| **el**          | `String`       | **Required**.                                           | The details are Under the table                              | `1.x~latest`    |
| **appId**       | `String`       | **Required**.                                           | Your App ID, detail from [Advance](https://minivaline.js.org/docs/en/#/Options?id=get-app-idapp-key) | `1.x~latest`    |
| **appKey**      | `String`       | **Required**.                                           | Your App Key,detail from [Advance](https://minivaline.js.org/docs/en/#/Options?id=get-app-idapp-key) | `1.x~latest`    |
| **mode**        | `String`       | Default: `DesertsP`                                     | The details are Under the table                              | `2.x~latest`    |
| **placeholder** | `String`       | Default: `null`                                         | Input Placeholder                                            | `1.x~latest`    |
| **pathname**    | `String`       | Default: `location.pathname`                            | The pathname of the page,The details are Under the table     | `1.x~latest`    |
| **math**        | `Boolean`      | Default: `true`                                         | The details are Under the table                              | `1.x~latest`    |
| **md**          | `Boolean`      | Default:`true`                                          | Support Markdown.                                            | `1.x~latest`    |
| **dark**        | `Boolean`      | Default: `false`                                        | [Dark model.](https://minivaline.js.org/docs/en/#/Options?id=how-to-add-dark-mode) | `3.x~latest`    |
| **lang**        | `String`       | Default: `navigator.language or navigator.userLanguage` | The details are Under the table                              | `1.x~latest`    |
| **emoticonUrl** | `String Array` | Default: `['https://cdn.jsdelivr.net/npm/alus@latest']` | The details are Under the table                              | `1.x~latest`    |
| **NoRecordIP**  | `Boolean`      | Default: `false`                                        | Do not record commenter IP.                                  | `1.x~latest`    |
| **maxNest**     | `Number`       | Default: `6`                                            | Sub-comment maximum nesting depth.                           | `1.x~latest`    |
| **pageSize**    | `Number`       | Default: `6`                                            | Pagination size.                                             | `1.x~latest`    |
| **visitor**     | `Boolean`      | Default: `true`                                         | Only `article reading access statistics`and `whole site access statistics` are provided. | `2.x~latest`    |
| **serverURLs**  | `String`       | Default: `http[s]://[tab/us].avoscloud.com`             | The details are Under the table                              | `1.x~latest`    |
| **barrager**    | `Number`       | Default: `1`                                            | The details are Under the table                              | `3.x~latest`    |
| **role**        | `String`       | Default: `admin`                                        | The details are Under the table                              | `3.x~latest`    |
| **closeCSS**    | `Boolean`      | Default: `false`                                        | Turn off loading CSS.                                        | `4.x~latest`    |
| **enableQQ**    | `Boolean`      | Default: `false`                                        | **Deleted**  The details are Under the table                 | `2.x~3.x`       |
|                 |                |                                                         |                                                              |                 |

### **el** `String`

+ **Required**. [object HTMLDivElement]

+ > You can find example at [**Install**](https://minivaline.js.org/docs/en/#/Install)
  >
  > Some plugins, which has been installed before, may not be required, 
>
  > eg  [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) **NOT** ADD this option

### **pathname** `String`

+ Default: `location.pathname`

+ The pathname of the page.

+ > You can find example at [**Install**](https://minivaline.js.org/docs/en/#/Install)
  >
  > Some plugins, which has been installed before, may not be required, 
  >
  > eg  [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) **NOT** ADD this option

### **mode** `String`

- Default: `DesertsP`
- Options: 

  - `DesertsP` DesertsP Style mode.
  - `xCss`  xCss Style mode.

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

- Default: `['https://cdn.jsdelivr.net/npm/alus@latest']`
- Expression Url.
- [How to customize emoticons?](https://minivaline.js.org/docs/en/#/Options?id=how-to-customize-emoticons)


#### **serverURLs** `String`

+ Default: `http[s]://[tab/us].avoscloud.com`
  
+ >  This configuration is suitable for domestic custom domain name users, the overseas version will be automatically detected (no need to fill in manually).
  
+ [Try to use cloudflare workers edge computing to improve the security](https://minivaline.js.org/docs/en/#/FAQ?id=how-to-improve-the-security-of-minivaline)

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
| **cloudflag** | `Boolean`      | Default: `false`    | The details are Under the table                              | `3.x~latest`    |
|               |                |                     | xCss Style mode **Others Options** bellow                    |                 |
| **region**    | `Boolean`      | Default: `false`    | The details are Under the table                              | `3.x~latest`    |
| **closeUA**   | `Boolean`      | Default: `false`    | Turn off UA detection.                                       | `3.x~latest`    |



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



