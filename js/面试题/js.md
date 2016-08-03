

// 参考: https://segmentfault.com/a/1190000006129337
(function(x){
    delete x;
    return x; // 1  delete只能删除object的熟悉
})(1);


var y = 1, x = y = typeof x;
x; // "undefined"


(function f(f){
    // 这里的f是传入的参数function(){ return 1; }
    return typeof f();//"number"
})(function(){ return 1; });


var f = (function f(){ return '1'; }, function g(){ return 2; })();
typeof f;//"number"
// 这里f===g
// 逗号操作符 对它的每个操作对象求值（从左至右），然后返回最后一个操作对象的值


var x = 1;
if (function f(){}) {
    x += typeof f;
}
x;//"1undefined"
// function expression中的函数名f是不能在函数体外部访问的


var x = [typeof x, typeof y][1];
typeof typeof x;//"string"
// x === 'undefined' 这里x是一个字符串了

(function(foo){
    return typeof foo.bar;//"undefined"
})({ foo: { bar: 1 } });
// 注意 foo.foo.bar===1
// 这个题其实没啥意思， 考细心

(function f(){
    function f(){ return 1; }
    var v = 3;
    return [f(), v];//[2, 3]
    var v = 4;
    function f(){ return 2; }
})();
// 注意  函数定义作用域会提高到最前, 但是变量不行

function f(){ return f; }
new f() instanceof f;//false
// 返回对象为false 其它(1,'a')会是true
// 如果构造函数返回了一个“对象”，那么这个对象会取代整个new出来的结果。如果构造函数没有返回对象，那么new出来的结果为步骤1创建的对象
