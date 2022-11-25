---
title: Introduction
type: docs
---

# Inventorjs

## @inventorjs/cli
前端脚手架框架，采用插件架构设计，内置脚手架核心及其他常用插件，实现开箱即用，开发者可使用框架提供的脚手架插件快速开发插件。

### 前置说明
> * 脚手架强制使用 pnpm(当前最流量，最先进的包管理工具) 作为包管理工具, 使用前请确保已全局安装 pnpm
### 安装

由于脚手架采用插件话设计(参考 @babel/cli)，所以将脚手架核心功能抽离至 @inventorjs/core 中，各个插件采用 peerDependencies 的方式引用，来确保 @inventorjs/core 版本的一致性
```
  pnpm add @inventorjs/core @inventorjs/cli -g
```

### 使用
```
  // 查看可用的插件命令
  inventor -h
  // 初始化 inventor 插件模版
  inventor plugin init
```
