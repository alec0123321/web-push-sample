# CSS3: animation & transition & box-shadow

## Transition 的寫法以及縮寫
``` sass
  transition: 0.5s
  transition-delay: 0.5s

  = transition: 0.5s 0.5s
```
# Web Push Sample
##  簡易上傳github pages的自動化流程


> 原先該有的資料結構
> 自行寫入style.sass及style.js
> sass在腳本執行後會自動生成css

| css | sass | js |img |
| -------- | -------- | -------- |-------- |
|      | style.sass    | style.js    |    |

## 使用的套件
> 可以直接使用npm install 從 package.json中下載回來
```js
var gulp = require('gulp'),
    connect = require('gulp-connect-php'),
    browserSync = require('browser-sync'),
    sass = require('gulp-ruby-sass'),
    plumber = require('gulp-plumber'),
    prefix = require('gulp-autoprefixer');
```
## 套件包裡包含
1. /css
2. /img
3. /js
4. /sass
5. gulpfile.js
6. package.json
7. .gitignore

> 套件下載好後就執行 gulp connect-sync 就可以同步瀏覽器寫code了，同時每次寫完sass後存檔就會自動轉成css並且壓縮，圖片也可以透過gulpfile.js裡面的指令進行壓縮
> 記得index.html要引入css不要引入成sass，且資料夾前面要寫.不然在github的server會抓不到資料夾
> js跟jquery最後在body的結尾後引入，以免沒載入成功
```html
  <link rel="stylesheet" href="./css/style.css">
  <script type="text/javascript" src="./js/style.js"></script>
```

> 寫完網站後先初始化Git
> 並上傳 上傳完後開新的分支到gh-pages 在push一次就能直接傳到github page了
```
git init
git add *
git commit -m "first"
git remote add origin [HTTPS]
git push origin master
git checkout -b gh-pages
git push --set-upstream origin gh-pages

```
