# 教程-量度 (Scale)
+ https://www.yuque.com/antv/f2/scale
> 这一节不是很理解

## 什么是量度：
> 度量 Scale，是数据空间到图形空间的转换桥梁，负责原始数据到 [0, 1] 区间数值的相互转换工作。针对不同的数据类型对应不同类型的度量。


## 根据数据的类型，F2 支持以下几种度量类型：
- identity，常量类型的数值，也就是说数据的某个字段是不变的常量；
- linear，连续的数字 [1, 2, 3, 4, 5]；
- cat，分类, ['男','女']；
- timeCat，时间类型；


## 在 F2 的使用中，我们主要通过列定义操作来接触度量：
```js
const data = [
  { a: 'a', b: 20 },
  { a: 'b', b: 12 },
  { a: 'c', b: 8 },
];
const defs = {
  a: {
    type: 'cat' // 声明 a 字段的类型
  },
  b: {
    min: 0, // 手动指定最小值
    max: 100 // 手动指定最大值
  }
};

chart.source(data, defs);
```
## 之后改变用这种：
```js
chart.scale('fieldName', {
  // 各个属性配置
});
```

### 下面列出的是通用的属性
> type/formatter/range/alias/tickCount/ticks

