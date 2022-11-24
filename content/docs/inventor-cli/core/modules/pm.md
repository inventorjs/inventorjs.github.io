---
title: pm[包管理模块]
type: docs
---

# pnpm 包管理模块
封装常用的 pnpm 包操作指令，并自动处理命令输出，可直接在插件中进行调用

## checkVersion()
校验脚手架运行环境是否满足需求(如：pnpm: ^7.12.0)

## addPackageJsonFields(fieldsData, filePath)
向 package.json 中添加字段
> * fieldsData: \<Object\> 字段键值对
> * filePath: \<Object\> package.json 文件路径

## getPackageJson(packageJsonPath)
获取 package.json 文件对象数据
> * packageJsonPath: \<Object\> package.json 文件路径

## savePackageJson(savePath, packageJson)
将对象数据保存都 package.json
> * savePath: \<Object\> package.json 文件路径
> * fieldsData: \<Object\> package.json 数据对象

## searchPackageJson(fromPath)
向上层搜索最近的 package.json 
> * fromPath: \<Object\> package.json 搜索起始路径

## root(options)
获取 node_modules 的安装路径
> * options: \<Object\>

## init(options)
初始化 package.json 包
> * options: \<Object\>

## addDependencies(packageNames, options)
安装多个包依赖，并将依赖保存至 package.json
> * packageNames: \<string[]\> 包名@版本列表
> * options: \<Object\>

## addDevDependencies(packageNames, options)
安装多个开发包依赖，并将依赖保存至 package.json
> * packageNames: \<string[]\> 包名@版本列表
> * options: \<Object\>

## removeDependencies(packageNames, options)
移除多个包依赖，并从 package.json 中移除
> * packageNames: \<string[]\> 包名@版本列表
> * options: \<Object\>

## removeDevDependencies(packageNames, options)
移除多个开发包依赖，并从 package.json 中移除
> * packageNames: \<string[]\> 包名@版本列表
> * options: \<Object\>
