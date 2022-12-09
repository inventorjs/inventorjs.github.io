---
title: Introduction
type: docs
---

# Inventorjs

## @inventorjs/cli
前端脚手架框架，采用插件架构设计，内置脚手架核心及其他常用插件，实现开箱即用，开发者可使用框架提供的脚手架插件快速开发插件。

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
