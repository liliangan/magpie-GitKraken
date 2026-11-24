# GitKraken Commit Message Generation (Magpie Gateway)

[中文](README.md)

## Purpose

Choose a model specifically for GitKraken commit message generation. This is also the main entry that configures the Magpie gateway connection shared by all GitKraken AI features.

## Usage

1. On Magpie's Agents page, enable “GitKraken 提交消息生成（Magpie 网关）” and choose a model for commit message generation.
2. On first use, select “Custom URL” in GitKraken Preferences, not the default OpenAI service. This plugin writes the gateway URL automatically, so you do not need to enter it manually. The API Key can be left blank without affecting normal use. To click GitKraken's “Test Connection” button, enter any non-empty value.
3. Use GitKraken's commit message generation feature. To change its model, choose a different model in Magpie.

The other five GitKraken feature plugins use the gateway connection configured here. Complete this connection before enabling them.
