## tune-codemods

A [jscodeshift](https://github.com/facebook/jscodeshift) codemod library that we use at tune.
## Install & Run

```sh
npm install -g jscodeshift
git clone https://github.com/AlexJuarez/tune-codemods.git
jscodeshift -t ./transforms/prefer-const <file>
```

## Scripts

- `auto-unmock` adds jest.unmock for all imports/ requires inside of files.
- `chai-to-jasmine` converts chai chain and should expressions to jest compatible jasmine.
- `import-to-require` converts all import statements to require statements.
- `mocha-mix-to-enzyme` replaces mochaMix a tune testing library with enzyme matchers.
- `prefer-const` converts let statements that are never reassigned to const.
- `rm-empty-beforeEach` removes empty beforeEach blocks.
- `rm-unused-vars` removes variableDeclarations that are never used in the file.
- `sinon-to-jasmine-spy` converts all sinon type spys to jasmine and jest
- `sort-keys` sorts all of the keys in object in ascending order.
- `order-imports` sorts all the imports by rules laid out in [eslint-plugin-import/order](https://github.com/benmosher/eslint-plugin-import/blob/master/docs/rules/order.md)
- `global-return-to-export` replaces top level return statements with export default
