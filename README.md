# gulp-avif-css

> Generates additional `.webp` & `.avif` classes for loading a specific image if it's supported by the browser

## Usage

Install `gulp-avif-css`:

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

Include the special plugin which adds `.avif` and `.webp` classes for `<body>` (if it's supported) into a JavaScript file and load it in `<head>` tag

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

Sets extensions that are going to be targeted by the plugin
