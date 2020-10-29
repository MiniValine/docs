## Install

Two ways.

### links

```html

<script src="https://cdn.jsdelivr.net/npm/minivaline@4/dist/MiniValine.min.js"></script>

```

+  Recommend the latest version https://www.npmjs.com/package/minivaline

### npm install

``` bash
# Install minivaline
npm install minivaline --save
```

``` js
// Use import
import MiniValine from 'minivaline';
// or Use require
const MiniValine = require('minivaline');

new MiniValine({
    el:'#vcomments',
    // other config
})
```



## Usage

### Simple

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>MiniValine - A simple comment system based on Leancloud.</title>
    <!--Load js and insert it before </ body>-->
    <script src="https://unpkg.com/minivaline/dist/MiniValine.min.js"></script>
</head>
<body>
    <div class="mvcomment"></div>
    <script>
      new MiniValine({
          el: '.mvcomment',
          appId: 'Your App ID',
          appKey: 'Your Key',
          placeholder: 'Write a Comment O(∩_∩)O~~'
      });
    </script>
</body>
</html>
```

### The Smart Way with pjax

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>MiniValine - A simple comment system based on Leancloud.</title>
</head>
<body>
    <div class="mvcomment"></div>
    <script>
    function load_minivaline() {
        setTimeout(function() {
            var HEAD = document.getElementsByTagName('head')[0] || document.documentElement;
            var src = 'https://cdn.jsdelivr.net/npm/minivaline@4/dist/MiniValine.min.js'
            var script = document.createElement('script')
            script.setAttribute('type','text/javascript')
            script.onload = function() {
               pjax_minivaline()
            }
            script.setAttribute('src', src)
            HEAD.appendChild(script)
        }, 1);
    };
    function pjax_minivaline() {
        if(!document.querySelectorAll(".mvcomment")[0])return;
        new MiniValine({
            el: '.mvcomment',
            appId: 'Your App ID',
            appKey: 'Your Key',
            placeholder: 'Write a Comment O(∩_∩)O~~'
        });
    }
    load_minivaline();
    document.addEventListener('pjax:complete', function () {
        pjax_minivaline();
    });
    </script>
</body>
</html>
```