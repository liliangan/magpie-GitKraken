# GitKraken Magpie 网关与 AI 模型配置

[English](README.en.md)

## 用途

通过 Magpie 配置 GitKraken 的 Magpie 网关与 AI 模型。本仓库提供**两种使用方式（二选一，不要同时启用）**：

1. **方式一：统一模型版（1 个包）**
   安装 `magpie-gitkraken-all-in-one`，单个条目即可完成 Magpie 网关连接配置，并将同一模型同步写入全部六项 GitKraken AI 功能，适合全部功能共用同一个模型的场景。
2. **方式二：独立模型版（6 个包）**
   安装 `magpie-gitkraken-ai`（必装主包，负责写入共享网关连接），并按需安装其余五个功能包，为六项功能分别选择不同模型。使用其他功能条目前，需要先启用 `magpie-gitkraken-ai` 完成连接配置。

## 包含的插件包

| 模式 | Magpie 条目 | npm 包名 | 目录 | 对应的 GitKraken 功能 |
| --- | --- | --- | --- | --- |
| 统一模型版 | GitKraken 全部 AI 功能（统一模型） | `magpie-gitkraken-all-in-one` | `GitKrakenAllInOne` | 一次配置网关并将同一模型应用到全部六项 AI 功能 |
| 独立模型版（主包） | GitKraken 提交消息生成（Magpie 网关） | `magpie-gitkraken-ai` | `GitKrakenCommitMessage` | 根据更改生成提交消息，同时负责连接 Magpie 网关 |
| 独立模型版 | GitKraken 解释更改 | `magpie-gitkraken-explain-commits` | `GitKrakenExplainCommits` | 解释提交、贮藏及其他更改 |
| 独立模型版 | GitKraken 贮藏消息生成 | `magpie-gitkraken-stash-message` | `GitKrakenStashMessage` | 生成贮藏消息 |
| 独立模型版 | GitKraken 拉取请求 | `magpie-gitkraken-pull-request` | `GitKrakenPullRequest` | 生成拉取请求的标题和描述 |
| 独立模型版 | GitKraken 冲突解决 | `magpie-gitkraken-conflict-resolution` | `GitKrakenConflictResolution` | 辅助解决合并冲突 |
| 独立模型版 | GitKraken 提交编写器 | `magpie-gitkraken-rebase` | `GitKrakenRebase` | 辅助编写和整理提交 |

## 安装

### 方式一：统一模型版（推荐省心）

```bash
magpie plugin add magpie-gitkraken-all-in-one
```

### 方式二：独立模型版（按功能单独选模型）

```bash
magpie plugin add magpie-gitkraken-ai
# 按需继续安装其他功能包：
magpie plugin add magpie-gitkraken-explain-commits
magpie plugin add magpie-gitkraken-stash-message
magpie plugin add magpie-gitkraken-pull-request
magpie plugin add magpie-gitkraken-conflict-resolution
magpie plugin add magpie-gitkraken-rebase
```

## 使用方法

1. 启动 Magpie，并确保准备使用的模型供应商已登录或配置好。
2. 根据所选方案在 Magpie 的 Agent 页面启用条目并选择模型：
   - 若使用**统一模型版**：启用“GitKraken 全部 AI 功能（统一模型）”并选择模型即可。
   - 若使用**独立模型版**：先启用“GitKraken 提交消息生成（Magpie 网关）”选择模型以完成共享网关连接，再启用其他需要的条目分别选择模型（其他五个条目不能单独完成网关连接配置）。
3. 首次使用时，在 GitKraken 偏好设置中选择“自定义 URL”，不要选择默认 OpenAI 服务。Magpie 网关地址由插件自动写入，无需手动填写；API Key 可以留空，不影响实际使用。若要点击 GitKraken 的“测试连接”，再填入任意非空值即可，其他功能无需重复设置。
4. 完全退出并重新打开 GitKraken，让它读取新的配置，然后正常使用对应的 AI 功能。使用期间保持 Magpie 运行。

后续更换模型时，在 Magpie 对应条目中重新选择即可；如果 GitKraken 界面仍显示旧模型，完全退出并重新打开 GitKraken。

插件目前只配置模型，不提供推理强度设置。
