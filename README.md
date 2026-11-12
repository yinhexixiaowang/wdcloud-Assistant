# wdcloud-Assistant
wdcloud助手

## 安装

在 Harness Desktop 中打开插件页面，添加 https://github.com/yinhexixiaowang/wdcloud-Assistant.git 并启用。

安装并启用后，在 Harness 聊天发送「召唤 wdcloud」。插件会尝试用记事本打开本地激活文件，未打开时可使用回复中的路径。把原有 wdCloud CDKEY 粘贴到第一行并保存，再发一次「召唤 wdcloud」。验证成功后会显示到期时间并清空文件。请勿在聊天中发送 CDKEY。视频拉片已内置。首次拉片会检测 FFmpeg。Windows x64 缺少 FFmpeg 时会联网下载固定版本、校验并缓存。

## 离线使用

成功激活或续期后，签名租约有效期内可断网重启并恢复，最长 24 小时。租约到期后需联网续期。

## 拉片输出

从 v0.8.0 起，duration_ms 表示本次分析窗口长度，source_duration_ms 可另记原片总长。sections 概括连续镜头的叙事段落，props 可记录道具的开镜状态，narrative 是可选的一句话总览。旧 JSON 仍可校验，并提示缺少段落。拉片仅分析画面和字幕。
