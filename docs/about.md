# 关于本项目

## 项目目标

实现从 Markdown 文档到公开网站的自动化发布：推送到 `main` 之后，不再手工上传任何文件。

## 技术组成

| 工具 | 作用 |
| --- | --- |
| Markdown | 编写文档内容 |
| MkDocs Material | 将文档构建成静态网站 |
| GitHub Actions | 自动执行安装、构建和部署 |
| GitHub Pages | 托管并提供网站访问地址 |

## 我的理解

我原本以为"部署"需要自己把生成的 HTML 传上去，实际做完才发现：
Actions 里的 `upload-pages-artifact` 只是把 `site/` 打成 artifact，
真正的发布由 `deploy-pages` 完成，而且 `deploy` 任务必须 `needs: build`，
保证构建成功才发布——这就是"源码 → 构建产物 → 托管网站"三段式的自动化。
