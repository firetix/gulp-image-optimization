# [gulp](https://github.com/wearefractal/gulp)-image-optimization [![Build Status](https://secure.travis-ci.org/sindresorhus/gulp-imagemin.png?branch=master)](http://travis-ci.org/sindresorhus/gulp-imagemin)

> Minify PNG, JPEG and GIF images with [image-min](https://github.com/kevva/image-min)

*Issues with the output should be reported on the image-min [issue tracker](https://github.com/kevva/image-min/issues).*

## Install

Install with [npm](https://npmjs.org/package/gulp-image-optimization)

```
npm install --save-dev gulp-image-optimization
```


## Example

```js
var gulp = require('gulp');
var imagemin = require('gulp-image-optimization');

gulp.task('images', function(cb) {
    gulp.src(['src/**/*.png','src/**/*.jpg','src/**/*.gif','src/**/*.jpeg']).pipe(imagemin({
        optimizationLevel: 5,
        progressive: true,
        interlaced: true
    })).pipe(gulp.dest('public/images')).on('end', cb).on('error', cb);
});


## API

### imagemin(options)

See the image-min [options](https://github.com/kevva/image-min#options).


## License

MIT © [Mohamed Rachidi](http://sindresorhus.com)
