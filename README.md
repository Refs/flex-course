
# Flex layout


## 解释 display :  flex | inline-flex;

### css formatting context

当我们使用 display: flex | inline-flex;  实际上我们就生成了 一个 css 格式化上下文； css 常见有以下四种 格式化 上下文

1. BFC block formatting context  -- display: block;

2. IFC inline formatting context -- display: inline;

3. GFC grid formatting context -- display: grid;

4. FFC flex formatting context  -- display: flex;

### display: block 与 display: flex 异同 （BFC versus FFC）
> 两者对给定的一种 格式化 环境，而 处于 环境内的 元素 的布局 会受到环境的影响；

1. BFC: 
  * 内部盒子垂直放置, 宽度默认会撑满父盒子；
  * 相临盒子的 margin 会塌陷合并；
  * 脱离文档流的盒子不会与文档流内的盒子重叠 (float: left; position: absolute | fixed)
  * 浮动的盒子会被计算在容器高度内；

2. FFC
  * 内部盒子 flex items 从左到右水平排列；cross axis 方向 会撑满 flex container;
  * 相邻 flex items 之间margin 不会合并；
  * float 属性 不再起作用；因为 float, vertical-align, clear 都是为 BFC 专门设计的；


### Flex Layout Box Model
格式化上下文是一个很抽象的概念，我们希望能利用一个盒子，将其具象化，这个盒子就是 flex layout box model;



### 盒子中的对象，



### display: flex 与 display: inline-flex 的区别




## the difference between flex and inline-flex

> https://stackoverflow.com/questions/27418104/difference-between-displayinline-flex-and-displayflex

## difference between align-items and align-content

> https://stackoverflow.com/questions/24313271/display-property-differences-for-inline-something

## justify-content and align-items

> the first just for main axis , another is just for cross axis; 

