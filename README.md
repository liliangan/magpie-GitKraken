# GitKraken Magpie 网关与 AI 模型配置

[English](README.en.md)

## 用途

通过 Magpie 为 GitKraken 的六项 AI 功能分别选择模型，各功能可以使用不同的模型。六个条目分别控制对应功能的模型，但网关连接配置由“GitKraken 提交消息生成（Magpie 网关）”条目统一写入；使用其他功能条目前，需要先启用该条目完成连接配置。

| Magpie 条目 | 对应的 GitKraken 功能 |
| --- | --- |
| GitKraken 提交消息生成（Magpie 网关） | 根据更改生成提交消息，同时负责连接 Magpie 网关 |
| GitKraken 解释更改 | 解释提交、贮藏及其他更改 |
| GitKraken 贮藏消息生成 | 生成贮藏消息 |
| GitKraken 拉取请求 | 生成拉取请求的标题和描述 |
| GitKraken 冲突解决 | 辅助解决合并冲突 |
| GitKraken 提交编写器 | 辅助编写和整理提交 |

## 使用方法

1. 启动 Magpie，并确保准备使用的模型供应商已登录或配置好。
2. 在 Magpie 的 Agent 页面启用“GitKraken 提交消息生成（Magpie 网关）”，选择模型。该条目同时负责设置 GitKraken 的共享网关连接，是其他五个功能条目的连接前置条件。
3. 首次使用时，在 GitKraken 偏好设置中选择“自定义 URL”，不要选择默认 OpenAI 服务。Magpie 网关地址由插件自动写入，无需手动填写；API Key 可以留空，不影响实际使用。若要点击 GitKraken 的“测试连接”，再填入任意非空值即可，其他五项功能无需重复设置。
4. 在 Magpie 中启用需要使用的其他 GitKraken 条目，分别选择模型。每个条目只更新对应功能的模型选择，可以单独切换模型，但不能单独完成网关连接配置。
5. 完全退出并重新打开 GitKraken，让它读取新的配置，然后正常使用对应的 AI 功能。使用期间保持 Magpie 运行。

后续更换模型时，在 Magpie 对应条目中重新选择即可；如果 GitKraken 界面仍显示旧模型，完全退出并重新打开 GitKraken。

插件目前只配置模型，不提供推理强度设置。
