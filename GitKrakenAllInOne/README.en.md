# GitKraken All AI Features (Unified Model)

[中文](README.md)

## Purpose

Configure GitKraken's Magpie gateway connection and apply the same selected model across all six GitKraken AI features (commit message generation, explain commits, stash message generation, pull requests, conflict resolution, and commit composer) using a single Magpie plugin.

## Installation

```bash
magpie plugin add magpie-gitkraken-all-in-one
```

## Usage

1. Start Magpie and make sure the intended model provider is signed in or configured.
2. On Magpie's Agents page, enable “GitKraken 全部 AI 功能（统一模型）” and choose a model.
3. On first use, select “Custom URL” in GitKraken Preferences, not the default OpenAI service. The gateway URL is written automatically by this plugin, so you do not need to enter it manually. The API Key can be left blank without affecting normal use. To click GitKraken's “Test Connection” button, enter any non-empty value.
4. Fully quit and reopen GitKraken so it reads the updated configuration. Keep Magpie running while using GitKraken AI features.

If you want to assign different models to individual features, use the six separate feature plugins instead and do not enable this plugin at the same time to avoid overwriting each other's settings.
