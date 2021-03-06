# egg-enums

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![Test coverage][codecov-image]][codecov-url]
[![David deps][david-image]][david-url]
[![Known Vulnerabilities][snyk-image]][snyk-url]
[![npm download][download-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/egg-enums.svg?style=flat-square
[npm-url]: https://npmjs.org/package/egg-enums
[travis-image]: https://img.shields.io/travis/LzxHahaha/egg-enums.svg?style=flat-square
[travis-url]: https://travis-ci.org/LzxHahaha/egg-enums
[codecov-image]: https://img.shields.io/codecov/c/github/LzxHahaha/egg-enums.svg?style=flat-square
[codecov-url]: https://codecov.io/github/LzxHahaha/egg-enums?branch=master
[david-image]: https://img.shields.io/david/LzxHahaha/egg-enums.svg?style=flat-square
[david-url]: https://david-dm.org/LzxHahaha/egg-enums
[snyk-image]: https://snyk.io/test/npm/egg-enums/badge.svg?style=flat-square
[snyk-url]: https://snyk.io/test/npm/egg-enums
[download-image]: https://img.shields.io/npm/dm/egg-enums.svg?style=flat-square
[download-url]: https://npmjs.org/package/egg-enums

<!--
Description here.
-->

## Install

```bash
$ npm i egg-enums --save
```

## Usage

```js
// {app_root}/config/plugin.js
exports.enums = {
  enable: true,
  package: 'egg-enums',
};
```

## Configuration

**There is nothing you need to config.**

## Example

```js
// {app_root}/app/enums/letters.js
// use array to init enum
module.exports = app => app.Enum([
  'A',
  'B',
  'C'
]);

// or

// {app_root}/app/enums/colors.js
// use object to set the values
module.exports = app => app.Enum({
  RED: 1,
  GREEN: 4,
  BLUE: 5,
});

// then you can use like this
console.log(app.enums.Letters.B === 1);       // true
console.log(app.enums.Colors.GREEN === 4);    // true
```

## Questions & Suggestions

Please open an issue [here](https://github.com/LzxHahaha/egg-enums/issues).

## License

[MIT](LICENSE)
