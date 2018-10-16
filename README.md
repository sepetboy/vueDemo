# y

> y

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

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## 添加sass依赖
``` bash
npm install --save-dev sass-loader
# sass-loader依赖于node-sass
npm install --save-dev node-sass

# 在build文件夹下的webpack.base.conf.js的rules里面添加配置
{
  test: /\.sass$/,
  loaders: ['style', 'css', 'sass']
}
# 在使用scss编写样式的vue文件中，在其style标签上添加lang="scss"，如<style lang="scss">
# 在webpack.base.conf.js文件中resolve下面为.scss文件的路径起一个别名，'styles': resolve('src/assets')
```
## 添加Iconfont矢量图标
``` bash
1.将心仪的图标放入购物车
2.点击购物车按钮，将图标添加至项目
3.进入项目，将图标下载到本地
4.将文件iconfont.eot、iconfont.svg、iconfont.ttf、iconfont.woff、iconfont.css拷到vue项目的assets文件夹中
5.修改iconfont.css文件中引用四个字体文件的路径
6.在main.js中导入iconfont.css文件，import '@/assets/iconfont.css'
```
