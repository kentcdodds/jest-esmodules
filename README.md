# Using Jest with native ESModules

This is a minimal repo that uses native ES modules and works with jest

1. `package.json` specifies this package as a `module` type.
2. `jest.config.js` disables the built-in babel transform with `transform: {}`.
   Note that this is not actually required for the tests to work, but it is if
   you want the ESModules to be executed as coded rather than being transformed.
3. `package.json`'s `test` script runs jest via `node` with the
   `--experimental-vm-modules` flag. Hopefully this won't be required in the
   long-term when this required feature is no longer experimental.

[Learn more](https://jestjs.io/docs/ecmascript-modules)
