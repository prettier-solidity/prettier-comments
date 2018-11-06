# prettier-comments

> Copypaste from: [https://github.com/prettier/prettier/blob/master/src/language-js/comments.js](https://github.com/prettier/prettier/blob/master/src/language-js/comments.js)

## How to use it w/ `prettier-plugin-solidity`

```bash
➜  prettier-comments git:(master) ✗ yarn link
yarn link v1.9.4
success Registered "prettier-comments".
info You can now run `yarn link "prettier-comments"` in the projects where you want to use this package and it will be used instead.
✨  Done in 0.07s.
➜  prettier-comments git:(master) ✗
```

```bash
➜  prettier-plugin-solidity git:(prettier-comments) ✗ yarn link "prettier-comments"
yarn link v1.9.4
success Using linked package for "prettier-comments".
✨  Done in 0.07s.
➜  prettier-plugin-solidity git:(prettier-comments) ✗ AST_COMPARE=true yarn test
yarn run v1.9.4
$ jest
 PASS  tests/IndexOf/jsfmt.spec.js
 PASS  tests/SplittableCommodity/jsfmt.spec.js
 PASS  tests/Etc/jsfmt.spec.js
 PASS  tests/Ownable/jsfmt.spec.js
 PASS  tests/BasicIterator/jsfmt.spec.js
 PASS  tests/strings/jsfmt.spec.js
 PASS  tests/SimpleAuction/jsfmt.spec.js
 PASS  tests/SampleCrowdsale/jsfmt.spec.js
 PASS  tests/Inbox/jsfmt.spec.js
 PASS  tests/SimpleStorage/jsfmt.spec.js
------------|----------|----------|----------|----------|-------------------|
File        |  % Stmts | % Branch |  % Funcs |  % Lines | Uncovered Line #s |
------------|----------|----------|----------|----------|-------------------|
All files   |    85.44 |    81.03 |    95.24 |    85.44 |                   |
 clean.js   |      100 |      100 |      100 |      100 |                   |
 index.js   |    93.75 |    83.33 |      100 |    93.75 |                38 |
 loc.js     |    88.89 |       75 |      100 |    88.89 |                10 |
 parser.js  |      100 |       75 |      100 |      100 |                14 |
 printer.js |    83.03 |    81.25 |    92.31 |    83.03 |... 68,470,472,513 |
------------|----------|----------|----------|----------|-------------------|

Test Suites: 10 passed, 10 total
Tests:       20 passed, 20 total
Snapshots:   10 passed, 10 total
Time:        3.654s
Ran all test suites.
✨  Done in 4.36s.
➜  prettier-plugin-solidity git:(prettier-comments) ✗
```
