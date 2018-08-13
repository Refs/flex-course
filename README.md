
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
  * 内部的盒子会垂直放置，宽度会撑满父盒子；
  * 相邻之间的盒子之间的margin 会合并；
  * 浮动的盒子不会与其它盒子重叠；
  * 清除浮动之后，浮动盒子的高度，会被计算在内；

2. FFC
  * 内部盒子 会从左到右 水平排列， 盒子沿 cross axis 方向 会撑满父盒子；
  * 相邻盒子之间的 margin 不会合并；
  * float 属性 不再起作用，类似 vertical-align, clear 都是专门针对 BFC 而设计的；

### display: flex 与 display: inline-flex 异同； 

display: inline-flex does not make flex items display inline. It makes the flex container display inline. That is the only difference between display: inline-flex and display: flex. A similar comparison can be made between display: inline-block and display: block


### Flex Layout Box Model
格式化上下文是一个很抽象的概念，我们希望能利用一个盒子，将其具象化，这个盒子就是 flex layout box model;

![](./images/flex-layout-box-model.png)

1. flex formatting context 中的对象

  * flex container | flex item
  * main axis | cross axis
  * flex line 
    + 默认是 single line ; 出现 multiple line 的前提是使用 flex-wrap: wrap属性；
    + line 的高度之和，默认等于 

2. flex container 中可以使用的属性（角度 与 维度） 

> 从 多个 维度 出发，去解释这个盒子；

  * flex-direction : column | row ; 
    + 本质上是翻转 坐标轴
    + flex item 依旧会沿着main 轴，从后向前排列，cross axis 方向 会撑满 flex container;
  * flex-wrap: wrap 
    + 当flex container overflow 的时候的一种处理方式
    + 当flex container 溢出的时候，会另起一行 flex line; 
    + 溢出的 flex items 会在 另起的 flex line 中，沿 main axis 的方向，从后向前排列；
  * flex-flow : row wrap;
    + 是 flex-wrap 与 flex-direction 的复合写法；
  * justify-content
    + 首先应明确，其作用的对象是main axis , 即只有在main axis 方向 其是起作用的；
    + 其次： 其规定了 flex item 在 main axis 方向的对齐方式；
 
  * align-content
    + 作用对象是 flex line; 前提是我们使用 flex-wrap, 即flex-line 为一条的时候，align-content 不起作用， 多条的时候默认值 为 stretch;
    + 其规定 flex line 在 cross axis 方向的对齐方式；
    + 其默认的值是 align-content: stretch; 所以会出现 上下space 之和 等于 中间 space 的情况；
    + 多条line的和值默认等于父盒子的高度；

   * align-items
    + 其对齐的方向 cross axis, 即只有在 cross axis 方向是其作用的；
    + 其对齐的对象是 flex line 而非 flex container, 
    + 默认的值是 stretch 即默认会撑开 flex line;

   * flex line 的 cross size
    + 如果 flex line 只有一条， 且 flex container 的有一个确切的 cross size，则 flex line 的 cross size 等于 flex container 的 cross size; 
    + 如果 flex line 有多条
      - 默认 align-content: stretch ， 多个 flex lines 的 cross size 的 和 等于 flex container的 cross size; flex line 均分 flex container 的 cross size;
      - 当 align-content 的值 不为 stretch 的时候，会将 flex line 里面 cross size 最大的一个 item 的高度 ，设置为 flex line 的 cross size;


3. flex item 中可以使用的属性
  * flex-grow
  * flex-shrink
  * flex-basis
  * order
  * align-self


### 盒子中的对象，



### display: flex 与 display: inline-flex 的区别




## the difference between flex and inline-flex

> https://stackoverflow.com/questions/27418104/difference-between-displayinline-flex-and-displayflex

## difference between align-items and align-content

> https://stackoverflow.com/questions/24313271/display-property-differences-for-inline-something

## justify-content and align-items

> the first just for main axis , another is just for cross axis; 

