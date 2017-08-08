# 来源

https://github.com/taosin/alioss-js-upload

https://www.npmjs.com/package/vue-oss-upload

关键点实际上有以下几点：

* 不能直接采用require或import导入OSS，为什么？似乎是ali-oss中包含的fs，child_process的问题。解决方法是将js直接引入到index.html中
* 但这样又带来第二个问题，即编译时会报OSS undefined的错误。此时，需要在.eslintrc.js中增加
  
  `
  ...
  "globals": {
    "OSS": true
  },
  ...`

# alioss

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


