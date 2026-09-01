# Java 每日小灶（java-daily-workspace）

> 一个风趣易懂的 Java 自学题库与面试速记单页应用，零依赖、零构建，开箱即看。

## 项目简介

「Java 每日小灶」是一个面向 Java 学习者 / 求职者的纯前端学习工具。把知识点、选择题、面试题都内嵌在 JSON 数据里，用一套清爽的单页界面串起来，主打「风趣讲解 + 卡片式记忆 + 闯关练习 + 面试速记」。所有学习进度都保存在浏览器本地，无需登录、无需联网即可使用。

## 功能特性

- **每日小灶**：274 张知识点卡片，每张含「故事化讲解（story）+ 代码示例（code）+ 一句话窍门（tip）」，覆盖 Java 基础、集合框架、字符串、异常、面向对象、泛型·反射·注解、并发编程、JVM 与 GC、计算机网络、IO 与 Netty、设计模式、Redis、MySQL 数据库、Spring 全家桶、消息队列、系统设计、新特性 等 20+ 分类；分 3 个难度层级（1/2/3 级）。
- **题库闯关**：343 道选择题，按 17 个模块组织（basic / oop / string / collection / exception / reflect / concurrency / jvm / modern / io / net / design / redis / db / arch / framework / mq）。
- **面试速记**：256 张面试卡片（含专业答案 `a` 与趣味答案 `a_fun`），按模块浏览，并支持「考试模式」自测。
- **错题本**：自动收集答错的题目，支持专项复习查漏补缺。
- **多种练习模式**：按模块练习 / 随机练习 / 错题练习 / 薄弱环节练习。
- **收藏与进度**：localStorage 记录已学、收藏、面试卡浏览、错题与完成度（存储键前缀 `jv4.`）。
- **数据导入导出**：学习记录可导出备份、可重新导入。
- **纯前端单页**：无框架、无构建步骤，数据全部内置在 JSON 文件中，双击即可打开。

## 技术栈

- 纯静态 **HTML + 原生 JavaScript + 内联 CSS**（无 React/Vue 等框架，无打包构建）。
- 数据驱动：知识点 `lessons.json`、题库 `questions.json`、面试题 `interview.json`。
- 本地持久化：浏览器 `localStorage`（键前缀 `jv4.`）。

## 目录结构

```
java-daily-workspace/
├── index.html        # 单页应用主文件（界面 + 逻辑 + 内联样式）
├── lessons.json      # 274 张知识点卡片
├── questions.json    # 343 道选择题（含模块字段）
└── interview.json    # 256 张面试速记卡片
```

## 本地运行

本项目是纯静态单页应用，**无需安装依赖、无需构建**：

1. 直接双击 `index.html` 用浏览器打开即可使用。
2. 若个别浏览器对 `file://` 加载本地 JSON 有限制，可启动一个本地静态服务器后再访问，例如：
   ```bash
   python -m http.server 8000
   # 然后浏览器打开 http://localhost:8000/
   ```

## 在线演示

https://chenbenkong.github.io/java-daily-workspace/

## 说明 / 备注

- 所有学习数据（已学、收藏、错题、进度）仅保存在**当前浏览器本地**（`localStorage`，前缀 `jv4.`），不上传任何服务器；更换或清理浏览器数据会清空进度，建议用「导出」功能备份。
- 题库与面试题为作者整理的学习资料，仅供练习参考。
