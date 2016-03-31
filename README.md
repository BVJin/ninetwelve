# ^O^

##Getting started

###Install webpack
#### `npm i webpack -S`

###Update config file
####
```
var webpack = require('webpack');
var path = require('path');

var BUILD_DIR = path.resolve(__dirname, 'src/client/public');
var APP_DIR = path.resolve(__dirname, 'src/client/app');

var config = {
  entry: APP_DIR + '/index.jsx',
  output: {
    path: BUILD_DIR,
    filename: 'bundle.js'
  }
};

module.exports = config;
```

###Setting Up Babel-Loader
####`npm i babel-loader babel-preset-es2015 babel-preset-react -S`
####`touch .babelrc`
```
{
  "presets" : ["es2015", "react"]
}
```

###Update webpack config.js
####
```
// Existing Code ....
var config = {
  // Existing Code ....
  module : {
    loaders : [
      {
        test : /\.jsx?/,
        include : APP_DIR,
        loader : 'babel'
      }
    ]
  }
}
```

###Install React.js
####```npm i react react-dom -S```


###Watch changes
####`./node_modules/.bin/webpack -d`

#### ^O^
