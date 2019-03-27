https://medium.com/@binyamin/creating-a-node-express-webpack-app-with-dev-and-prod-builds-a4962ce51334

For our Development build, we want to transpile it from ES6+, lint it, run unit tests on it, run coverage reports for it,
and to enable Hot Module Reloading (HMR) for an easier development experience. 

Express server file for dev and prod.
Webpack config files for Dev and Prod application code, and for the server too.

---------------------------------------------------------

Our Tech Stack

Express — server
Webpack 4 — bundling
Jest — testing
Babel — ES6+ transpilation: 
    ECMAScript 6 is also known as ES6 and ECMAScript 2015: Some people call it JavaScript 6.
ESlint — Linting
    The pluggable linting utility for JavaScript and JSX
JSX: Syntax extension to JavaScript: https://reactjs.org/docs/introducing-jsx.html
Webpack Dev Middleware — Bundle code in memory instead of in a file
Webpack Hot Middleware — Enables Hot Module Reloading (HMR)
UglifyJS — UglifyJS is a JavaScript parser, minifier, compressor and beautifier toolkit.
mini-css-extract-plugin — minifies CSS

---------------------------------------------------------

nmp init -y
npm start
npm install --save-dev webpack webpack-cli webpack-node-externals
npm install --save-dev @babel/core @babel/preset-env babel-loader
npm install html-loader
npm install html-webpack-plugin
npm install --save-dev css-loader file-loader style-loader
npm install --save-dev mini-css-extract-plugin uglifyjs-webpack-plugin optimize-css-assets-webpack-plugin
npm install --save-dev webpack-dev-middleware
npm install url-loader
npm install --save-dev webpack-hot-middleware
npm install --save-dev mini-css-extract-plugin uglifyjs-webpack-plugin optimize-css-assets-webpack-plugin
npm install --save-dev eslint babel-eslint eslint-loader eslint-plugin-react
npm run build
npm start