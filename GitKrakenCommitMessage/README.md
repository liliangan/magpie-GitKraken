# GitKraken 提交消息生成（Magpie 网关）

[English](README.en.md)

## 用途

为 GitKraken 的提交消息生成功能单独选择模型，并设置所有 GitKraken AI 功能共用的 Magpie 网关连接。

## 使用方法

1. 在 Magpie 的 Agent 页面启用“GitKraken 提交消息生成（Magpie 网关）”，选择用于生成提交消息的模型。
2. 首次接入时，在 GitKraken 偏好设置中选择“自定义 URL”，不要选择默认 OpenAI 服务。网关地址由此插件自动写入，无需手动填写；API Key 可以留空，不影响实际使用。若要点击 GitKraken 的“测试连接”，填入任意非空值即可。
3. 在 GitKraken 中使用提交消息生成功能。更换此功能的模型时，在 Magpie 中重新选择模型。

其他五个 GitKraken 功能插件共用此处配置的网关连接；启用它们前，请先完成上述连接配置。
