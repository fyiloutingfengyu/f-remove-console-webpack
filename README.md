# f-remove-console-webpack

## Installation
```sh
npm install f-remove-console-webpack --save-dev
```

## Usage
```js
// webpack.config.js
const RemoveConsolePlugin = require('f-remove-console-webpack')

// demo1: remove console.log by default
module.exports = {
  // other code ...
  plugins: [
    new RemoveConsolePlugin()
  ]
}

// demo2: remove console.log, console.warn, console.error 
module.exports = {
  // other code ...
  plugins: [
    new RemoveConsolePlugin({ include: ['log', 'warn', 'error'] })
  ]
}

// demo3: remove console.*
module.exports = {
  // other code ...
  plugins: [
    new RemoveConsolePlugin({ include: ['*'] })
  ]
}
```


## Options
| option | description | default |
| ------ | ----------- | ------- |
| include | An array of console methods that you want to remove. | ['log']|
