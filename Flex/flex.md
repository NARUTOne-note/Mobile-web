# Welcome to Flex

- [MDN Flex](https://developer.mozilla.org/zh-CN/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes)
- [w3c Flex](https://www.w3cplus.com/css3/a-guide-to-flexbox-new.html)
- 🔥[flex 视图学习](https://zhuanlan.zhihu.com/p/47613256)

## 简写语法

**单值语法**: 值必须为以下其中之一:

- 一个无单位数(`<number>`): 它会被当作`<flex-grow>`的值。
- 一个有效的宽度(width)值: 它会被当作 `<flex-basis>`的值。

关键字`none`，`auto`或`initial`.

- `initial` 元素会根据自身宽高设置尺寸
- `auto` 元素会根据自身的宽度与高度来确定尺寸，但是会伸长并吸收 flex 容器中额外的自由空间，也会缩短自身来适应 flex 容器。这相当于将属性设置为 "flex: 1 1 auto".
- `none` 元素会根据自身宽高来设置尺寸。它是完全非弹性的

**双值语法**: 第一个值必须为一个无单位数，并且它会被当作 `<flex-grow>` 的值。第二个值必须为以下之一：

- 一个无单位数：它会被当作 `<flex-shrink>` 的值。
- 一个有效的宽度值: 它会被当作 `<flex-basis>` 的值。

**三值语法**:

- 第一个值必须为一个无单位数，并且它会被当作 `<flex-grow>` 的值。
- 第二个值必须为一个无单位数，并且它会被当作 `<flex-shrink>` 的值。
- 第三个值必须为一个有效的宽度值， 并且它会被当作 `<flex-basis>` 的值。
