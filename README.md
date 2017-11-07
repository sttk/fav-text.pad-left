# [@fav/text.pad-left][repo-url] [![NPM][npm-img]][npm-url] [![MIT License][mit-img]][mit-url] [![Build Status][travis-img]][travis-url] [![Build Status][appveyor-img]][appveyor-url] [![Coverage status][coverage-img]][coverage-url]

Pad characters on left side of a source string.

> "fav" is an abbreviation of "favorite" and also the acronym of "for all versions".
> This package is intended to support all Node.js versions and many browsers as possible.
> At least, this package supports Node.js >= v0.10 and major Web browsers: Chrome, Firefox, IE11, Edge, Vivaldi and Safari.


## Install

To install from npm:

```sh
$ npm install --save @fav/text.pad-left
```

***NOTE:*** *npm < 2.7.0 does not support scoped package, but even old version Node.js supports it. So when you use such older npm, you should download this package from [github.com][repo-url], and move it in `node_modules/@fav/text.pad-left/` directory manually.*


## Usage

For Node.js, when installing `@fav/text.pad-left` from npm:

```js
var padLeft = require('@fav/text.pad-left');
padLeft('abc', 8); // => '     abc'
padLeft('abc', 8, '_-'); // => '_-_-_abc'
```

For Web browsers:

```html
<script src="fav.text.pad-left.min.js"></script>
<script>
var padLeft = fav.text.padLeft;
padLeft('abc', 8); // => '     abc'
</script>
```


## API

### <u>padLeft(source, [, length ] [, padding ]) : string</u>

Pads *padding* on left side of *source*.

If *length* is less than the length of *source*, return *source* with no padding.

If *padding* is not specified, this function use a white space (`'\u0020'`) as a padding.

**NOTE:** This function doesn't check data types of the arguments, and assumes that they are given as per the specific data type.

**NOTE:** This function is different from `String#padStart` at the point that it uses a white space (`'\u0020'`) as *padding* when specified `null` or an empty string to *padding*.  

#### Parameter:

| Parameter |  Type  | Description                      |
|-----------|--------|----------------------------------|
| source    | string | The source string.               |
| length    | number | The length of the result text. (Optional, and `source.length` in default.) |
| padding   | string | The padding characters. (Optional, and `' '` in default.) |

#### Return:

The padded string.

**Type:** string


## Checked                                                                      

### Node.js (4〜8)

| Platform  |   4    |   5    |   6    |   7    |   8    |
|:---------:|:------:|:------:|:------:|:------:|:------:|
| macOS     |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Windows10 |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|

### io.js (1〜3)

| Platform  |   1    |   2    |   3    |
|:---------:|:------:|:------:|:------:|
| macOS     |&#x25ef;|&#x25ef;|&#x25ef;|
| Windows10 |&#x25ef;|&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef;|&#x25ef;|

### Node.js (〜0.12)

| Platform  |  0.7   |  0.8   |  0.9   |  0.10  |  0.11  |  0.12  |
|:---------:|:------:|:------:|:------:|:------:|:------:|:------:|
| macOS     |        |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Windows10 |        |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|&#x25ef;|

### Web browsers

| Platform  | Chrome | Firefox | Vivaldi | Safari |  Edge  | IE11   |
|:---------:|:------:|:-------:|:-------:|:------:|:------:|:------:|
| macOS     |&#x25ef;|&#x25ef; |&#x25ef; |&#x25ef;|   --   |   --   |
| Windows10 |&#x25ef;|&#x25ef; |&#x25ef; |   --   |&#x25ef;|&#x25ef;|
| Linux     |&#x25ef;|&#x25ef; |&#x25ef; |   --   |   --   |   --   |


## License

Copyright (C) 2017 Takayuki Sato

This program is free software under [MIT][mit-url] License.
See the file LICENSE in this distribution for more details.

[repo-url]: https://github.com/sttk/fav-text.pad-left/
[npm-img]: https://img.shields.io/badge/npm-v0.1.0-blue.svg
[npm-url]: https://www.npmjs.com/package/@fav/text.pad-left
[mit-img]: https://img.shields.io/badge/license-MIT-green.svg
[mit-url]: https://opensource.org/licenses/MIT
[travis-img]: https://travis-ci.org/sttk/fav-text.pad-left.svg?branch=master
[travis-url]: https://travis-ci.org/sttk/fav-text.pad-left
[appveyor-img]: https://ci.appveyor.com/api/projects/status/github/sttk/fav-text.pad-left?branch=master&svg=true
[appveyor-url]: https://ci.appveyor.com/project/sttk/fav-text-pad-left
[coverage-img]: https://coveralls.io/repos/github/sttk/fav-text.pad-left/badge.svg?branch=master
[coverage-url]: https://coveralls.io/github/sttk/fav-text.pad-left?branch=master
