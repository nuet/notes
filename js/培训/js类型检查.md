// 检测"String"
if (typeof name === "string") {
    anotherName = name.substring(3);
}

// 检测"Number"
if (typeof count === "number") {
    updateCount(count);
}

// 检测"Boolean"
if (typeof found === "boolean" && found) {
    message("Found!");
}

// 检测"Undefined"
if (typeof MyApp === "undefined") {
    MyApp = {
        // 其他代码
    };
}

// 这个注意
console.log(typeof null);   // "object"
var a = null;
if(a === null) {
    console.log('a is null');
}
console.log(typeof {});             // "object"
console.log(typeof []);             // "object"
console.log(typeof new Date());     // "object"
console.log(typeof new RegExp());   // "object"


// 检测引用值=============================
// instanceof的一个有意思的特性是它不仅检测构造这个对象的构造器，还检测原型链。原型链包含了很多信息，包括定义对象所采用的继承模式。
// 比如，默认情况下，每个对象都继承自Object，因此每个对象的value instanceof Object都会返回ture
// 检测日期
if (value instanceof Date) {
    console.log(value.getFullYear);
}

// 检测 Error
if (value instanceof Error) {
    throw value;
}

// 检测正则表达式
if (value instanceof RegExp) {
    if (value.test(anotherValue)) {
        console.log("Matches");
    }
}

// 判断函数
console.log(myFunc instanceof Function); // true 不好, iframe每个有自己的Function构造函数
console.log(typeof myFunc === "function"); // true 判断函数

// 判断数组, 每个iframe都有各自的Array构造函数
function isArray(value) {
    if (typeof Array.isArray === "function") {
        return Array.isArray(value); //ES5 规范
    } else {
        return Object.prototype.toString.call(value) === "[object Array]";
    }
}
// IE 9+、FireFox 4+、Safari 5+、Opera 10.5+、Chrome 都实现了Array.isArray()方法。

// 检测属性
// hasOwnProperty() 方法用来判断某个对象是否含有指定的自身属性。 不能是原型链上
// "prop" in object  可以判断原型链上的



