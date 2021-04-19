# Options

MiniValine 自 version 6.x 起回归极简主义！ 因此 6.x 移除了 5.x 的全部功能特性，只保留了基础评论功能！！！

> Less is More
------------------------------

!> 注意这里是 MiniValine version 6.x 的配置项

## Mount Options

!> 注意一些插件不需要添加Mount Options（挂载选项），直接看底下的基础选项和样式选项

> 一些插件可能事先写在实现逻辑里面了，不需要再添加这项，如果再添加可能导致错误, 
>
> 比如 [hexo-next-minivaline](https://github.com/MiniValine/hexo-next-minivaline) | [docsify-minivaline](https://github.com/MiniValine/docsify-minivaline) **不要**添加这个选项

| Option   | type     | Required or Default                      | description                      |
| -------- | -------- | ---------------------------------------- | -------------------------------- |
| **el**   | `String` | **Required**.                            | [object HTMLDivElement] 挂载在哪 |
| **path** | `String` | Default: `location.pathname`的最终的取值 | 文章路径，详见表格底下备注       |

### **el** `String`

+ **Required**. [object HTMLDivElement]

+ > 即挂载在什么地方，可以在 [**Install**](https://minivaline.js.org/docs/cn/#/Install) 找到例子
  >

### **path** `String`

+ Default: `location.pathname`的最终的取值

+ The pathname of the page

+ > 即 文章路径 ，可以在 [**Install**](https://minivaline.js.org/docs/v5/#/Install) 找到例子
  >
  > 注意如果开发一个主题或插件，有些场景不用加引号，因为本身是变量，加了引号变成常字符串了。


## Base Options

| Option                 | type           | Default               | description                                                  |
| ---------------------- | -------------- | --------------------- | ------------------------------------------------------------ |
| **serverURL**          | `String`       | `null`                | Cloudflare workers 后端地址                                   |
| **placeholder**        | `String`       | `null`                | 输入框占位符                                                  |
| **lang**               | `String`       | 用户目前语言           | 语言                                                          |
| **emoticonUrl**        | `String Array` | 内置表情               | 自定义表情链接                                                |
| **maxNest**            | `Number`       | `6`                   | 评论嵌套最大深度                                              |
| **pageSize**           | `Number`       | `6`                   | 每页评论数目                                                  |
| **avatarUrl**          | `String`       | gravatar头像CDN        | 自定义头像CDN                                                 |
| **avatarD**            | `String`       | 默认头像               | 自定义默认头像                                                 |
| **uploadImageURL**     | `String`       | 默认图床地址           | 自定义图床地址                                                 |
| **uploadImageParse**   | `Function`     | 默认图床返回值解析方法  | 自定义图床返回值解析方法                                        |

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

### **avatarUrl** `String`

+ Default: `https://cdn.v2ex.com/gravatar`
+ 头像CDN



### **avatarD** `String`

+ Default: `robohash`
+ 默认头像
+ 详见 https://secure.gravatar.com/site/implement/images/#default-image

## Advance

### How to Add Dark Mode?

可使用 CSS 变量修改配色方案.

### 如何自定义图床？

向 uploadImageURL 发送 POST 请求，使用 uploadImageParse 方法解析返回值

```js
new MiniValine({
  uploadImageURL:'https://xxxx上传地址',
  uploadImageParse:((res)=>{
    console.log(res)
    return "xxxx上传地址返回的图片链接地址"
  })
});
```
### 回调函数

#### FinishLoaded

成功挂载后回调

```js
new MiniValine({
  FinishLoaded:(()=>{
    console.log("FinishLoaded")
  })
});
```

#### PageLoaded

每页加载完成后回调

```js
new MiniValine({
  PageLoaded:(()=>{
    console.log("PageLoaded")
  })
});
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
      placeholder: 'Write a Comment',
      emoticonUrl: ['https://cdn.jsdelivr.net/gh/MiniValine/alus']
  });

```

or

```
  new MiniValine({
      el: '.comment',
      placeholder: 'Write a Comment',
      emoticonUrl: ['https://cdn.jsdelivr.net/gh/MiniValine/Bilibilis@master','https://cdn.jsdelivr.net/npm/alus']
  });

```




 6.Try to be faster.

The author uses a `Python` script to generate `index.json` here. The friends who have the ability can try it.

Modify `FilePath` please.

```python
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
