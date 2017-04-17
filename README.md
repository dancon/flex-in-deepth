# 深入学习 Flexbox

使用 flexbox 首先就是要声明一个 flex container

```
  display: flex | inline-flex;
```

开启 flexbox 格式化上下文。

# flex 术语

flex container： 使用了 `display: flex;` 的元素；

flex item: the child/children of the flex container.

# THe properties of flex container: 

  * flex-direction
  
  * flex-wrap
  
  * flex-flow
  
  * justify-content
  
  * align-item
  
  * align-content
  
### flex-direction

```
  flex-direction: row | column | row-reverse | column-reverse;
```

> default： row

### flex-wrap

```
  flex-wrap: no-wrap | wrap | wrap-reverse;
```

> default： no-wrap

### flex-flow

是 `flex-direction` 和 `flex-wrap` 的合体简写

```
  flex-flow: row nowrap;
```

### justify-content

定义了 main-axis 方向上的对齐方式

```
  justify-content: flex-start | flex-end | center | space-between | space-around;
```

> default: flex-start

### align-item

```
  align-item: stretch | flex-start | flex-end | center | baseline;
```

> default： stretch

### align-content

设置多行在 cross-axis 放上的对齐方式

```
  align-content: stretch | flex-start | flex-end | center
```

> default: stretch

# The properties of Flex item

  * order
  
  * flex-grow
  
  * flex-shrink
  
  * flex-basis
  
  * align-self
  
### order

```
  order: number;
```

> default: 0;

### flex-grow

```
  flex-grow: 0 | positive number;
```

> default: 0 

### flex-shrink

```
  flex-shrink: 0 | positive number;
```

> default: 1

### flex-basis

用来指定 flex item 的初始大小

```
  flex-basis: auto | numver em | number px | number rem ...;
```

> default: auto

如果为 flex item 指定了 `flex-grow: 1` 就会忽略 `flex-basis`, 如果为 flex item 指定了 `flex-basis` 且值非 `auto` 就会忽略 `width`

### flex 

`flex` 是 `flex-grow`, `flex-shrink`, `flex-basis` 的简写。 

```
  flex: flex-grow flex-shrink flex-basis;
```

flex: none 等价于

```
  flex: 0 0 auto; 
```
> flex item 不伸缩，固定大小，浏览器调整大小也不会响应

flex: auto 等价于

```
  flex: 1 1 auto;
```

> flex item 根据内容计算初始宽度，根据 flex-grow 比例分配 flex container 剩余空间，会根据浏览器的大小调整而改变 flex item 大小

flex: positive number 等价于

```
  flex: positive number 1 0;
```

### align-self

只修改特定一个 flex item 在 cross-axis 方向上的对齐方式。

```
  align-self: auto | flex-start | flex-end | center | stretch
```

# 其他

如果在 flex item 上使用 `margin: 0 auto;` 这样的样式，那么在 flex container 上指定 `justify-content` 就无效了。