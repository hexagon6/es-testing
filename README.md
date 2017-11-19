# ECMAScript 6+ testing setup for node

This project allows you to quickly start coding with ECMAScript 6+ in node with tests from the beginnning

## How to install

Install `degit` globally if you don't have it yet: `npm i -g degit`

Check out the latest commit of this repository and install dependencies:

1. `degit https://github.com/hexagon6/es-testing.git my-projectfolder`
2. `npm install` or `yarn`

## How to run tests

`npm test` or `yarn test`

## Watch mode

`npm test -w` or `yarn test -w`

This command
 runs tests on each save of a file and
 let's you focus on your code.

## Folder structure

```
├── src
│   └── index.js        <- implementation
├── test
│   └── index.test.js   <- tests
```

## Test runner

[ava](https://www.npmjs.com/package/ava)

## Transpilation setup with babel for new ES features

babel-preset-env
- [preset-env](http://babeljs.io/docs/plugins/preset-env)

enabled transforms
- [object-rest-spread](https://babeljs.io/docs/plugins/transform-object-rest-spread/)

You are free to extend the transform options in package.json at key `babel` (no need for .babelrc file to keep project configuration neatly packed)

```
$ jq '.babel' package.json
{
  "plugins": [
    "transform-object-rest-spread"
  ],
  "presets": [
    [
      "env",
      {
        "targets": {
          "node": "current"
        }
      }
    ],
    "@ava/stage-4"
  ]
}
```

Enjoy!
