# 翻面 · 印刷工坊美学

一个可跨 PPT、网页、UI、演示视频与动效复用的审美 skill。以纸墨、漫画光影、编辑式排版和有功能含义的物件组织设计。

基于对 [《耗时四天，我用 opus5.5 做了一款射击游戏并上架了》](https://www.bilibili.com/video/BV13MxT63EqD/) 的视觉复核而创建。它提供的是审美标准与判断方法，不限定主题、页数或技术栈。

## 使用

可在 [v1.0.0 发布页](https://github.com/yuchenlogin/flipside-design-skill/releases/tag/v1.0.0) 下载 `flipside-design.skill`。它采用 ZIP 格式；若解压工具不识别后缀，可将副本改名为 `.zip` 后解压。

将本仓库放在 Codex 的技能目录下，目录名为 `flipside-design`：

```text
~/.codex/skills/flipside-design/SKILL.md
```

如果使用自定义 `CODEX_HOME`，放入对应的 `skills/flipside-design`。已在本机安装的用户无需再次复制；若当前聊天的技能列表尚未刷新，在新聊天中调用。

直接说：

> 使用 $flipside-design 作为审美标准，帮我做一份学术论文汇报 PPT。

或：

> 使用 $flipside-design 设计这个响应式网页，保留现有内容与功能。

> 使用 $flipside-design 做一段方法介绍动效，强调“输入变成结果”的过程。

也可以写「使用翻面美学」。不用把 `.skill` 当作命令后缀；`.skill` 文件是可搬运的压缩包，解压后的 `SKILL.md` 才是技能入口。

## 它会怎样影响作品

- 暖纸色阅读面、墨黑文字、冷蓝空间、锈橙主动作。
- 粗黑标题、宋体编辑标题、窄体数字与清晰正文各司其职。
- 网点、纸纹、磨损按材料和层级使用，数据与文字保持可读。
- 根据功能选择校样、档案、工作台、比较窗或地图等组织方式。
- 根据语义使用卷轴、翻面、开窗、推近、转印、印记等动作。
- 按内容选择 Quiet、Balanced 或 Expressive 强度；不把所有作品做成游戏菜单。

## 先看什么

- [完整视觉复核报告](ANALYSIS.md)：审美判断、澄清项与具体亮点。
- [SKILL.md](SKILL.md)：供 agent 执行的简洁入口。
- [视觉系统](references/visual-system.md)：美术、字体、配色、材料与特效。
- [页面与组件](references/composition-components.md)：布局语法与组件状态。
- [动效规范](references/motion.md)：原视频动作证据和独立标注的建议参数。
- [跨媒介适配](references/media-adaptation.md)：PPT、网页、UI、视频等。
- [证据索引](references/evidence.md)：27 张静帧、14 段动作联系表。
- [设计 tokens](assets/design-tokens.json) 与 [CSS 变量](assets/flipside-tokens.css)。
- [两页学术样张](examples/academic/slides.html)：虚构数据的静态 HTML，展示这套审美如何适配信息密集的汇报。
- [响应式界面样张](examples/ui/index.html)：方法比较、选择与应用；附[桌面预览](examples/ui/desktop-selected-vs-applied.png)和 [360 px 窄屏预览](examples/ui/mobile-360.png)。下载 HTML 后可直接在浏览器打开。
- [验证记录](VALIDATION.md)：技能校验、配色对比度与独立前向测试。

## 证据边界

本次复核使用公开视频的 768 × 480 / 30 fps 版本。能确认字体角色、材料、排版与动作过程；不能从视频恢复原字体文件、shader 实现或作者的精确动画参数。建议字体、色值和时长均明确标为复用方案。

作者水印、视频字幕、浏览器提示不属于游戏设计。参考截图与联系表属于来源分析资料，保留原作者归属，不作为可复制到新项目中的通用美术素材。本仓库不对源视频、游戏角色、商标或截图授予许可。

版本：1.0.0 · 完成日期：2026-10-30。变更记录见 [CHANGELOG.md](CHANGELOG.md)。
