# conventional-changelog-jquery

[![ESM-only package][package]][package-url]
[![NPM version][npm]][npm-url]
[![Node version][node]][node-url]
[![Dependencies status][deps]][deps-url]
[![Install size][size]][size-url]
[![Build status][build]][build-url]
[![Coverage status][coverage]][coverage-url]

[package]: https://img.shields.io/badge/package-ESM--only-ffe536.svg
[package-url]: https://nodejs.org/api/esm.html

[npm]: https://img.shields.io/npm/v/conventional-changelog-jquery.svg
[npm-url]: https://npmjs.com/package/conventional-changelog-jquery

[node]: https://img.shields.io/node/v/conventional-changelog-jquery.svg
[node-url]: https://nodejs.org

[deps]: https://img.shields.io/librariesio/release/npm/conventional-changelog-jquery
[deps-url]: https://libraries.io/npm/conventional-changelog-jquery/tree

[size]: https://packagephobia.com/badge?p=conventional-changelog-jquery
[size-url]: https://packagephobia.com/result?p=conventional-changelog-jquery

[build]: https://img.shields.io/github/actions/workflow/status/nholuongut/conventional-changelog/tests.yaml?branch=master
[build-url]: https://github.com/nholuongut/conventional-changelog/actions

[coverage]: https://coveralls.io/repos/github/nholuongut/conventional-changelog/badge.svg?branch=master
[coverage-url]: https://coveralls.io/github/nholuongut/conventional-changelog?branch=master

[conventional-changelog](https://github.com/nholuongut/conventional-changelog) [jQuery](https://github.com/jquery/jquery) preset.

**Issues with the convention itself should be reported on the JQuery issue tracker.**

## Install

```bash
# yarn
yarn add -D conventional-changelog-jquery
# pnpm
pnpm add -D conventional-changelog-jquery
# npm
npm i -D conventional-changelog-jquery
```

## JQuery Convention

Commit messages should describe what changed, and reference the issue number if the commit closes or is associated with a particular issue. Commit messages for all jQuery projects should look like this:

```
Component: Short Description

Optional Long Description

Fixes #xxx
Closes gh-yyy
Ref #zzz
```

Every commit must have a subject (the first line). Everything else is optional.

### Subject

This is the first line. It consists of a component, like "Event" or "Autocomplete".

### Long description

There are two line breaks between the subject and the long description. The description can have any length and formatting, like lists.

### References

References to issues or pull requests go after the long description, each one on their own line.

* Use **Fixes** when the commit fixes an open issue.

* Use **Closes** when the commit closes an open pull request.

* Use **Ref** when referencing an issue or pull request that is already closed or should remain open. Examples include partial fixes and commits that add a test but not a fix.

* Always use "gh-xxx" for GitHub issues and pull requests within the same repository. Use "\[user\]/\[repo\]#xxx" when referencing an issue or pull request in another repository, e.g., "Closes jquery/jquery-ui#175".

Based on https://github.com/jquery/contribute.jquery.org/blob/master/pages/commits-and-pull-requests.md#commit-guidelines
