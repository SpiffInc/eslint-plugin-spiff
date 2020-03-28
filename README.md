
This is a trial of [GitHub Repository Template](https://github.blog/2019-06-06-generate-new-repositories-with-repository-templates/).

Please update `package.json` after you created new repository with this template.

**File Structure**:

- `docs/rules/` is the directory to put documentation.
- `lib/rules/` is the directory to put rule definitions.
- `scripts/` is the directory to put development scripts.
- `tests/lib/` is the directory to put tests for `lib/`.
- `.eslintignore` and `.eslintrc.js` are the configuration to lint this repository.

**Dependencies**:

This template uses [mocha](https://www.npmjs.com/package/mocha), [nyc](https://www.npmjs.com/package/nyc), and [Travis CI](https://travis-ci.com/) for tests, as same as ESLint itself. If you want to use other tools, customize it.

**Development Tools**:

- `npm run add-rule foo` command adds a rule definition.
- `npm version` command updates the following stuff by the `meta` property of rules:
    - the header of `docs/rules/*.md`.
    - `lib/configs/recommended.js` file.
    - `lib/index.js` file.
    - the rule table in `README.md` file.

Below is an example of README.

----

# eslint-plugin-spiff (template)

<!--
[![npm version](https://img.shields.io/npm/v/eslint-plugin-spiff.svg)](https://www.npmjs.com/package/eslint-plugin-spiff)
[![Downloads/month](https://img.shields.io/npm/dm/eslint-plugin-spiff.svg)](http://www.npmtrends.com/eslint-plugin-spiff)
[![Build Status](https://travis-ci.org/mysticatea/eslint-plugin-spiff.svg?branch=master)](https://travis-ci.org/mysticatea/eslint-plugin-spiff)
[![Coverage Status](https://codecov.io/gh/mysticatea/eslint-plugin-spiff/branch/master/graph/badge.svg)](https://codecov.io/gh/mysticatea/eslint-plugin-spiff)
[![Dependency Status](https://david-dm.org/mysticatea/eslint-plugin-spiff.svg)](https://david-dm.org/mysticatea/eslint-plugin-spiff)
-->

A template for ESLint plugins.

## Installation

Use [npm](https://www.npmjs.com/) or a compatibility tool to install.

```
$ npm install --save-dev eslint eslint-plugin-spiff
```

### Requirements

- Node.js v8.10.0 or newer versions.
- ESLint v5.16.0 or newer versions.

## Usage

Write your config file such as `.eslintrc.yml`.

```yml
plugins:
  - spiff
rules:
  spiff/example-rule: error
```

See also [Configuring ESLint](https://eslint.org/docs/user-guide/configuring).

## Configs

- `spiff/recommended` ... enables the recommended rules.

## Rules

<!--RULE_TABLE_BEGIN-->
### Stylistic Issues

| Rule ID                                           | Description      |       |
| :------------------------------------------------ | :--------------- | :---: |
| [spiff/example-rule](./docs/rules/example-rule.md) | An example rule. |  ⭐️   |

<!--RULE_TABLE_END-->

## Semantic Versioning Policy

This plugin follows [Semantic Versioning](http://semver.org/) and [ESLint's Semantic Versioning Policy](https://github.com/eslint/eslint#semantic-versioning-policy).

## Changelog

- [GitHub Releases]()

## Contributing

Welcome your contribution!

See also [ESLint Contribution Guide](https://eslint.org/docs/developer-guide/contributing/).

### Development Tools

- `npm test` runs tests and measures coverage.
- `npm version <TYPE>` updates the package version. And it updates `lib/configs/recommended.js`, `lib/index.js`, and `README.md`'s rule table. See also [npm version CLI command](https://docs.npmjs.com/cli/version).
- `npm run add-rule <RULE_ID>` creates three files to add a new rule.