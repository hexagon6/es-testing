# ECMAScript 6+ testing setup

# babel-preset-env
- [preset-env](http://babeljs.io/docs/plugins/preset-env)

# enabled transforms
- [object-rest-spread](https://babeljs.io/docs/plugins/transform-object-rest-spread/)

# How to install

Install `degit` globally if you don't have it yet: `npm i -g degit`

Check out the latest commit of this repository:

1. `degit https://github.com/hexagon6/es-testing.git my-projectfolder`
2. `npm install` or `yarn`

# How to run tests

`npm test` or `yarn test`

# Watch mode

`npm test -w` or `yarn test`

# Folder structure

```
.
├── src
│   └── index.js        <- implementation
├── test
│   └── index.test.js   <- tests
```

Enjoy!
