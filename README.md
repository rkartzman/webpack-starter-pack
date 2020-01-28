# webpack-starter-pack
starter pack for webpack and babel config

## Babel packages

`# babel basics` npm i -D @babel/core @babel/cli @babel/node @babel/register 
`# babel plugins` npm i -D @babel/preset-env @babel/plugin-proposal-class-properties @babel/plugin-proposal-optional-chaining @babel/plugin-proposal-decorators @babel/plugin-proposal-function-bind @babel/plugin-syntax-export-default-from @babel/plugin-syntax-dynamic-import @babel/plugin-transform-runtime
`# babel runtime` npm i -S core-js@3 @babel/runtime


## Babel config for webpack config
"plugins": [
    [
      "@babel/plugin-proposal-class-properties",
      {
        "loose": true
      }
    ],
    "@babel/plugin-proposal-optional-chaining",
    [
      "@babel/plugin-proposal-decorators",
      {
        "legacy": true
      }
    ],
    "@babel/plugin-proposal-function-bind",
    "@babel/plugin-syntax-export-default-from",
    "@babel/plugin-syntax-dynamic-import",
]

## Dev server config for webpack config 
devServer: {
      contentBase: [
        projectRoot
      ],
      quiet: false,
      //host: '0.0.0.0', // use this if you want to test on mobile
      // host:
      hot: true,
      port: 3030,
      // publicPath: outputFolder,
      writeToDisk: true,  // need this for the VSCode<->Chrome debug extension to work
      // filename: outFile,
    },
