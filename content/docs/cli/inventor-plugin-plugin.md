---
title: inventor-plugin-plugin[插件管理]
type: docs
---

# 脚手架内置插件管理插件
用于快速开发 inventor 脚手架插件，提供快速开发模版以及开发调试能力

## 使用方式
### 插件本地开发
下面以开发 "*inventor-plugin-test*" 插件为例
```

  // 初始化插件，按规则输入插件名称，输入插件包名称 inventor-plugin-test
  inventor plugin init

  // 进入插件目录，启动开发
  cd inventor-plugin-hello

  // 将插件链接到全局
  pnpm link -g

  // 修改插件配置文件 ~/.inventorrc 在 plugins 字段添加 ["inventor-plugin-test"]

  // 启动开发服务器
  pnpm dev

  // 此时即可通过 inventor 命令调用插件
  inventor -h
```

### 插件发布至仓库
发布前记得确认 .npmrc 文件中的 registry，当前默认是 ***https://registry.npmjs.org***
```

  // 生成新的包版本
  pnpm version patch

  // 发布至 npm 仓库
  pnpm publish

  // 此时可全局安装当前插件如 inventor-plugin-test
  pnpm add inventor-plugin-hello -g

  // 然后即可正常使用插件
  inventor hello
```
