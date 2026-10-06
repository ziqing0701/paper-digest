# Paper Digest

顶刊论文精读与科研训练归档站。

## 结构

- `index.html`：归档首页
- `archive.json`：论文元数据、去重记录与周报定位
- `style.css`：统一样式
- `reports/YYYY-Www.html`：每个 ISO 自然周一个完整周报，例如 `reports/2026-W41.html`

## 自动化约定

定时任务在每周二、周四、周六和周日执行。每次运行时：

1. 读取 `archive.json`，检查历史 DOI、标题和主题，避免重复；
2. 检索并核验 1–2 篇高质量论文；
3. 计算当天所属 ISO 周；
4. 若本周周报不存在，则创建 `reports/YYYY-Www.html`；
5. 若本周周报已存在，则读取后在保留原内容的基础上追加当天日期区块，并更新顶部目录；
6. 向 `archive.json` 追加论文元数据；
7. 每篇论文的 `report_url` 指向本周周报中的当天锚点，例如：
   `https://ziqing0701.github.io/paper-digest/reports/2026-W41.html#2026-10-06`
8. 聊天窗口只返回简短摘要、当天区块直达链接和归档首页。

同一自然周只维护一个 HTML 文件。周一至周日按 ISO 周计算，进入下一自然周后创建新的周报文件。

GitHub Pages 从 `main` 分支根目录发布。

归档首页：
https://ziqing0701.github.io/paper-digest/
