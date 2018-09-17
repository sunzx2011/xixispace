---
title: 字典标准系统
date: 2018-09-17
categories: 字典
tags: [字典]
---

# 推广梯商机发布平台接口测试

> 地址： http://139.224.8.18:8020/tuiguangti

> 说明： 为您搭建商机推广成功之梯

> 版本： 1.0

### 字典标准系统

#### 新增字典信息

* URL | /api/sys/comm_code/add
* 方式 | post
* 类别 | application/json
* 说明 | 新增字典信息，返回是否成功标志

###### 入参

参数编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|必填|-
description|描述字段|String|500|非必填|-
sortNo|排序号|Integer|-|必填|1
type|类型|String|50|必填|-
value|代码值|String|500|必填|-

###### 出参

返回编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
type|type|boolean|-|-|-

*** 

#### 查询字典详情

* URL | /api/sys/comm_code/query_id
* 方式 | post
* 类别 | application/json
* 说明 | 查询符合ID序号的单条字典数据详情，返回数据结果

###### 入参

参数编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
id|ID|Integer|-|必填|1

###### 出参

返回编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|-|-
description|描述字段|String|500|-|-
id|ID|Integer|-|-|1
sortNo|排序号|Integer|-|-|1
type|类型|String|50|-|-
value|代码值|String|500|-|-

*** 

#### 查询字典列表

* URL | /api/sys/comm_code/query_list
* 方式 | post
* 类别 | application/json
* 说明 | 模糊查询符合条件的字典数据，返回数据结果

###### 入参

参数编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|非必填|-
type|类型字段|String|50|非必填|-
value|代码值|String|500|非必填|-

###### 出参

返回编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|-|-
description|描述字段|String|500|-|-
id|ID|Integer|-|-|1
sortNo|排序号|Integer|-|-|1
type|类型|String|50|-|-
value|代码值|String|500|-|-

*** 

#### 查询字典列表

* URL | /api/sys/comm_code/query_list_by_page
* 方式 | post
* 类别 | application/json
* 说明 | 模糊查询符合条件的字典数据，返回数据结果

###### 入参

参数编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|非必填|-
countSql|是否获取总数|boolean|-|必填|true
pageNum|当前页码|Integer|-|必填|1
pageSize|每页的数量|Integer|-|必填|1
type|类型字段|String|50|非必填|-
value|代码值|String|500|非必填|-

###### 出参

返回编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|-|-
description|描述字段|String|500|-|-
id|ID|Integer|-|-|1
sortNo|排序号|Integer|-|-|1
type|类型|String|50|-|-
value|代码值|String|500|-|-

*** 

#### 删除字典信息

* URL | /api/sys/comm_code/remove
* 方式 | post
* 类别 | application/json
* 说明 | 删除单条字典信息数据，返回是否成功标志

###### 入参

参数编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
id|ID|Integer|-|必填|1

###### 出参

返回编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
type|type|boolean|-|-|-

*** 

#### 更新字典信息

* URL | /api/sys/comm_code/update
* 方式 | post
* 类别 | application/json
* 说明 | 更新单条字典数据，返回是否成功标志

###### 入参

参数编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
code|代码字段|String|50|非必填|-
description|描述|String|500|非必填|-
id|ID|Integer|-|必填|1
sortNo|排序号|Integer|-|非必填|1
type|类型字段|String|50|非必填|-
value|代码值|String|500|非必填|-

###### 出参

返回编码|名称|类型|长度|是否必填|示例
-|-|-|-|-|-
type|type|boolean|-|-|-

*** 

