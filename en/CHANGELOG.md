# Version

> + [Option Detail](https://minivaline.js.org/docs/en/#/Options)  |  [Release Version](https://www.npmjs.com/package/minivaline)  | [Version ChangeLog](https://minivaline.js.org/docs/en/#/CHANGELOG)
> + Note that we **recommend** that you update the **fixed** ones. 
> + The **add**ed ones mean that **previous** versions are **not supported**.
> + And the **deleted** ones mean that there may be some problems when **upgrading**. 
> + Please **test the configuration** before plan to **change version**!



## 5.x （Latest）

- Adaptive pairing [waline](https://github.com/lizheming/waline) Back end data interaction
- All advanced rendering functions are turned off by default, that is, only the basic comment function is enabled by default

### Add

- option.backend
- option.enableFlag
- option.enableUA
- option.RecordIP

### Change

- option.barrager The default value is changed from`1`to`0`
- option.md The default value is changed from`true`to`false`
- option.math The default value is changed from`true`to`false`
- option.visitor The default value is changed from`true`to`false`
- option.mode The default value is changed from`DesertsP`to`xCss`

### Fix

+ Null

### Del

+ option.closeFlag
+ option.closeUA
+ option.NoRecordIP



## 4.x 

### Add

+ Security Policy Support
+ option.closeCSS

### Fix

+ Remediation of potential prototype contamination

### Del

+ [option.enableQQ](https://minivaline.js.org/docs/en/#/Options?id=enableqq-boolean)

---

## 3.x

### Add

+ option.dark
+ option.barrager
+ option.role
+ option.xCss.closeFlag
+ option.xCss.cloudflag
+ option.xCss.region
+ option.xCss.closeUA

### Fix

+ Cannot close UA and open region at the same time
+ Artitalk is not compatible with minivaline

### Del

+ Null

----

## 2.x

### Add

+ option.mode
+ option.visitor
+ option.enableQQ
+ option.xCss.master
+ option.xCss.friends
+ option.xCss.tagMeta

### Fix

+ Null

### Del

+ Null

----

## 1.x

### Add

+ option.el
+ option.appId
+ option.appKey
+ option.placeholder
+ option.math
+ option.md
+ option.lang
+ option.emoticonUrl
+ option.NoRecordIP
+ option.maxNest
+ option.pageSize
+ option.serverURLs
+ option.DesertsP.adminEmailMd5

### Fix

+ Null

### Del

+ Null



