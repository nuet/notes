

[从 BEM 谈大型项目中 CSS 的组织和管理]
(https://www.ibm.com/developerworks/cn/web/1512_chengfu_bem/)(将了几种BEM，OOCSS，SMACSS，ACSS)

BEM
OOCSS bootstrap
SMACSS
ACSS


BEM  适合组件和模块化使用
BEM  好处是避免CSS命名冲突， 方便样式覆盖
组件规范
1. 组件应该是“自洽的”，其本身就应该构成了一个“生态圈”，也就是说，他几乎不需要外部供给，自给自足就能够运转下去
2. 透过 CSS class 来作为 Javascript 选取 DOM 节点的方式，就是 Javascript Hook。用 jQuery 可以常常看到这样的写法：$('.nav--main a')，
    可是当 CSS 跟 Javascript 搅在一起反而造成两边维护上的不便，当改了 CSS 时 Javascript 也要跟著改。
    所以用 HTML 的属性去选取 DOM 节点会更好，如果非要用 CSS 的 class 那也可以多写一个 js- 的 prefix，以表示这个节点有被 Javascript 使用
    HTML 里两个 class 之间用两个空格，会比一个空格看起来好阅读 <li class="nav--main  js-nav--main"><a>.........</a></li>
    JS用的旋转器最好分开,用data-js-myselector
禁止事项
1. BEM禁止使用子代选择器

### 块作用

### 元素作用

### 修饰符作用
  修饰符用来定义块或元素的外观和行为
  菜单块中的菜单项可以有选中或非选中的状态

[]
(http://blog.lxjwlt.com/front-end/2015/10/08/why-bem.html)(这个说的不错)
block-name__element-name--modifier-name  这个是标准BEM命名
blockName-elementName--modifierName  驼峰式
block-name_element-name--modifierName  单下划线
blockName__elementName-modifierName  修饰器名用单横线连接
块名__元素名--修饰器名
项目中每个块名都是唯一的, 元素都带上快名, 这样就避免冲突

## 自选器缺点  
1. 下面.list样式名很容易和其他模块冲突
2. 层次关系过长，逻辑不清晰，非常不利于维护 例: .page-btn ul li a {}
[引用](http://blog.lxjwlt.com/front-end/2015/10/08/why-bem.html)
~~~html
  <div class="page-btn">
     <!-- ... -->
     <ul class="list"></ul>
     <!-- ... -->
  </div>

  <style>
    .page-btn { /* ... */ }
    .page-btn .list { /* ... */ }
  </style>
~~~
~~~html
  <style>
  .button {
  	display: inline-block;
  	border-radius: 3px;
  	padding: 7px 12px;
  	border: 1px solid #D5D5D5;
  	background-image: linear-gradient(#EEE, #DDD);
  	font: 700 13px/18px Helvetica, arial;
  }
  .button--state-success {
  	color: #FFF;
  	background: #569E3D linear-gradient(#79D858, #569E3D) repeat-x;
  	border-color: #4A993E;
  }
  .button--state-danger {
  	color: #900;
  }
  </style>
  <button class="button">
  	Normal button
  </button>
  <button class="button button--state-success">
  	Success button
  </button>
  <button class="button button--state-danger">
  	Danger button
  </button>
~~~

~~~html
  <style>
    .menu {
     list-style: none;
    }
    .menu__item {
     font-weight: bold;
    }
    .menu__item--selected {
     color: red;
    }
    /**/
    .menu {
     list-style: none;
     &__item {
       font-weight: bold;
       &--selected {
         color: red;
       }
     }
    }
  </style>

  <ul class="menu">
    <li class="menu__item menu__item--selected">Menu Item 1</li>
    <li class="menu__item">Menu Item 2</li>
    <li class="menu__item">Menu Item 3</li>
  </ul>
~~~

~~~css
  .block {}
  .block__element {}
  .block--modifier {}
  /*
  .block 代表了更高级别的抽象或组件。
  .block__element 代表.block的后代，用于形成一个完整的.block的整体。
  .block--modifier代表.block的不同状态或不同版本。
  */

  .site-search {} /* 块 */
  .site-search__field {} /* 元素 */
  .site-search--full {} /* 修饰符 */
~~~

## 原子类缺点
1. 依赖了原子类，不方便组件移植，如使用了bootstrap的原子类就要依赖整个bootstrap, 原子类也有可能会冲突
