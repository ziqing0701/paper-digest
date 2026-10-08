# Figures storage and reuse policy

每周图像文件建议放到 `YYYY-Www/` 子目录，例如 `2026-W41/paper-short-title-fig2.webp`。

仅保存已经核验许可允许在公开 GitHub Pages 页面转载的图，包括核对单张 Figure 的第三方版权声明。原论文开放获取并不必然授权每张图的再发布。

在周报正文对应证据层次使用：

```html
<figure class="paper-figure">
  <a class="figure-image-link" href="../assets/figures/YYYY-Www/paper-fig2.webp" target="_blank" rel="noopener noreferrer">
    <img src="../assets/figures/YYYY-Www/paper-fig2.webp" loading="lazy" decoding="async"
         alt="Fig. 2，简述数据和轴含义">
  </a>
  <figcaption>
    <strong>原文 Fig. 2a–d：证据内容概括。</strong>
    <div class="figure-reading">具体解释坐标、关键结果、误差、能够支持的结论和下一步实验动机。</div>
    <div class="figure-source">来源：作者 / 论文 DOI / 官方 Figure 页面 · 许可：CC BY 4.0（核验后如实填写）</div>
  </figcaption>
</figure>
```

不适合转载或获取失败的图：在同一论证段落使用 `figure-link-only` 框，给出经过验证的 Figure/DOI 官方链接和内容解释，不留下失效图片。

`example-evidence.svg` 为本站原创纯示意图，仅用于确认模板显示正常，不能当作论文图。
