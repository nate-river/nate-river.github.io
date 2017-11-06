---
layout: post
title:  "webpack react 配置"
tags:
categories:
---

`package.json`

```json
{
  "name": "",
  "version": "1.0.0",
  "main": "",
  "license": "MIT",
  "dependencies": {
    "babel-core": "^6.18.2",
    "babel-loader": "^6.2.8",
    "babel-preset-es2015": "^6.18.0",
    "babel-preset-react": "^6.16.0",
    "body-parser": "^1.15.2",
    "react": "^15.4.1",
    "react-dom": "^15.4.1",
    "react-redux": "^4.4.6",
    "redux": "^3.6.0",
    "webpack": "^1.14.0"
  }
}
```

`webpack.config.js`

```javascript
const webpack = require('webpack');
module.exports = {
  entry: {
    login: './dev/login.jsx',
    register: './dev/register.jsx',
    admin: './dev/admin.jsx'
  },
  output: {
    path: './static/js/admin/',
    filename: '[name].js'
  },
  module: {
    loaders: [{
      test: /\.js[x]?$/,
      exclude: /node_modules/,
      loader: 'babel-loader?presets[]=es2015&presets[]=react'
    }]
  },
  plugins: [
    // new webpack.DefinePlugin({
    //   'process.env': {
    //     'NODE_ENV': JSON.stringify('production')
    //   }
    // }),
    // new webpack.optimize.UglifyJsPlugin({
    //   compress: {
    //     warnings: true
    //   }
    // })
    // new webpack.SourceMapDevToolPlugin({
    //   // Match assets just like for loaders.
    //   test: string | RegExp | Array,
    //   include: string | RegExp | Array,
    //
    //   // `exclude` matches file names, not package names!
    //   exclude: string | RegExp | Array,
    //
    //   // If filename is set, output to this file.
    //   // See `sourceMapFileName`.
    //   filename: string,
    //
    //   // This line is appended to the original asset processed. For
    //   // instance '[url]' would get replaced with an url to the
    //   // sourcemap.
    //   append: false | string,
    //
    //   // See `devtoolModuleFilenameTemplate` for specifics.
    //   moduleFilenameTemplate: string,
    //   fallbackModuleFilenameTemplate: string,
    //
    //   module: bool, // If false, separate sourcemaps aren't generated.
    //   columns: bool, // If false, column mappings are ignored.
    //
    //   // Use simpler line to line mappings for the matched modules.
    //   lineToLine: bool | {test, include, exclude}
    // })
  ]
};
```
