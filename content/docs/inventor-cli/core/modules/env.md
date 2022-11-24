---
title: env[环境管理模块]
type: docs
---

# 环境管理模块
主要提供脚手架当前执行环境的一些相关信息，管理脚手架执行上下文

## isTTY()
判断当前是否是标准终端环境，如在子进程中(pnpm exec -r), 则返回false

## pwd()
获取当前所在路径

## homedir()
获取当前用户家目录

## context()
获取安装脚手架上下文(global|local)

## username()
获取当前用户名

## uid()
获取当前用户 uid

## dirname(metaUrl)
获取文件所在目录(主要用于转换 import.meta.url)
> * metaUrl: \<string\> 模块的 import.meta.url 值

## filename(metaUrl) {
获取文件绝对路径(主要用于转换 import.meta.url)
> * metaUrl: \<string\> 模块的 import.meta.url 值

## changeCwd(enterCwd)
改变当前命令执行上下文目录
> * enterCwd: \<string\> 执行上下文目录
