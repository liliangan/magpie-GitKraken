# GitKraken 全部 AI 功能（统一模型）

[English](README.en.md)

## 用途

通过单个 Magpie 插件一次性完成 GitKraken 的 Magpie 网关连接配置，并将同一选定模型同步应用到全部六项 GitKraken AI 功能（提交消息生成、解释更改、贮藏消息生成、拉取请求、冲突解决、提交编写器）。

## 安装

```bash
magpie plugin add magpie-gitkraken-all-in-one
```

## 使用方法

1. 启动 Magpie，并确保准备使用的模型供应商已登录或配置好。
2. 在 Magpie 的 Agent 页面启用“GitKraken 全部 AI 功能（统一模型）”，选择要使用的模型。
3. 首次接入时，在 GitKraken 偏好设置中选择“自定义 URL”，不要选择默认 OpenAI 服务。网关地址由此插件自动写入，无需手动填写；API Key 可以留空，不影响实际使用。若要点击 GitKraken 的“测试连接”按钮，填入任意非空值即可。
4. 完全退出并重新打开 GitKraken，让它读取新的配置。使用期间保持 Magpie 运行。

如果需要为六项功能分别指定不同模型，请改用六个独立功能插件，不要与本插件同时启用，以免互相覆盖配置。
