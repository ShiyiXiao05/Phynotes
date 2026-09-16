# 大学物理笔记

这是基于上海交通大学 大学物理(荣誉)系列课程编写的大学物理笔记。计划更新力学，热学，电磁学，光学，量子物理五份笔记。目前已经更新电磁学、光学和量子物理笔记。推荐使用 XeLaTeX 编译。编写过程中使用Claude Code进行了辅助排版和拼写检查等工作。

## 目录与编辑

`Electromagnetism/`、`Optics/`、`Quantum/` 分别是一份独立的笔记。每个目录中的 `Notes.tex` 是编译入口，包含导言区、封面、序言和目录，并按顺序通过 `\input` 引入 `chapters/` 下的章节文件。正文请在相应的章节文件中修改；图片放在该笔记的 `figure/` 目录下。参考文献目前保留在各自的 `Notes.tex` 末尾。

请从对应笔记目录运行编译命令，以正确找到图片和字体。例如：

```sh
cd Quantum
latexmk -xelatex -interaction=nonstopmode -halt-on-error Notes.tex
```

将 `Quantum` 换成 `Optics` 或 `Electromagnetism` 即可编译其他笔记。需要安装包含 XeLaTeX 和 `latexmk` 的 TeX 发行版。生成的 `Notes.pdf` 位于同一目录；其他编译中间文件由 `.gitignore` 排除。

光学笔记的注记环境（`noteenv`）以及部分手工插图标题（`\insertpic`）使用仓库内的 `Optics/fonts/LXGWWenKaiGB-Regular.ttf`（霞鹜文楷 GB）。光学正文仍沿用原有字体设置；编译光学笔记时需保留该字体文件及其相对路径。
