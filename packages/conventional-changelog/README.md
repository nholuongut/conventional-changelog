#  [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url] [![Coverage Status][coverage-image]][coverage-url]

> Generate a changelog from git metadata


## Usage

You most likely only need to use this module if you're building a library that provides an abstraction on top of conventional commits,  See [Getting started](https://github.com/nholuongut/conventional-changelog#getting-started) if you're an end-user.

```sh
$ npm install --save conventional-changelog
```

```js
import conventionalChangelog from 'conventional-changelog';

conventionalChangelog({
  preset: 'angular'
})
  .pipe(process.stdout); // or any writable stream
```

Or if you want to use your own custom preset:

```js
import conventionalChangelog from 'conventional-changelog';
import config from '@org/conventional-changelog-custom-preset';

conventionalChangelog({config})
  .pipe(process.stdout); // or any writable stream
```

## API

### conventionalChangelog([options, [context, [gitRawCommitsOpts, [parserOpts, [writerOpts]]]]])

Returns a readable stream.

#### options

See the [conventional-changelog-core](https://github.com/nholuongut/conventional-changelog/tree/master/packages/conventional-changelog-core) docs. The API is the same with the following changes or additions:

##### preset

Type: `string` Possible values: `'angular', 'atom', 'codemirror', 'conventionalcommits', 'ember', 'eslint', 'express', 'jquery', 'jshint'`

It's recommended to use a preset so you don't have to define everything yourself. Presets are names of built-in `config`.

A scoped preset package such as `@scope/conventional-changelog-custom-preset` can be used by passing `@scope/custom-preset` to this option.

**NOTE:** `options.config` will be overwritten by the values of preset. You should use either `preset` or `config`, but not both.

## [Notes for parent modules](https://github.com/nholuongut/conventional-changelog-core#notes-for-parent-modules)

## License

MIT

[npm-image]: https://badge.fury.io/js/conventional-changelog.svg
[npm-url]: https://npmjs.org/package/conventional-changelog
[travis-image]: https://travis-ci.org/nholuongut/conventional-changelog.svg?branch=master
[travis-url]: https://travis-ci.org/nholuongut/conventional-changelog
[daviddm-image]: https://david-dm.org/nholuongut/conventional-changelog.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/nholuongut/conventional-changelog
[coverage-image]: https://coveralls.io/repos/github/nholuongut/conventional-changelog/badge.svg?branch=master
[coverage-url]: https://coveralls.io/github/nholuongut/conventional-changelog?branch=master
