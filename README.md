# CC Game Framework Project

参见：[从零开始构建标准库 - 知乎专栏](https://zhuanlan.zhihu.com/learncpp)

实现一个游戏框架。

## 介绍

架构是**C/C++**，渲染用**DirectX**，库用**WTF/STL/ATL**。

从易到难，逐步推进。

## 历程

### 第一阶段：搭好脚手架

项目架构：

- base - 基础类
- ui - 界面逻辑
- render - DX渲染逻辑
- lua - lua代码
- lua_ext - lua扩展
- script - lua脚本

整体思路：

- 将窗口包装成Window类，借鉴自MFC中的相关内容
- D2D1和DWrite的初始化
- 实现图元工厂模式，统一管理DX资源，已实现色块和文字的渲染
- 截取Window的特定消息，进行渲染

当前进度：

- 已整合Lua 5.3.3
- 实现背景渐变的效果

TODO：

- 实现定时器功能
- 实现触发器功能
- 实现场景切换功能