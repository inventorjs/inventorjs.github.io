---
title: log[日志处理模块]
type: docs
---

# 日志处理模块

## clear()
清空终端输出日志信息，仅对标准终端有效
## info(msg, options)
打印 INFO 类型日志信息
> * msg: \<unknown\> 日志信息
> * options: \<Object\>
>   * boxen: \<BoxenOptions | true\>
>   * dedent: \<boolean\>
>   * art: \<figlet.Options & { color: green | cyan }\>

## success(msg, options)
打印 SUCCESS 类型日志信息
> * msg: \<unknown\> 日志信息
> * options: \<Object\>
>   * boxen: \<BoxenOptions | true\>
>   * dedent: \<boolean\>
>   * art: \<figlet.Options & { color: green | cyan }\>

## error(msg, options)
打印 ERROR 类型日志信息
> * msg: \<unknown\> 日志信息
> * options: \<Object\>
>   * boxen: \<BoxenOptions | true\>
>   * dedent: \<boolean\>
>   * art: \<figlet.Options & { color: green | cyan }\>

## warn(msg, options)
打印 warn 类型日志信息
> * msg: \<unknown\> 日志信息
> * options: \<Object\>
>   * boxen: \<BoxenOptions | true\>
>   * dedent: \<boolean\>
>   * art: \<figlet.Options & { color: green | cyan }\>


## raw(msg, options)
将日志转化为字符串，并输出原始日志信息
> * msg: \<unknown\> 日志信息
> * options: \<Object\>
>   * boxen: \<BoxenOptions | true\>
>   * dedent: \<boolean\>
>   * art: \<figlet.Options & { color: green | cyan }\>

## bye(msg, options)
打印 bye 类型日志信息，**并退出当前进程**
> * msg: \<unknown\> 日志信息
> * options: \<Object\>
>   * boxen: \<BoxenOptions | true\>
>   * dedent: \<boolean\>
>   * art: \<figlet.Options & { color: green | cyan }\>
