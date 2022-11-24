---
title: Plugin[插件基础类]
type: docs
weight: 2
---

# 插件基础抽象类(Plugin)
插件实例基础抽象类，封装常用的脚手架插件开发相关功能，插件需要继承该抽象类以实现插件功能(其中 abtract 方法和属性为子插件必须实现的)，插件实例通过脚手架框架内部自动创建，插件开发者无需手动初始化插件实例，插件实例和方法在子插件种皆可通过 this 获取。
## new Plugin(params)
插件构造函数为脚手架框架内部调用，插件开发者无需创建插件实例

* params:
>  * entryPath: \<string\> 插件入口路径

## this.entryPath
> * Type: \<string\> 插件入口路径

## this.templatePath
> * Type: \<string\> 插件模版路径

## this.actionPath
> * Type: \<string\> action 文件夹路径

## this.prompt(questions) 
实现命令行可交互问答，对 inquirer 核心功能封装
> * questions: \<Object[]\> 问题数组
>   * type: \<checkbox|text\> 问题类型
>   * name: \<string\> 问题键名
>   * message: \<string\> 问题描述
>   * choices: \<Object[]\> 问题可选项
>     * name: \<string\> 选项名称
>     * value: \<string\> 选项值

## this.install(options)
在上下文目录执行 pnpm install 进行包安装
> * options: \<Object\> 调用选项

## this.addDependencies(packageNames, options)
在上下文目录批量添加依赖包
> * packageNames: \<string[]\> 依赖包名称数组(如：axios@1.0.0)

## this.addDevDependencies(packageNames, options)
在上下文目录批量添加开发依赖包
> * packageNames: \<string[]\> 依赖包名称数组(如：axios@1.0.0)

## this.removeDependencies(packageNames, options)
在上下文目录批量删除依赖包
> * packageNames: \<string[]\> 依赖包名称数组(如：axios@1.0.0)

## this.removeDevDependencies(packageNames, options)
在上下文目录批量删除开发依赖包
> * packageNames: \<string[]\> 依赖包名称数组(如：axios@1.0.0)

## this.getPackageJson(fromPath = this.entryPath)
从 fromPath 开始查找 package.json 文件直到根目录，并返回 json 对象
> * fromPath: \<string\> 查找起始路径

## this.addPackageJsonFields(fieldsData, filePath)
向 package.json 添加字段
> * fieldsData: \<Object\> 字段数据对象
> * filePath: \<string\> package.json 文件路径

## this.savePackageJson(filePath, packageJson)
保存 packageJson 对象到 package.json 文件
> * filePath: \<string\> package.json 文件路径
> * packageJson: \<Object\> packageJson 数据对象

## this.getPackageName(fromPath = this.entryPath)
获取指定路径的 npm 包名称
> * fromPath: \<string\> 查找起始路径

## this.getPluginName(frompath = this.entryPath)
获取指定路径的 inventor-plugin 名称，即命令行执行名称
> * fromPath: \<string\> 查找起始路径

## this.confirmOverwrites(paths)
询问是否覆盖指定路径的文件
> * paths: \<string[]\> 文件路径列表

## this.renderTemplate(templateName, destinationName, options)
渲染指定模版文件夹到目标文件夹
> * templateName: \<string\> 模版名称(即在 templates 的子文件夹名称)
> * destinationName: \<string\> 目标文件夹名称
> * options: \<Object\> 模版渲染选项
>   * data: \<Object\> 模版数据
>   * overwrites: \<Boolean\> 是否覆盖已存在目标文件

## this.renderTemplateFile(templateName, templateFile, destinationFile, options)
渲染指定模版文件到目标文件
> * templateName: \<string\> 模版名称(即在 templates 的子文件夹名称)
> * templateFile: \<string\> 模版目录下的文件，相对模版路径
> * destinationFile: \<string\> 目标文件名称
> * options: \<Object\> 模版渲染选项
>   * data: \<Object\> 模版数据
>   * overwrites: \<Boolean\> 是否覆盖已存在目标文件

