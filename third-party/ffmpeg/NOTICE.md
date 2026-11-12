# FFmpeg 运行时

首次拉片缺少 FFmpeg 时，Windows x64 客户端从 Gyan 的原始发布地址下载 FFmpeg 8.1.2 Essentials（GPLv3 构建），核对固定 SHA-256 后按独立进程调用。wdcloud 插件包本身不附带该二进制。

- 构建发布与来源信息 https://github.com/GyanD/codexffmpeg/releases/tag/8.1.2
- FFmpeg 源码 https://ffmpeg.org/download.html
- 许可证信息 https://ffmpeg.org/legal.html

## 7-Zip 解压工具

首次准备 FFmpeg 时，插件从 Igor Pavlov 的官方发行页临时下载 7-Zip 26.06 独立解压程序 7zr.exe，验证 SHA-256 后仅解包 FFmpeg 的两个可执行文件。该工具不随插件包分发。

- 7-Zip 26.06 发行、对应源码与许可证 https://github.com/ip7z/7zip/releases/tag/26.06
