---
title: git[git命令模块]
type: docs
---

# git 命令模块
封装 git 相关命令行工具

## init(options)
初始化 git 仓库
> * options: \<Object\>
>   * output: \<Boolean\> 是否输出运行结果
>   * pipeline: \<'stdout' | 'stderr'\> 输出文件描述符
>   * pipe: \<Function\>
>     * buf: \<Buffer\> 处理命令输出的 buffer
