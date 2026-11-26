# 我的技术文档

欢迎访问我的个人文档网站。本网站使用 MkDocs 构建，通过 GitHub Actions 自动部署到 GitHub Pages。

- 作者：ak4399-ctrl
- 实践主题：静态文档自动部署
- [关于本项目](about.md)
- [使用指南](guide.md)
- [API 参考](api.md)

## 为什么写这个站点

我在实践课里学到的关键一点是：**文档的源码和最终网站不是一回事**。
`docs/` 里放的是 Markdown 源码，`site/` 是 `mkdocs build` 生成的静态网站，
真正对外提供服务的是 GitHub Pages 托管的 `site/`。

| 角色 | 内容 | 谁维护 |
| --- | --- | --- |
| 源码 | `docs/*.md`、`mkdocs.yml` | 我，手工编写 |
| 构建产物 | `site/` | `mkdocs build` 自动生成，不提交 |
| 托管 | GitHub Pages | Actions 自动上传并发布 |
