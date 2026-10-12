# 概述

本仓库是天邈汉化组 《无主之地：前奏》汉化 v1.43
所有版权归属[天邈汉化组](https://keylol.com/t114561-1-1)

为了避免网盘失效或收费  而上传此汉化文件

# 使用方法

1. 下载本仓库 并覆盖 `BorderlandsPreSequel` 原游戏的三个文件夹
2. 修改`BorderlandsPreSequel/WillowGame/Config/DefaultEngine.ini`中的`[Engine.Engine]`
```
MediumFontName=chFont.Mid
LargeFontName=chFont.Mid
SubtitleFontName=chFont.Mid
```
即可生效

## Linux下覆盖文件提示
先进入原游戏目录 将所有文件名转为小写。
再进入本项目将所有文件名转为小写 并覆盖原文件
参考脚本
```
find . -depth | while IFS= read -r item; do
    dir=$(dirname "$item")
    base=$(basename "$item")
    lower_base=$(echo "$base" | tr '[:upper:]' '[:lower:]')
    if [ "$base" != "$lower_base" ]; then
        mv "$dir/$base" "$dir/$lower_base"
    fi
done
```
