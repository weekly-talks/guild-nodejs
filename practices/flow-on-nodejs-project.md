# Why I need Flow on Node.js project?

- because type checking highlight type errors on static check, which otherwise would be runtime errors

## Why Flow it IDE does type checking on code annotated with JSDoc?

Good question! JSDoc plus IDE could be enough for some projects. But in case, could that IDE do type inference? Flow could.

# How to use Flow on Node.js projects

Unfortunatelly by using Flow, we add new syntax constructs to the JavaScript code, which means that Node.js would fail to parse that code.

The only way to run Flow-annotated code is to use Babel with transformation which strips Flow annotations.

- https://babeljs.io/docs/plugins/preset-flow/

```
npm install --save-dev babel-preset-flow
# configure Babel to use `flow` preset, e.g. using `.babelrc` file
babel-node example.js
```
