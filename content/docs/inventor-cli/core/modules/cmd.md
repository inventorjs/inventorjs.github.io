---
title: cmd[命令处理模块]
type: docs
---

# 命令行程序调用模块
封装 execa 调用方法，提供对返回数据 buffer 进行处理的能力

## exec(bin, args, options)
调用命令行程序
> * bin: \<string\> 执行命令行程序
> * args: \<string[]\> 命令行程序参数
> * options: \<Object\>
>   * output: \<Boolean\> 是否输出运行结果
>   * pipeline: \<'stdout' | 'stderr'\> 输出文件描述符
>   * pipe: \<Function\>
>     * buf: \<Buffer\> 处理命令输出的 buffer
