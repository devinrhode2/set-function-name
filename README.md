# set-function-name <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Set a function’s name.

## Usage

```javascript
var setFunctionName = require('set-function-name');
var assert = require('assert');

const obj = {
    concise() {},
    arrow: () => {},
    named: function named() {},
    anon: function () {},
};
assert.equal(obj.concise.name, 'concise');
assert.equal(obj.arrow.name, 'arrow');
assert.equal(obj.named.name, 'named');
assert.equal(obj.anon.name, 'anon');

setFunctionName(obj.concise, 'brief');
setFunctionName(obj.arrow, 'pointy');
setFunctionName(obj.named, '');
setFunctionName(obj.anon, 'anonymous');

assert.equal(obj.concise.name, 'brief');
assert.equal(obj.arrow.name, 'pointy');
assert.equal(obj.named.name, '');
assert.equal(obj.anon.name, 'anonymous');
```

[package-url]: https://npmjs.org/package/set-function-name
[npm-version-svg]: https://versionbadg.es/ljharb/set-function-name.svg
[deps-svg]: https://david-dm.org/ljharb/set-function-name.svg
[deps-url]: https://david-dm.org/ljharb/set-function-name
[dev-deps-svg]: https://david-dm.org/ljharb/set-function-name/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/set-function-name#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/set-function-name.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/set-function-name.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/set-function-name.svg
[downloads-url]: https://npm-stat.com/charts.html?package=set-function-name
[codecov-image]: https://codecov.io/gh/ljharb/set-function-name/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/set-function-name/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/set-function-name
[actions-url]: https://github.com/ljharb/set-function-name/actions
