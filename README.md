# Node.js with Datatables demo

I am using this project to learn node.js and how to build a development environment and bundle into a deployable package.  This package should have the following:

- Node JS is the server
- Datatables and Editor for CRUD operations
- JS based API for reading and writing to the DB
- Use of JSON Server for test data
- Sqlite and MySql DBs for production data
- Bootstrap for styling

<hr>
<h2>First is to setup the development environment.</h2>

<h3>Webpack</h3>
Webpack 4 is a module bundler. Webpack takes modules with dependencies and generates static assets representing those modules.

```
npm install webpack webpack-dev-middleware --save-dev
```

- webpack (Webpack Compiler/Bundler) [NPM Link](https://www.npmjs.com/package/webpack)
- webpack-dev-middleware (Uses Webpack to compile assets in-memory and serve them) [NPM Link](https://www.npmjs.com/package/webpack-dev-middleware)

<h3>Babel</h3>

Babel 7 will be used for transpiling the code.  This allows for use of Javascript ES6 enhancements and Node modules.  Babel will "transpile" them to ES5 code for compatibility with older browsers.  For example Babel will take a `const` variables carefully scoped `var` variables, template stings will be converted to string concatenation, etc.
