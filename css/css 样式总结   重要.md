
填充空格
.space {
  width: 1em;
  display: inline-block;
}


固定到顶部
sticky：(这是css3新增的属性值)粘性定位，官方的介绍比较简单，或许你不能理解。其实，它就相当于relative和fixed混合。最初会被当作是relative，相对于原来的位置进行偏移；一旦超过一定阈值之后，会被当成fixed定位，相对于视口进行定位
nav {
  position: sticky;
  top: 80px;
}
[demo](https://jsbin.com/xagijemodo/edit?html,css,output)
