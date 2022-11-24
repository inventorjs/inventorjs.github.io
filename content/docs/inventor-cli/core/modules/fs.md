---
title: fs[文件处理模块]
type: docs
---

# 文件处理模块
导出 fs-extra 常用函数，并封装常用的文件操作功能

## fs-extra 导出
> * readdir
> * readFile
> * writeFile
> * stat

## getAllFiles(dirPath)
获取目标路径下所有文件路径(深层次递归获取)
> * dirPath: \<string\> 目标目录路径

## getExistsTemplateFiles(templateDir, destinationDir) 
获取已存在目标文件的模版文件列表
> * templateDir: \<string\> 模版目录路径
> * destinationDir: \<string\> 目标目录路径

## exists(filePath) 
判断目标路径是否存在
> * filePath: \<string\> 目标路径

## renderTemplate(templateDir, destinationDir, options)
将模版文件夹所有文件渲染到目标文件夹
> * templateDir: \<string\> 模版文件夹路径
> * destinationDir: \<string\> 目标文件夹路径
> * options: \<Object\> 模版渲染选项
>   * data: \<Object\> 模版数据

## renderTemplate(templateFile, destinationFile, options)
渲染单个模版文件到目标路径
> * templateFile: \<string\> 模版文件路径
> * destinationFile: \<string\> 目标文件路径
> * options: \<Object\> 模版渲染选项
>   * data: \<Object\> 模版数据
