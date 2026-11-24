# GitKraken Magpie Gateway and AI Model Configuration

[中文](README.md)

## Purpose

Use Magpie to choose a model independently for each of GitKraken's six AI features. Each entry controls the model for its matching feature. The “GitKraken 提交消息生成（Magpie 网关）” entry also writes the shared Magpie gateway connection, so it must be enabled before the other five entries are used.

| Magpie entry | GitKraken feature |
| --- | --- |
| GitKraken 提交消息生成（Magpie 网关） | Generates commit messages and configures the Magpie gateway connection |
| GitKraken 解释更改 | Explains commits, stashes, and other changes |
| GitKraken 贮藏消息生成 | Generates stash messages |
| GitKraken 拉取请求 | Generates pull request titles and descriptions |
| GitKraken 冲突解决 | Assists with merge-conflict resolution |
| GitKraken 提交编写器 | Assists with composing and organizing commits |

## Usage

1. Start Magpie and make sure the intended model provider is signed in or configured.
2. On Magpie's Agents page, enable “GitKraken 提交消息生成（Magpie 网关）” and choose a model. This is the prerequisite that configures GitKraken's shared Magpie gateway connection.
3. On first use, select “Custom URL” in GitKraken Preferences, not the default OpenAI service. The plugin writes the Magpie gateway URL automatically, so you do not need to enter it manually. The API Key can be left blank without affecting normal use. If you want to click GitKraken's “Test Connection” button, enter any non-empty value; the other five features need no separate key setup.
4. Enable any other GitKraken entries needed in Magpie and choose their models independently. Each entry updates only its matching feature's model and cannot configure the gateway connection on its own.
5. Fully quit and reopen GitKraken so it reads the updated configuration. Keep Magpie running while using GitKraken AI features.

To change a model later, select a new model in the matching Magpie entry. If GitKraken still displays the previous model, fully quit and reopen GitKraken.

These plugins configure models only; they do not configure reasoning effort.
