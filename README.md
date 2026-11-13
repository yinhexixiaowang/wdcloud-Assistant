# wdcloud-Assistant
wdcloud助手

## 安装

在 Harness Desktop 中打开插件页面，添加 https://github.com/yinhexixiaowang/wdcloud-Assistant.git 并启用。

安装并启用后，在 Harness 聊天发送「召唤 wdcloud」。插件会尝试用记事本打开本地激活文件，未打开时可使用回复中的路径。把原有 wdCloud CDKEY 粘贴到第一行并保存，再发一次「召唤 wdcloud」。验证成功后会显示到期时间并清空文件。请勿在聊天中发送 CDKEY。视频拉片已内置。首次拉片会检测 FFmpeg。Windows x64 缺少 FFmpeg 时会联网下载固定版本、校验并缓存。

## 离线使用

成功激活或续期后，签名租约有效期内可断网重启并恢复，最长 24 小时。租约到期后需联网续期。

## 拉片输出

从 v0.8.0 起，duration_ms 表示本次分析窗口长度，source_duration_ms 可另记原片总长。sections 概括连续镜头的叙事段落，props 可记录道具的开镜状态，narrative 是可选的一句话总览。旧 JSON 仍可校验，并提示缺少段落。拉片仅分析画面和字幕。

从 v0.8.1 起，贴纸、标题、字幕和水印的变化单独发生时不计为切镜。boundary_basis 记录段落边界依据，camera_actions 单独记录摄影机运动。

## 0.9.0 拉片与已知限制

- wdcloud_video_outline 提供零图像 token 的文本地图。wdcloud_video_read 读取字幕轨、字幕文件或画面 OCR。分镜、地图与字幕工具共用切点候选。
- 烧录字幕需要可用的外部 OCR。配置 DSH_OCR_CMD 为可执行文件的绝对路径，工具会传入图片路径并读取 UTF-8 标准输出。未配置时尝试 PATH 中的 Tesseract，中文需要 chi_sim 语言数据。采样时刻仅表示画面证据，真实中文识别率尚待验收。
- 不分析声音。填写 start_state 前使用 zoom 的 at: "start" 核验开镜画面。
- 带 sections 的 JSON 现在默认严格校验。这是破坏性变更，校验历史段落可显式传 strict: false。

### 文本地图标签

「疑似叠层」来自既有局部变化信号，不能区分字幕与非文字贴纸。请用字幕读取或抽帧核实。
