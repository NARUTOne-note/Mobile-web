# Grid 布局

> css grid

flex 布局是一维布局，Grid 布局是二维布局。flex 布局一次只能处理一个维度上的元素布局，一行或者一列。Grid 布局是将容器划分成了“行”和“列”，产生了一个个的网格

**注意**：

- 定义网格时，定义的是网格轨道，而不是网格线

## 容器属性

- `display`：`grid` 则该容器是一个块级元素，`inline-grid` 则容器元素为行内元素

- `grid-template-columns`: 列宽, `grid-template-rows`: 行高
  - 声明三列（行），宽（高）度分别为 `200px 100px 200px`
  - `repeat(count, value)`: 重复次数, 重复值 `repeat(2, 50px)`
  - `auto-fill` 关键词: `repeat(auto-fill, 200px)`,  200 px，但数量是不固定的，容器能够容纳得下，就可以放置元素
  - `fr` 关键字: `200px 1fr 2fr`, 第一个列宽设置为 200px，后面剩余的宽度分为两部分，宽度分别为剩余宽度的 1/3 和 2/3
  - `minmax()`：长度范围，`1fr 1fr minmax(300px, 2fr)` 第三个列宽最少也是要 300px，但是**最大不能大于第一第二列宽的两倍**
  - `auto` 关键词：容器剩余填充 `100px auto 100px`

- `grid-row-gap` 行间距、`grid-column-gap` 列间距、 `grid-gap` 间距
  - `grid-gap: 10px 20px;`: 行，列间距

- `grid-template-areas`: 定义区域模板(合并单元格)，一个区域由一个或者多个单元格组成, `grid-area` 属性指定项目放在哪一个区域
  - `". header  header"` + `"sidebar content content"` 两行区域, `.` 符号代表空的单元格，也就是没有用到该单元格
  - `grid-area: sidebar;` 定义区域

- `grid-auto-flow`: 控制着被自动布局的元素的布局算法怎样运作
  - `row`: 默认，从行开始填充
  - `column`: 从列开始
  - `row dense`，`column dense` 尽可能填满表格

## 项目属性
