# Version 

> + [选项细节](https://minivaline.js.org/docs/cn/#/Options)  |  [发行版本](https://www.npmjs.com/package/minivaline)  | [版本更新日志](https://minivaline.js.org/docs/cn/#/CHANGELOG)
> + 注意对于修复的内容，我们建议你更新
> + 对于添加的内容意味着之前的版本不支持
> + 删除的功能意味着，不更改配置直接升级可能会出现问题
> + 在改变版本之前，一定要提前测试配置



## 5.x （Latest）

- 适配对[walinel](https://github.com/lizheming/waline)后端数据交互
- 默认关闭所有高级渲染功能,即默认只有基础评论功能

### Add

- option.backend

+ option.enableFlag
+ option.enableUA
+ option.RecordIP

### Change

- option.barrager 默认值由`1`改为`0`
- option.md 默认值由`true`改为`false`
- option.math 默认值由`true`改为`false`
- option.visitor 默认值由`true`改为`false`
- option.mode 默认值由`DesertsP`改为`xCss`

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

+ 修复潜在的原型污染

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

+ 无法同时关闭 UA 和开启 region
+ Artitalk与MiniValine不兼容

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


