# ObjectSpread support in acorn

[![Build Status](https://travis-ci.org/UXtemple/acorn-object-spread.svg?branch=master)](https://travis-ci.org/UXtemple/acorn-object-spread)
[![NPM version](https://img.shields.io/npm/v/acorn-object-spread.svg)](https://www.npmjs.org/package/acorn-object-spread)

**NOTE**: Object spread is now part of the core library, so you probably don't need this plugin anymore.

This is plugin for [Acorn](http://marijnhaverbeke.nl/acorn/) - a tiny, fast JavaScript parser, written completely in JavaScript.

## Usage

You can use this module directly in order to get Acorn instance with plugin installed:

```javascript
var acorn = require('acorn-object-spread');
```

Or you can use `inject.js` for injecting plugin into your own version of Acorn like this:

```javascript
var acorn = require('acorn-object-spread/inject')(require('./custom-acorn'));
```

Then, use the `plugins` option whenever you need to support objectSpread while parsing:

```javascript
var ast = acorn.parse(code, {
  plugins: { objectSpread: true }
});
```
## License

This plugin is issued under the [MIT license](./LICENSE).

With <3 by UXtemple.
