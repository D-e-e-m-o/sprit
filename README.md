# sprit

[![NPM version](https://badge.fury.io/js/sprit.svg)](http://badge.fury.io/js/sprit)

sprit features:

- Generates sprites and proper style files out of a directory of images.
- Supports multiple reader engine (jimp, canvas, lwip)

# Installation

```bash
npm install sprit
```

# Usage

## Programmatic usage

```js
require('sprit').create({
  src: [
    './icons/*.png', // include files
    '!./icons/ignore-*.png' // ignore files
  ],
  output: {
    processor: require('sprit/src/processor/less-processor')
  }
})

```

## Programmatic usage with Gulp

```js
const gulp = require('gulp')

gulp.task('sprite', () => {
  const options = {
    src: [
      './icons/*.png', // include files
      '!./icons/ignore-*.png' // ignore files
    ],
    output: {
      processor: require('sprit/src/processor/less-processor')
    }
  }
  return require('sprit').src(options)
    .pipe(gulp.dest('./dist'))
})
```

# Thank

- https://github.com/sprity/sprity

# LICENSE

The MIT License (MIT)

see [LICENSE](LICENSE)
