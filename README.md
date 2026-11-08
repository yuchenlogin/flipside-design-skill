# 翻面 · 印刷工坊美学

从主题和功能构思设计，用形体、线条、光影、材料、排版与因果动效形成完整表达。可用于 PPT、网页、UI、演示视频和静态视觉作品。

基于对 [《耗时四天，我用 opus5.5 做了一款射击游戏并上架了》](https://www.bilibili.com/video/BV13MxT63EqD/) 的画面分析与实际使用反馈。

## v2 的设计重点

准星页的压印机把样本、承接位置、操作把手和结果纸签组织成同一套关系。方架承担支撑，圆柱与圆盘交代运动，球形把手提示接触，纸签提供可读结果。光线、轮廓与尺度差让这个概念成为有分量的画面。

v2 将这种从功能到形体、再到视觉与动作的推导写入 skill 的主要执行流程。

- 从当前内容寻找值得被看见的操作或关系，发展适合它的主视觉与构图。
- 根据支撑、运动、接触、柔韧性安排直线与曲线、棱角与圆滑、厚重与轻薄。
- 区分轮廓、遮挡、结构、信息和纹理线，协调受光面、投影与接触阴影。
- 让动作遵循对象的结构，保持输入与结果的身份连续。
- Quiet、Balanced、Expressive 都保留概念、造型、光线和构图的完成度。
- 以完成画面和关键操作检查泛化，使用颜色、字体和参数前先完成设计判断。

## 使用

本机已安装时，可以在新聊天中直接调用。

> 使用 $flipside-design 作为审美标准，帮我做一份学术论文汇报 PPT。

> 使用 $flipside-design 设计这个网页，围绕它的实际功能发展有特点的视觉概念。

> 使用 $flipside-design 做一段方法介绍动画，体现输入、作用过程与结果之间的关系。

也可以写「使用翻面美学」。调用名称保持 `$flipside-design`。

可从 [v2.0.0 发布页](https://github.com/yuchenlogin/flipside-design-skill/releases/tag/v2.0.0) 下载 `flipside-design.skill`。文件采用 ZIP 格式，解压后将 `flipside-design` 文件夹放入技能目录。解压工具若无法识别后缀，可把副本改名为 `.zip`。

```text
~/.codex/skills/flipside-design/SKILL.md
```

使用自定义 `CODEX_HOME` 时，放入对应的 `skills/flipside-design`。

## 阅读与复用

- [SKILL.md](SKILL.md) 提供执行入口。
- [概念推导](references/design-reasoning.md) 从准星装置、光学窗和沙盘推导跨领域构思方法。
- [形体、线条、光线与空间](references/form-light-space.md) 说明棱角、曲率、轮廓、材料与明暗怎样共同设计。
- [动效](references/motion.md) 从对象身份、约束、作用和结果推导动作，并保留源片段。
- [页面与组件](references/composition-components.md)、[跨媒介适配](references/media-adaptation.md) 提供具体场景中的决策依据。
- [视觉系统](references/visual-system.md) 与 [tokens](assets/design-tokens.json) 提供字体、材料和配色起点。
- [审美验收](references/evaluation.md) 用完成画面检查概念与执行质量。
- [完整视觉复核报告](ANALYSIS.md) 解释源观察与本次深化，[证据索引](references/evidence.md) 收录 27 张静帧和 14 组动作联系表。
- [验证记录](VALIDATION.md) 记录版本、任务、实际产物、检查范围与不足。

## v2 实际样张

两组独立构思用于检查跨任务迁移，数据与素材均为虚构示例。下载 HTML 后可直接在浏览器打开。

- [章节编排工具](examples/v2/editor/index.html) 把时间结构呈现为可重排的纸带，支持选择、改序与文本预览。查看[桌面画面](examples/v2/editor/desktop-final.png)、[重排结果](examples/v2/editor/desktop-verified.png)和[窄屏画面](examples/v2/editor/mobile-360.png)。
- [雨水花园原理汇报](examples/v2/rain-garden/index.html) 用带厚度的连续剖面解释水的路径，以共同尺度比较分配。查看[第一页](examples/v2/rain-garden/page-1.jpg)和[第二页](examples/v2/rain-garden/page-2.jpg)。

## 来源与适用范围

源视频分析基于 768 × 480 / 30 fps 版本。原始字体文件、渲染实现与精确动画曲线仍未取得。概念与造型规律属于基于画面的设计解释，字体、色值、时长属于迁移建议。

参考截图与联系表保留原作者归属，仅用于分析核对。制作新作品时使用原创内容或用户提供的素材。源视频、游戏角色、商标与截图的权利归原权利人。

v2.0.0 · 2026-11-08。版本变更见 [CHANGELOG.md](CHANGELOG.md)。
