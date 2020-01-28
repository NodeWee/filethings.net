---
title: '用 FFMPEG 批量转换媒体（视频、音频）文件'
layout: post/post
tags: 
    - FFMPEG
    - 转换文件
---

## &para;

`FFmpeg` 是一个开源免费跨平台的视频和音频流方案。可以通过命令行直接调用来处理媒体文件。  
FFmpeg 的安装，可参考其官方网站：[https://ffmpeg.org/](https://ffmpeg.org/)  


## &para; macOS 下批量转换视频、音频媒体文件

### 方法一，直接在终端输入命令

示例:  
```shell
for f in `ls *.aiff`; do ffmpeg -i "$f" "${f/%.aiff/.mp3}";done
```

&nbsp;

### 方法二，傻瓜式的脚本工具

**「`ffmpeg-batch-converter.sh`」**（by 穿卡芦苇）  
> 通过交互来逐步指定转换参数。减轻记忆命令的负担   
> [⬇️下载脚本](/download/ffmpeg-batch-converter_v20200128.sh)
&nbsp;&nbsp;
[💻源码](https://github.com/NodeWee/macOS-Workflow/blob/master/ffmpeg-batch-converter.sh)  

使用方法： 通过命令行运行 `bash ffmpeg-batch-converter.sh`