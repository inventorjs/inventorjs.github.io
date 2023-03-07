---
title: Introduction
type: docs
---

# Inventorjs

# @inventorjs/cli
前端脚手架框架，采用插件架构设计，内置脚手架核心及其他常用插件，实现开箱即用，开发者可使用框架提供的脚手架插件快速开发插件。

## 脚手架框架解决的问题
* 命令管理：开发者无需关心底层 commander 等各种复杂工具的使用，只需要按规范实现对象功能即可
* 环境管理：脚手架运行环境往往比较负责，编写脚手架不在需要关心运行环境，由框架内部管理
* 文件管理：开发者无需关心底层文件读写，通过调用上层接口如果"渲染模版"，即可实现快速生成功能
* cmd管理：开发者无需关心底层 execa 底层工具的复杂调用，封装上层功能，仅通过传异步任务即可实现命令调用，并封装输入输出，自动格式化
* 配置管理：脚手架往往需要一个配置文件，而开发这难于管理，框架提供上层抽象能力，方便管理
* 日志管理：框架提供完备的日志打印封装，提供多种日志打印场景，开发这不需要关心底层细节即可实现标准输出
* 插件管理：框架采用插件化设计(类似 yoman)，开发者可通过统一入口管理插件，无需更多脚手架命令，可实现自动化插件管理
* 快速开发：框架提供快速开发模版，一分钟内即可完成一个脚手架插件初始化并发布，开发者只需要实现插件功能即可

### 前置说明
> * corepack 作为 node 新版本的包管理工具，用于管理(yarn, pnpm)包工具，强烈建议开启 corepack
```

  corepack enable
```
> * 脚手架强制使用 [pnpm](https://pnpm.io/)(当前最先进的包管理工具) 作为包管理工具, 使用前请确保已全局安装 pnpm

### 安装

由于脚手架采用插件话设计(参考 @babel/cli)，所以将脚手架核心功能抽离至 @inventorjs/core 中，各个插件采用 peerDependencies 的方式引用，来确保 @inventorjs/core 版本的一致性
```
  // 安装脚手架以及脚手架核心
  pnpm add @inventorjs/cli-core @inventorjs/cli-core -g
```

### 使用
#### 使用内置插件
当前插件内置插件列表，后续可能会新增更多内置插件
* *inventor-plugin-plugin*: 用于快速开发 inventor 插件
* *inventor-plugin-app*: 用于快速开发前端应用，支持多种前端应用模版

```

  // 查看可用的插件命令
  inventor -h

  // 查看 plugin 插件的使用方式
  inventor plugin

  // 查看 app 插件的使用方式
  inventor app
```

#### 安装第三方插件
第三方插件强制格式为 (@scope/)inventor-plugin-[name]，由第三方人员开发，可根据功能进行安装
***注意：plugin 命令默认会自动注册插件至 .inventorrc，如果配置文件非 json 格式，可能回注册失败，手动注册即可以***
```

  // 自动安装第三方插件，如安装 inventor-plugin-test，默认全局安装，如需要局部安装添加 --local 参数即可安装到当前目录
  inventor plugin add inventor-plugin-test

  // 全局调用使用第三方插件
  inventor test

  // 本地调用第三方插件
  pnpm inventor test
```
