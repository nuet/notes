
## ajax 使用promise例子
~~~javascript
getData(method, url){
  var promise = new Promise(function(resolve, reject){
    var xmlHttp = new XMLHttpRequest();
    xmlHttp.open(method, url);
    xmlHttp.send();
    xmlHttp.onload = function () {
      if (this.status == 200 ) {
        resolve(this.response);
      } else {
        reject(this.statusText);
      }
    };
    xmlHttp.onerror = function () {
      reject(this.statusText);
    };
  })
  return promise;
}

getData('get','www.xxx.com').then(successFun, failFun)
~~~

~~~javascript
new Promise(function(resolve, reject){
    resolve(5)
}).then(function(value){
    taskA()
}).then(function(value){
    taskB()
}).then(function(value){
    taskC()
}).catch(function(reason){
    console.log(reason)
})
~~~

### Promise.all 数组都执行完才返回 一个reject则reject但是其他Promise还是会执行
~~~javascript
function timeout(time) {
    return new Promise(function (resolve) {
        setTimeout(function () {
            resolve(time);
        }, time);
    });
}
console.time('promise')
Promise.all([
    timeout(10),
    timeout(60),
    timeout(100)
]).then(function (values) {
    console.log(values); [10, 60, 100]
    console.timeEnd('promise');   // 107ms
});
~~~

### Promise.race 数组中有一个对象resolve或reject时，就改变自身的状态，并执行响应的回调但其他Promise也会执行
~~~javascript
function timeout(time) {
    return new Promise(function (resolve) {
        setTimeout(function () {
            console.log(time)
            resolve(time);
        }, time);
    });
}
console.time('promise')
Promise.race([
    timeout(10),
    timeout(60),
    timeout(100)
]).then(function (values) {
    console.log(values); [10, 60, 100]
    console.timeEnd('promise');   // 107ms
});

// 结果依次为
// 10
// 10
// promise: 11.1ms
// 60
// 100
~~~


### Promise 参考 https://segmentfault.com/a/1190000007598894#articleHeader4
~~~javascript
function start() {
  return new Promise((resolve, reject) => {
    resolve('start');
  });
}

start()
  .then(data => {
    // promise start
    console.log('result of start: ', data);
    return Promise.resolve(1); // p1
  })
  .then(data => {
    // promise p1
    console.log('result of p1: ', data);
    return Promise.reject(2); // p2
  })
  .then(data => {
    // promise p2
    console.log('result of p2: ', data);
    return Promise.resolve(3); // p3
  })
  .catch(ex => {
    // promise p3
    console.log('ex: ', ex);
    return Promise.resolve(4); // p4
  })
  .then(data => {
    // promise p4
    console.log('result of p4: ', data);
  });
  /* 结果
  result of start:  start
  result of p1:  1
  ex:  2
  result of p4:  4
  */
  ~~~
