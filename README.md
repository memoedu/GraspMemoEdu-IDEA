# GraspMemoEdu IDEA 插件

GraspMemoEdu Academy Bridge 在 IntelliJ IDEA 中打开网站上的练习，并将 IDEA 的作答检查结果回传给当前学习账号。

从 GraspMemoEdu 的计算机科学指南打开 [IntelliJ IDEA 安装小节](https://memoedu.github.io/GraspMemoEdu-Pages/#/subjects/cs/guide?section=idea-setup)，复制提示词交给本机 Agent。预编译插件与 SHA-256 在 [Releases](https://github.com/memoedu/GraspMemoEdu-IDEA/releases)。

## 兼容与安装入口

- 插件 ID 为 `edu.graspmemo.academy`，支持 IDEA 的 262 系列。首个公开版本以 Windows、IDEA 2026.2.2（含 JetBrains Runtime 25）和 JetBrains Academy 2026.10 构建及测试。已有兼容且可用的安装可以直接复用。
- IDEA 从 [JetBrains 官方渠道](https://www.jetbrains.com/idea/download/)获取，JetBrains Academy（`com.jetbrains.edu`）从 [JetBrains Marketplace](https://plugins.jetbrains.com/plugin/10081-jetbrains-academy)获取。插件 ZIP 可以通过 IDEA 的磁盘安装入口安装。Windows 的当前用户协议注册可用源码维护仓库中的 `idea-plugin/Install.ps1`，传入本机的实际安装路径和已安装文件哈希。源码脚本默认值仅适用于维护环境。
- 在 IDEA 实际使用的 config 目录中，按 [配置样例](graspmemoedu-academy.example.json)提供 `graspmemoedu-academy.json`。课程项目路径、版本与清单来自课程的授权分发渠道。所需 JDK、检查器和测试包随题目适配器而异。本仓库发布通用插件，课程项目和课程判题包由其原入口提供。
- 测试时从登录后的 GraspMemoEdu 打开一题，核对 IDEA 实际打开的题目及网页的连接状态。网站用题目轮次的临时票据接收打开回执。

源码维护于 [memoedu/GraspMemoEdu 的 idea-plugin](https://github.com/memoedu/GraspMemoEdu/tree/main/idea-plugin)。每个 Release 标出用于构建的源码提交，以及测试使用的 IDEA 和 Academy 版本。
