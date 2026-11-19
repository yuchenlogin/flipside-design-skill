# 运行评测

从仓库根目录执行以下命令。需要 Node.js 22+ 和 Google Chrome。首次准备依赖后可断网运行。

```sh
npm ci --prefix tools
tools/render evals/suite.json /tmp/inkworks-current
tools/render evals/legacy.json /tmp/inkworks-legacy
```

也可以安装工具锁定的 Chromium：`cd tools && npx playwright-core install chromium`。使用该浏览器时，给渲染命令加上 `INKWORKS_BROWSER=bundled`。

每个 manifest 给出画布宽高、页面 ID 和文件路径。路径相对于 manifest 中的 `root`（默认是 manifest 所在目录的上一级）。单页可覆盖 `width`、`height`、`settle`（毫秒，须大于 600）。`stylesheets` 用于还原 HTML 片段的宿主样式。渲染器只提供本地文件并阻断外部请求，缺文件、页面异常、可见文本回退到系统字体都会导致失败。

- `contact-sheet.jpg` 比较最终构图。各页的 `final.jpg` 保留原始画布尺寸。
- `frames.jpg` 将每页的 0、150、300、600 ms 排为一行。JS 使用虚拟时钟，CSS/WAAPI 动画按其本地时间轴取样；可用页面条目中的 `trigger` 指定真实点击。对单页使用 `settle` 可延长默认 1600 ms 终态。
- `without-text.jpg` 隐去 HTML 和 SVG 文字检查主角；图像内的字应在原稿中另行隐藏。
- `metrics.json` 记录浏览器版本、真实绘制字体及归一化包围盒。给 3–7 个主要对象加 `data-shape`，给主角加 `data-hero`。缺少 `data-shape` 时仍使用标题、图形、区域子元素推断，报告会注明。
- 按包围盒面积分三档，投到 12×8 网格上，比较每个格子占用面积的交并比。相同布局得 1，默认 ≥0.72 提醒复看。相同语义或构图仍应由人核对。这个值不衡量原创性或审美质量。

## 新旧版本盲评

每个版本独立用 `suite.json` 同一组 `brief` 生成六件作品，另做同一海报的第二个世界。不可向生成者展示另一版本作品。为各自输出各写一份 manifest，使用相同 ID、画布、时间点和渲染设置。

```sh
tools/blind /tmp/inkworks-old /tmp/inkworks-current /tmp/inkworks-blind
```

将盲评目录的 `ballot/` 交给评者。按项目分别查阅 A、B 的最终画面、遮字图和帧序列，参照评分表给分并写理由。回收评分后再打开同级 `key.json`。修订时保留两轮评分与改动记录。

## 为交互定义时间零点

在页面条目中加入 `"trigger": {"click": "#press"}`。页面与本地字体就绪后，渲染器向该元素发出真实鼠标点击，随后截取第 0 帧。减弱动态复测会重载页面并执行同一个输入。每个选择器必须唯一且可点击。省略 `trigger` 时仍从页面入场开始取样。以 250 ms 定时器启动一个 1000 ms 动画为例，300 ms 帧只应呈现其前 50 ms。作者主动暂停的动画保留暂停位置。

同一输出目录一次只接受一个渲染进程，第二个进程会报错。异常终止后若留有同名 `.lock` 空目录，确认没有写入进程后再删除锁目录或换用新的输出路径。

每个页面另存 `reduced.jpg`，用于核对系统减弱动态时的最终信息。设置环境变量 `INKWORKS_FILM=1` 可额外写出 `film/*.jpg`，每 50 ms 一帧（20 fps），供制作动效预览。

## 验证同一项目的页间变化

`tools/render evals/series.json /tmp/inkworks-series` 会复现三页车门开闭小样。页码可实际跳转。通过[世界设定](series/world.md)定位每页主角、相邻构图和动作池的覆盖。
