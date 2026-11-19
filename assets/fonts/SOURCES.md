# 本地字体

[Noto Sans SC](https://github.com/google/fonts/tree/main/ofl/notosanssc) 和 [Noto Serif SC](https://github.com/google/fonts/tree/main/ofl/notoserifsc) 保留可变字重。仓库中的 TTF 是按样张字符裁出的子集。[Barlow Condensed](https://github.com/google/fonts/tree/main/ofl/barlowcondensed) 使用上游的 Medium 和 Bold。每个字体家族的 SIL Open Font License 原文随字体分发。

替换样张文案后，把所有所需文本汇总为 UTF-8 文件，再从上游 TTF 生成子集。例如：

```sh
hb-subset 'NotoSansSC[wght].ttf' --text-file=sample-text.txt \
  --unicodes+=20-ff,2000-206f,2190-21ff,25a0-25ff \
  --output-file=assets/fonts/noto-sans-sc.ttf
```

Serif 使用相同字符集。引用 `fonts.css` 即可离线渲染。新项目可以放入其世界指定的其他本地授权字体；渲染器检查浏览器实际使用的字体。
