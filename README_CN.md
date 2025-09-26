![Screenshot](https://user-images.githubusercontent.com/16438795/239653023-369442f4-e35f-4dc7-98f4-5cf7a266c2f9.png)

* 简单的 [KataGo](https://github.com/lightvector/KataGo) 分析GUI界面。请查看 [Releases](https://github.com/rooklift/ogatak/releases) 获取最新版本。
* 棋子和棋盘图形修改自 [Sabaki](https://github.com/SabakiHQ/Sabaki)，在此表示感谢。
* 概念借鉴自 [Lizzie](https://github.com/featurecat/lizzie)，受到 [KaTrain](https://github.com/sanderland/katrain)、[CGoban](https://www.gokgs.com/download.jsp) 和 [LizGoban](https://github.com/kaorahi/lizgoban) 的影响。
* 原创、独立的代码库。

## 优点

* 一旦设置完成，使用相对简单。
* 我个人喜欢这种美学设计...
* 具有大部分正常的Lizzie风格功能。
* 功能完善的SGF编辑器。
* 正确处理许多其他GUI难以处理的SGF文件，特别是让子和中盘棋盘编辑。
* 可以加载NGF、GIB和UGI文件（尽管不完美）。
* 除了Electron之外没有依赖，从源代码运行相当容易，不会引入大量的npm模块。

## 缺点

* 不包含KataGo，设置需要至少一分钟的工作。
* 基于Electron的应用程序，每个人都讨厌这些（它们很大）。

## 设置

* 下载并解压Ogatak、KataGo和KataGo权重文件。
* 在Ogatak中，选择菜单项 `Setup` `-->` `Locate KataGo...`（并找到katago.exe）
* 在Ogatak中，选择菜单项 `Setup` `-->` `Choose network...`（并找到权重文件） 

## 性能提示

* 要求KataGo提供每步归属信息的设置（参见`Analysis`菜单）相当苛刻，如果您遇到任何延迟，应该关闭它。
* 或者，考虑更改引擎报告率（参见`Setup`菜单），从默认的0.1（最密集）改为其他值。
* 由于KataGo算法和KataGo缓存之间复杂的交互，如果您以某种方式使用GUI，特别是如果您经常点击最佳移动，`wide root noise`设置可能会导致感知性能下降。它也可能影响整个文件分析速度。

## 关于分析配置文件

* KataGo需要一个分析配置文件。KataGo提供了这样的文件作为`analysis_example.cfg`，如果存在，Ogatak将使用这个文件，除非您明确指定了不同的文件。您可能会发现更改其中的一些设置会带来更好（或更差）的性能。一些人发现KaTrain作者选择的[这些设置](https://github.com/sanderland/katrain/blob/master/katrain/KataGo/analysis_config.cfg)会快一些。

## 翻译

* 目前，可以翻译大部分菜单项和一些GUI文本。请参见`src/modules/translations.js`获取说明。
* 感谢以下翻译者：ParmuzinAlexander、CGLemon、Bandysol。

## 联系我

* 您经常可以在[计算机围棋 Discord](https://discord.com/invite/5vacH5F)上找到我。
