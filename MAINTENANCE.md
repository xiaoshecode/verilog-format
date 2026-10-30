# verilog-format 维护说明

使用 Java 实现的 Verilog 格式化命令行工具。

- 上游：https://github.com/ericsonj/verilog-format
- 在线文档：https://xiaoshecode.github.io/xiaoshecode/repos/verilog-format/
- 检查日期：2026-10-30

## 环境与使用

- 准备 Java 和 Maven；以 pom.xml 为编译配置。

使用/检查入口（需先满足依赖条件）：

- `mvn clean package`
- `java -jar target/verilog-format-1.0.1-full.jar --help`

## 目录职责

- src/ — Java 格式化源码
- pom.xml — Maven 构建
- verilog/ — Verilog 示例
- bin/ — 上游预构建压缩包

## 本次整理

- 新增维护文档和在线文档入口，补全用途、目录、使用路径及验证边界。

## 检查记录

- **仓库目录与入口盘点**（passed）：检查 Git 索引中的 66 个路径、README 和项目配置；不等于功能验收。
- **XML parse**（passed）：1 个文件通过解析；不导入依赖、不执行应用。
- **完整构建与端到端运行**（not_run）：本机 PATH 无 Java/Maven；未构建或执行上游二进制。jar 文件名应以 target/ 实际构建产物为准。

## 验证边界与待办

- 本机 PATH 无 Java/Maven；未构建或执行上游二进制。构建依赖历史 Maven/Launch4j 配置，需要在匹配工具链复验。

## 后续维护约定

保留上游许可证与作者信息。沿用现有模块边界和格式配置；修复功能时同步最小回归验证。依赖或接口变更需写明迁移步骤，避免仅为目录美观搬动公开入口。
