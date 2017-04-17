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
  
### order

```
  order: number;
```

> default: 0;