---
layout: post/post
title: 用 FFMPEG 批量转换媒体（视频、音频）文件
uuid: 4AD174FA-1E36-4D92-ACE7-63FC02FA5D6B
tags: 
 - FFMPEG
 - 转换文件
---
> 最后更新于：2020-02-08





<center class="hr-sect">§</center>

`FFmpeg` 是一个开源免费跨平台的视频和音频流方案。可以通过命令行直接调用来处理媒体文件。    
FFmpeg 的安装，可参考其官方网站：[https://ffmpeg.org/](https://ffmpeg.org/)

<center class="hr-sect">§</center>

## macOS 下批量转换视频、音频媒体文件

### 方法一，直接在终端输入命令

示例:  
```shell  
for f in `ls *.aiff`; do ffmpeg -i "$f" "${f/%.aiff/.mp3}";done  
```

<hr>

### 方法二，傻瓜式的脚本工具

**「`ffmpeg-batch-converter.sh`」**（by 穿卡芦苇）      
> 通过交互来逐步指定转换参数。减轻记忆命令的负担       
> [⬇️下载脚本](/download/ffmpeg-batch-converter_v20200128.sh)&nbsp;&nbsp;[💻源码](https://github.com/NodeWee/macOS-Workflow/blob/master/ffmpeg-batch-converter.sh)  

使用方法： 通过命令行运行 `bash ffmpeg-batch-converter.sh`


