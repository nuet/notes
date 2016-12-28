
### 避免加载模块缓存
~~~javascript
delete require.cache[require.resolve('./server.js')];
app = require('./server.js');
~~~
