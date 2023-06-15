# ESLint Complexity of Code [![npm][npm_img]][npm_url] [![Checks ➜ Tests ➜ Publish][build_img]][build_url]

[ESLintCC][npm_url] is a ECMAScript/JavaScript/TypeScript tool
that computes complexity of code by using [ESLint][eslint_npm]

> ESLint calculates complexity of code,
> while this tool only collects a report based on his [complexity rule messages][eslint_rule]

## Installation and Usage

> Requirements, principles of local and global installation and usage
> are the same as [ESLint Installation and Usage][eslint_usage]

Globally:

    $ npm install -g eslintcc
    $ eslintcc yourfile.js

Locally:

    $ npm install eslintcc
    $ ./node_modules/.bin/eslintcc yourfile.js

NPX (you can do it without installing):

    $ npx eslintcc yourfile.js

Integration in JavaScript application ([see more...](#nodejs-api)):

```js
const { Complexity } = require('eslintcc');

const complexity = new Complexity();
const report = await complexity.lintFiles(['yourfile.js']);

console.log(JSON.stringify(report, null, '\t'));
```

**Note:** ESLintCC ignores all rules, specified in configuration files,
and uses to generate a report only [complexity rules][eslint_rule].

[see more about eslintcc...](https://github.com/eslintcc/eslintcc#readme)

[npm_img]: https://img.shields.io/npm/v/eslintcc.svg

[npm_url]: https://www.npmjs.com/package/eslintcc

[build_img]: https://github.com/eslintcc/eslintcc/actions/workflows/main.yml/badge.svg?branch=main

[build_url]: https://github.com/eslintcc/eslintcc/actions/workflows/main.yml?query=branch:main

[eslint_npm]: https://www.npmjs.com/package/eslint

[eslint_rule]: https://eslint.org/docs/rules/complexity

[eslint_usage]: https://github.com/eslint/eslint#installation-and-usage
