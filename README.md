# Brix - PC（Windows）端

> 📱 **主项目（手机版 / Android）**：[wccch-wzz/Brix-Android](https://github.com/wccch-wzz/Brix-Android)
>
> 本仓库为 **Brix PC（Windows）端源码仓库**（Brix 1.0.0）。

## 这是什么

Brix 是一个基于 Electron 的 **Minecraft 启动器 / 模组管理器**：

- 游戏版本与加载器管理（Forge / NeoForge / Fabric / OptiFine）
- 模组、整合包、资源搜索与安装（Modrinth / CurseForge）
- 微软 / 离线 / 外置登录（authlib-injector）
- Java 运行时检测与自动安装
- 局域网联机（UPnP / EasyTier）、崩溃诊断等

## 目录结构

```
├── main.js / main/         Electron 主进程（窗口/协议/存储/更新/崩溃日志）
├── server.js / server/     业务服务层（brix:// 协议，无端口）
├── js/ + index.html        渲染进程前端（原生 JS）
├── activation/             激活授权模块
├── bbot/                   Bbot 组件
├── plugins/                插件（modrinth、mod-dev-tools）
└── scripts/                构建/发布脚本
```

## 运行与构建

```bash
npm install          # 安装依赖（dependencies 见 package.json）
npm start            # 开发运行（Electron）
# 打包：electron-builder（NSIS）产出 Brix-Setup-*.exe
```

> 提示：node_modules 与构建产物不入库，请按需安装/构建。

## 关联项目

| 项目 | 说明 | 链接 |
|---|---|---|
| 📱 Brix-Android | 手机版（主项目） | https://github.com/wccch-wzz/Brix-Android |
| 💻 Brix-PC | PC（Windows）端（本仓库） | https://github.com/wccch-wzz/Brix-PC |
