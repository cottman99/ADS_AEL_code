# ADS自定义布局函数库

[English Version](README.md)

## 项目描述
这是一个基于ADS（Advanced Design System）的布局函数库，使用AEL（Application Extension Language）编写。该工具集提供了一系列用于自动生成各种电感结构的函数，包括多圈八边形电感、交叉结构和端子的布局功能。

## 功能特点
- 多圈电感生成，支持自定义参数
- 八边形电感布局，尺寸可配置
- 支持单圈和多圈电感结构
- 自动处理多层设计中的交叉结构
- 可自定义端子配置
- 中空矩形和专用八边形绘制功能
- 灵活的层管理（导线层、底层、过孔层）
- 参数化控制：
  - 圈数
  - 圈间距
  - 导线宽度
  - 拐角系数
  - 端子尺寸

## 安装说明
```AEl
1. 将所有.ael文件复制到您的ADS工作空间
2. 在ADS中加载所需函数：
   load("include.ael");
   # 或根据需要加载单个函数
```

## 使用方法
```scheme
# 示例：绘制多圈电感
draw_inductor_multi_ring(
    centerX,            # 中心X坐标
    centerY,            # 中心Y坐标
    Nturns,            # 圈数
    spacing,           # 圈间距
    lengthX,           # X方向长度
    lengthY,           # Y方向长度
    cornerK,           # 拐角系数
    pathWidth,         # 导线宽度
    wireLayerName,     # 导线层名称
    underLayerName,    # 底层名称
    viaLayerName,      # 过孔层名称
    terminalmode,      # 端子模式
    terminalWidth,     # 端子宽度
    terminalLength,    # 端子长度
    terminalGap,       # 端子间隙
    intersection_spacing_ratio  # 交叉结构间距比例
);
```

## 贡献指南
欢迎提交Pull Request来贡献代码！

## 开源协议
本项目采用 MIT 协议开源 - 查看 [LICENSE](LICENSE) 文件了解更多信息。

## 作者信息
- 作者：PhiChi
- 知乎：[PATactics](https://www.zhihu.com/people/flyzi-you-58)

## 致谢
特别感谢是德科技（Keysight）开发的优秀 ADS（Advanced Design System）软件。 