# 智能看板-循环经济链子页面API
​	

## 配置页面——获得配置信息

返回一个json，包含以下字段

| 字段     | 类型          | 描述                                                         |
| -------- | ------------- | ------------------------------------------------------------ |
| p1source | array(object) | 生产产量中，可供选择的全部产品，每一项包含name和value两字段，分别表示产品名称和产品id |
| p1array  | array(string) | 生产产量中，已配置的产品id的列表                             |
| p2source | array(object) | 原料库存中，可供选择的全部产品，每一项包含name和value两字段，分别表示产品名称和产品id |
| p2array  | array(string) | 原料库存中，已配置的产品id的列表                             |
| p3source | array(object) | 生产绩效中，可供选择的全部分厂，每一项包含name和value两字段，分别表示分厂名称和分厂id |
| p3array  | array(string) | 生产绩效中，已配置的分厂id的列表                             |
| p4source | array(object) | 生产消耗中，可供选择的全部分厂，每一项包含name和value两字段，分别表示分厂名称和分厂id |
| p4array  | array(string) | 生产消耗中，已配置的分厂id的列表                             |
| p7source | array(object) | 生产质量中，可供选择的全部产品，每一项包含name和value两字段，分别表示产品名称和产品id |
| p7array  | array(string) | 生产质量中，已配置的产品id的列表                             |

​	

## 配置页面——保存配置信息

提交一个json，包含以下字段

| 字段    | 类型          | 描述                             |
| ------- | ------------- | -------------------------------- |
| p1array | array(string) | 生产产量中，已配置的产品id的列表 |
| p2array | array(string) | 原料库存中，已配置的产品id的列表 |
| p3array | array(string) | 生产绩效中，已配置的分厂id的列表 |
| p4array | array(string) | 生产消耗中，已配置的分厂id的列表 |
| p7array | array(string) | 生产质量中，已配置的产品id的列表 |

​	

## 展示页面——获取展示数据

返回一个json，包含以下字段

| 字段 | 类型          | 描述                                                         |
| ---- | ------------- | ------------------------------------------------------------ |
| p1   | array(object) | 描述生产产量，是一个对象数组，数组的每一项表示一个产品，包含字段name,v1,v2,v3，分别描述了产品名称，当前产量，月计划，上月实绩 |
| p2   | array(object) | 描述原料库存，是一个对象数组，数组的每一项表示一个产品，包含字段name,v1,v2,v3，分别描述了产品名称，当前库存，消耗量，入库量 |
| p3   | array(object) | 描述生产绩效，是一个对象数组，数组的每一项表示一个分厂，包含字段name,v1,v2,v3,v4，分别描述了分厂名称，制造成本，产量，质量，安全环保 |
| p4   | array(object) | 描述生产消耗，是一个对象数组，数组的每一项表示一个分厂，包含字段name,v1,v2,v3,v4，分别描述了分厂名称，原料，辅料，设备，能源 |
| p5   | array(object) | 描述设备运行指标，是一个对象数组，数组的每一项表示一个日期，包含字段date,v1,v2，分别描述了日期，完好率，消缺率 |
| p6   | array(object) | 描述能耗指标，是一个对象数组，数组的每一项表示一个月份，包含字段month,v1,v2,v3,v4，分别描述了月份，水耗计划，水耗实际，电耗计划，电耗实际 |
| p7   | array(object) | 描述生产质量，是一个对象数组，数组的每一项表示一个产品，包含字段name,v1,v2,v3,v4，分别描述了产品名称，优等品，合格，不合格，一等品 |
| p8   | array(object) | 描述安环指标，是一个对象数组，数组的每一项表示一个月份，包含字段month,v1,v2,v3，分别描述了月份，安全，环保，健康 |

