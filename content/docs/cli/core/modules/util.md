---
title: util[通用工具模块]
type: docs
---

# 通用工具模块
封装常用的工具函数

## getPluginName(packageName)
通过插件 npm 包名称，获取插件命令名称
> * packageName: \<string\> npm 包名称
## humanSize(bytes, options)
将字节单位转换成人类可读的单位
> * bytes: \<number\> 字节大小
> * options: \<Object\>
>   * base: \<number\> 基数
>   * standard: \<string\> 转换标准
