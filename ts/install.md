

[参考]
(https://www.tslang.cn/docs/handbook/react-&-webpack.html)

[TypeScript + React环境构建和demo]
(http://blog.csdn.net/cithegod/article/details/76173267)(create-react-app)(能typescript)

[ts 编译选项]
(https://tslang.cn/docs/handbook/compiler-options.html)


npm i typescript -S

./node_modules/.bin/tsc --init   生成tsconfig.json

npm i ts-loader -D

// .ts(x) 文件应该首先经过 Typescript loader 的处理, 然后是 babel 的处理
      { test: /\.tsx?$/, loaders: ['babel-loader', 'ts-loader'], include: path.resolve('src') }

npm i @types/react @types/react-dom -S
npm i @types/react-router @types/redux @types/react-redux -S

npm i -S redux react-redux @types/react-redux
