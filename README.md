# Node.js with Datatables demo

I am using this project to learn node.js and how to build a development environment and bundle into a deployable package.  This package should have the following:

- Node JS is the server
- Datatables and Editor for CRUD operations
- JS based API for reading and writing to the DB
- Use of JSON Server for test data
- Sqlite and MySql DBs for production data
- Bootstrap for styling

<hr>
<h2>First step is to setup the development environment.</h2>

<h3>Webpack</h3>
Webpack 4 is a module bundler. Webpack takes modules with dependencies and generates static assets representing those modules.

```
npm install webpack webpack-dev-middleware --save-dev
```

- webpack (Webpack Compiler/Bundler) [NPM Link](https://www.npmjs.com/package/webpack)
- webpack-dev-middleware (Uses Webpack to compile assets in-memory and serve them) [NPM Link](https://www.npmjs.com/package/webpack-dev-middleware)

<h3>Babel</h3>

Babel 7 will be used for transpiling the code.  This allows for use of Javascript ES6 enhancements and Node modules.  Babel will "transpile" them to ES5 code for compatibility with older browsers.  For example Babel will take a `const` variables carefully scoped `var` variables, template stings will be converted to string concatenation, etc.

```
npm install @babel/cli @babel/core @babel/node @babel/preset-env @babel/register --save-dev
```

- @babel/core (Babel Transpiler) [NPM Link](https://www.npmjs.com/package/@babel/core)
- @babel/cli (CLI that communicates with Babel Transpiler) [NPM Link](https://www.npmjs.com/package/@babel/cli)
- @babel/node (babel-node is a CLI that works exactly the same as the Node.js CLI, with the added benefit of compiling with Babel presets and plugins before running it.) [NPM Link](https://www.npmjs.com/package/@babel/node)
- @babel/preset-env (Transpiles files using ES6, ES7, and ES8. The same as babel-preset-latest, which includes babel-preset-es2015, babel-preset-es2016, and babel-preset-es2017. However, babel-preset-latest is deprecated and replaced by babel-preset-env) [NPM Link](https://www.npmjs.com/package/@babel/preset-env)
- @babel/register (All subsequent files required by node with the extensions .es6, .es, .jsx and .js will be transformed by Babel) [NPM Link](https://www.npmjs.com/package/@babel/register)


<h3>JS/JSX & CSS Loaders</h3>

```
npm install babel-loader style-loader css-loader --save-dev
```

- babel-loader (Loads the files to Webpack for Babel to transpile) [NPM Link](https://www.npmjs.com/package/babel-loader)
- style-loader (Add exports of a module as style to DOM. Necessary when using css-loader, sass-loader, or less-loader) [NPM Link](https://www.npmjs.com/package/style-loader)
- css-loader (Loads CSS file with resolved imports and returns CSS code) [NPM Link](https://www.npmjs.com/package/css-loader)
