# 使用指南

1. 修改 docs 目录中的 Markdown 文件。
2. 在本地预览并检查页面及链接。
3. 提交修改并推送到 main 分支。
4. 在 Actions 页面查看构建与部署状态。
5. 打开网站检查内容是否更新。

## 常用命令

- `python -m mkdocs serve`：本地预览。
- `python -m mkdocs build --strict`：构建网站并严格检查警告。

## 一次完整流程示例

```bash
# 1. 本地预览（默认 http://127.0.0.1:8000/）
python -m mkdocs serve

# 2. 改完内容后提交
git add docs/index.md
git commit -m "更新首页说明"
git push origin main

# 3. 不需要再做任何部署操作，Actions 会自动完成
```

> 注意：`--strict` 会把警告当作错误，本地能过、CI 过不了，通常就是链接或导航写错了。
