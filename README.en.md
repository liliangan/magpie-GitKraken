# GitKraken Magpie Gateway and AI Model Configuration

[中文](README.md)

## Purpose

Configure GitKraken's Magpie gateway and AI models through Magpie. This repository offers **two usage modes (choose one and do not enable both at the same time)**:

1. **Option 1: Unified Model (1 package)**
   Install `magpie-gitkraken-all-in-one` to configure the Magpie gateway connection and apply the same model to all six GitKraken AI features from a single entry.
2. **Option 2: Per-Feature Models (6 packages)**
   Install `magpie-gitkraken-ai` (required main package that writes the shared gateway connection) along with any of the other five feature packages to choose different models independently. Enable `magpie-gitkraken-ai` before using the other five entries.

## Included Packages

| Mode | Magpie entry | npm package | Directory | GitKraken feature |
| --- | --- | --- | --- | --- |
| Unified model | GitKraken 全部 AI 功能（统一模型） | `magpie-gitkraken-all-in-one` | `GitKrakenAllInOne` | Configures the gateway and applies one model across all six AI features |
| Per-feature (main) | GitKraken 提交消息生成（Magpie 网关） | `magpie-gitkraken-ai` | `GitKrakenCommitMessage` | Generates commit messages and configures the Magpie gateway connection |
| Per-feature | GitKraken 解释更改 | `magpie-gitkraken-explain-commits` | `GitKrakenExplainCommits` | Explains commits, stashes, and other changes |
| Per-feature | GitKraken 贮藏消息生成 | `magpie-gitkraken-stash-message` | `GitKrakenStashMessage` | Generates stash messages |
| Per-feature | GitKraken 拉取请求 | `magpie-gitkraken-pull-request` | `GitKrakenPullRequest` | Generates pull request titles and descriptions |
| Per-feature | GitKraken 冲突解决 | `magpie-gitkraken-conflict-resolution` | `GitKrakenConflictResolution` | Assists with merge-conflict resolution |
| Per-feature | GitKraken 提交编写器 | `magpie-gitkraken-rebase` | `GitKrakenRebase` | Assists with composing and organizing commits |

## Installation

### Option 1: Unified Model

```bash
magpie plugin add magpie-gitkraken-all-in-one
```

### Option 2: Per-Feature Models

```bash
magpie plugin add magpie-gitkraken-ai
# Install additional feature packages as needed:
magpie plugin add magpie-gitkraken-explain-commits
magpie plugin add magpie-gitkraken-stash-message
magpie plugin add magpie-gitkraken-pull-request
magpie plugin add magpie-gitkraken-conflict-resolution
magpie plugin add magpie-gitkraken-rebase
```

## Usage

1. Start Magpie and make sure the intended model provider is signed in or configured.
2. On Magpie's Agents page, enable the plugin entry and select a model according to your chosen mode:
   - **Unified Model**: Enable “GitKraken 全部 AI 功能（统一模型）” and choose a model.
   - **Per-Feature Models**: Enable “GitKraken 提交消息生成（Magpie 网关）” first to configure GitKraken's shared Magpie gateway connection, then enable any other entries you need and choose their models independently (the other five entries cannot configure the gateway connection on their own).
3. On first use, select “Custom URL” in GitKraken Preferences, not the default OpenAI service. The plugin writes the Magpie gateway URL automatically, so you do not need to enter it manually. The API Key can be left blank without affecting normal use. If you want to click GitKraken's “Test Connection” button, enter any non-empty value; the other features need no separate key setup.
4. Fully quit and reopen GitKraken so it reads the updated configuration. Keep Magpie running while using GitKraken AI features.

To change a model later, select a new model in the matching Magpie entry. If GitKraken still displays the previous model, fully quit and reopen GitKraken.

These plugins configure models only; they do not configure reasoning effort.
