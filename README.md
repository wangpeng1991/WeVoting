
# WeVoting

A voting APP. [View online](https://we-voting-ele.herokuapp.com/)

具体功能为：

+ 对于已经授权用户可以：
  + 新建一个 poll，可自定义其中的选项
  + 存储发起的 polls，下次登陆仍旧可以看到自己发起的 polls 集合
  + 看到应用中所有用户创建的 polls 的实时投票结果 （用图表展示）
  + 向所有 polls 投票（每个 poll 每个用户号只能投一票）.
  + 可分享 poll (poll 详情页支持外部 landing)

+ 非授权用户只能：
  + 看到应用中所有用户创建的 polls 的实时投票结果 （用图表展示）

To do list:

+ Unit test
+ Wechat login (???)
+ List page data pagination;

## Techstack overview

#### Server:

+ 环境：Node
+ 框架：Express
+ 工具：Request
+ 模版引擎：Ejs
+ DataBase: Mongodb

#### Front-end:

+ 语言标准：ECMAScript 6
+ 框架: React + ReactDOM + React-Router
+ 模块化：ES6 module
+ 编译构建：Webpack + Babel
+ 插件： `react-d3-components`

## Setup

+ Install node.js [Ubuntu/Mac](https://github.com/creationix/nvm) , [Windows](https://nodejs.org/en/download/)

+ Clone this project
	```
	git clone https://github.com/elevenBeans/WeVoting.git
	cd WeVoting
	```
+ Install local dependencies
	```
	npm install
	```

## Development mode

Run `./start.sh`

Or

Run `export NODE_ENV=dev-HMR && ./start.sh` (enable HMR).


## Production mode

Run `export NODE_ENV=production && ./start.sh`.

## Directories

```
|-- client // front-end code
  |-- components // front-end components
    |-- footer.jsx // public footer
    |-- header.jsx // public header
    |-- loading.jsx // loading amination
    |-- spning.jsx // spning amination
  |-- lib // front-end library
    |-- utils.jsx
  |-- detail.jsx // detail page
  |-- home.jsx // home page
  |-- index.jsx // front-end intrance
  |-- list.jsx  // list page
  |-- new.jsx // new page
|-- controller // server-end controller
  |-- routes
    |-- api.js // api controller
    |-- login.js // login routes
    |-- view.js // view routes
  |-- DBhandler.js // DataBase CRUD
|-- dist // compiled front-end code
  |-- vendor
    |-- react-dom.min.js // react-dom production version
    |-- react.min.js // react production version
  |-- loading.css
  |-- router.bundle.js // bundled react-router
  |-- vote.bundle.js // bundled voteApp JS file
|-- views // server-end views
  |-- error.ejs
  |-- footer.ejs
  |-- header.ejs
  |-- index.ejs
|-- .gitignore
|-- Procfile // heroku file
|-- README.md
|-- index.js // app intrance file
|-- package.json
|-- serverConfig.js // enviroment configuration
|-- start.sh // start file for mac
|-- webpack.config.js
```
## Pages

+ home page
   + router: `/`
   + example: `https://we-voting-ele.herokuapp.com/`
+ list page
   + router: `/list(/:name)`
   + example: `https://we-voting-ele.herokuapp.com/list`

+ detail page
   + router: `/detail(/:id)`
   + example: `https://we-voting-ele.herokuapp.com/detail/1494908221812`

+ new page
   + router: `/new`
   + example: `https://we-voting-ele.herokuapp.com/new`

## LICENSE

[MIT](https://mit-license.org/)
