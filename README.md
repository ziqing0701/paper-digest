# Paper Digest

顶刊论文精读与科研训练归档站。

## 结构

- `index.html`：归档首页
- `archive.json`：论文元数据与去重记录
- `style.css`：统一样式
- `reports/YYYY-MM-DD.html`：每期完整报告

## 自动化约定

每次定时任务执行时：

1. 检索并核验 1–2 篇高质量论文；
2. 生成 `reports/YYYY-MM-DD.html`；
3. 向 `archive.json` 追加论文元数据；
4. 聊天窗口仅返回简要摘要和完整报告链接。

GitHub Pages 建议从 `main` 分支根目录发布。
