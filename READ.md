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
```
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
```
  <link rel="stylesheet" href="./css/style.css">
  <script type="text/javascript" src="./js/style.js"></script>
```
