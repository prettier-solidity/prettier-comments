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
 PASS  tests/SimpleAuction/jsfmt.spec.js
 PASS  tests/SplittableCommodity/jsfmt.spec.js
 PASS  tests/Ownable/jsfmt.spec.js
 PASS  tests/IndexOf/jsfmt.spec.js
 PASS  tests/BasicIterator/jsfmt.spec.js
 PASS  tests/SampleCrowdsale/jsfmt.spec.js
 PASS  tests/SimpleStorage/jsfmt.spec.js
 PASS  tests/Inbox/jsfmt.spec.js
 FAIL  tests/Etc/jsfmt.spec.js
  ● Test suite failed to run

    TypeError: Cannot read property 'type' of undefined

      193 |
      194 | function addBlockOrNotComment(node, comment) {
    > 195 |   if (node.type === "BlockStatement") {
          |            ^
      196 |     addBlockStatementFirstComment(node, comment);
      197 |   } else {
      198 |     addLeadingComment(node, comment);

      at addBlockOrNotComment (../prettier-comments/src/language-js/comments.js:195:12)
      at handleIfStatementComments (../prettier-comments/src/language-js/comments.js:270:5)
      at handleOwnLineComment (../prettier-comments/src/language-js/comments.js:25:5)
      at node_modules/prettier/index.js:9586:11
          at Array.forEach (<anonymous>)
      at Object.attach (node_modules/prettier/index.js:9560:12)
      at attachComments (node_modules/prettier/index.js:10381:14)
      at coreFormat (node_modules/prettier/index.js:10411:21)
      at format (node_modules/prettier/index.js:10570:16)
      at formatWithCursor (node_modules/prettier/index.js:10582:12)

 PASS  tests/strings/jsfmt.spec.js
------------|----------|----------|----------|----------|-------------------|
File        |  % Stmts | % Branch |  % Funcs |  % Lines | Uncovered Line #s |
------------|----------|----------|----------|----------|-------------------|
All files   |    82.04 |    77.01 |    85.71 |    82.04 |                   |
 clean.js   |      100 |      100 |      100 |      100 |                   |
 index.js   |    93.75 |    83.33 |      100 |    93.75 |                38 |
 loc.js     |    88.89 |       75 |      100 |    88.89 |                10 |
 parser.js  |      100 |       75 |      100 |      100 |                14 |
 printer.js |    78.79 |    76.88 |    76.92 |    78.79 |... 95,498,509,513 |
------------|----------|----------|----------|----------|-------------------|

Test Suites: 1 failed, 9 passed, 10 total
Tests:       18 passed, 18 total
Snapshots:   9 passed, 9 total
Time:        3.906s
Ran all test suites.
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
➜  prettier-plugin-solidity git:(prettier-comments) ✗
```
