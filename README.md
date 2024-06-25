<!--
 * @Author: xushengyichn xushengyichn@outlook.com
 * @Date: 2024-03-03 16:07:17
 * @LastEditors: xushengyichn xushengyichn@outlook.com
 * @LastEditTime: 2024-06-25 23:05:58
 * @FilePath: \TongjiThesis\README.md
 * @Description: 
 * 
 * Copyright (c) 2024 by ${git_name_email}, All Rights Reserved. 
-->
# TongjiThesis
## 总览
个人自用同济大学硕博士论文LaTeX模板。
本人并没有LaTeX格式编写经验，所以这个模板的编写主要参考了前辈的模板，并基于[同济大学学位论文写作规范（20231228更新）](https://gs.tongji.edu.cn/info/1063/1754.htm)对前辈的模板进行了修改。本模板的编写主要是为了方便自己的毕业论文写作，所以可能不够完善，目前只是一个初步的版本。

## 使用说明
__注意：__ 采用`biber`编译参考文献。
### 安装
推荐使用 [Texlive](https://mirrors.tuna.tsinghua.edu.cn/ctan/systems/texlive/Images/)，直接在[tuna](https://mirrors.tuna.tsinghua.edu.cn/ctan/systems/texlive/Images/)下载很快的。


### 使用（一定要仔细看啊）
主文件为 `thesis.tex`，该文档头部说明了本模板的所有选项（包含 __数字式引用及作者年份引用的切换选项__，默认使用数字上标的引用格式）。

1. 基本的编译步骤是：`tex,biber,tex,tex`(这里的tex替换成你常用的`tex`，如`xelatex`)。一般的前端都可以定制成一键运行这些步骤，如emacs的`C-c C-a`，vscode的 LaTeX Workshop 插件，WinEdt自带的编译按键等。
1. 首选`xelatex`编译，次选`pdflatex`，`lualatex`貌似也能用。
1. 使用`xelatex`时，如果提示缺少某字体，不要慌，请参考下面的字体安装说明。
2. 增加魔术注释，默认 pdflatex biber pdflatex pdflatex,可以删除注释采用编译器默认方式编译。
### 字体安装注意事项：
  1. 可在[此处](https://github.com/marquistj13/TongjiThesis/issues/18)下载安装。
  2. 或者自己想办法下载安装（各种系统对应的字库详见： [ctex 宏集文档](https://ctan.org/pkg/ctex)。如果你用的是windows系统，可以搜索中易的对应字体下载，如中易隶书，Mac系统的字体则是华文字库，且其隶书的设置较为复杂，详见下节的配置。）
  3. 对于`windows系统`而言，如果不想安装字体的话，可参考 [自动进行字体配置+pifont](https://github.com/marquistj13/TongjiThesis/commit/8d88c8fce195e78d9d485a6b65eae5867582e243)的修改，将`tongjithesis.cls`中的这一行：`\IfFileExists{/dev/null}{}{\PassOptionsToClass{fontset=windowsold}{ctexbook}}` 删掉。


主要参考资料：
* [TongjiThesis](https://github.com/marquistj13/TongjiThesis)


## 本模板对老模板的主要改动
相较于老版tongjithesis，目前改动如下:
1. 修改新版写作规范对封面的要求（目前仅修改了学术学位部分）
2. 在thesis.tex增加魔术注释，方便编译
3. 根据2024年6月时的模板要求，将页眉居中