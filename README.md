
# Flex layout


## Css Formatting context

1. BFC block formatting context 
  - 概念：块级格式化上下文，内部盒子垂直放置，相临盒子的margin重叠，内部样式不影响外部，不会和float元素重叠，内部浮动元素高度会被算在容器高度中;
  - 形成条件：float 属性不为 none、overflow 不为 visible、position 为 absolute 或 fixed、display为inline-block、table-cell、table-caption;
2. IFC inline formatting context
  - 概念：内联格式化上下文、内部盒子水平放置;
  - 形成条件：display为inline、inline-block的外层会形成IFC环境，用于水平居中内联元素或内联元素垂直居中;
3. GFC
  - 概念：网格布局格式化上下文;
  - 形成条件：display设置为grid;
4. FFC
  - 概念：自适应格式化上下文;
  - 形成条件：display设置为flex、inline-flex;


> 示例1： 




## the difference between flex and inline-flex

> https://stackoverflow.com/questions/27418104/difference-between-displayinline-flex-and-displayflex

## difference between align-items and align-content

> https://stackoverflow.com/questions/24313271/display-property-differences-for-inline-something

## justify-content and align-items

> the first just for main axis , another is just for cross axis; 

