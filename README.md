# gulp-avif-css

> Generates additional expressions with `.webp` & `.avif` classes and appropriate extension

## Usage

Install `gulp-avif-css` as a development dependency:

```shell
npm install -D gulp-avif-css
```

Add it to your `gulpfile.js`

```javascript
const gulp = require("gulp")
const avifcss = require("gulp-avif-css")

gulp.src("./src/css/*.css")
    .pipe(avifcss())
    .pipe(gulp.dest("./dist"))
```

Include special plugin adds `.avif` and `.webp` classes to body (if it supports) into your JavaScript file (add it into head tag)

```javascript
import "gulp-avif-css/plugin"
```

## Examples

#### Input:

```css
.box {
    background-image: url("image.png");
}
```

#### Output:

```css
.box {
    background-image: url("image.png");
}

.webp .box {
    background-image: url("image.webp");
}

.avif .box {
    background-image: url("image.avif");
}
```

## Parameters

### `extensions`
Type: `Array`\
Default: `["png", "jpg", "jpeg", "JPG", "JPEG"]`

Sets fallback extensions
