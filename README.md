# my-docs

使用 **MkDocs Material** 编写的技术文档，并通过 **GitHub Actions** 自动部署到 **GitHub Pages**。

- 网站地址：<https://ak4399-ctrl.github.io/my-docs/>
- 个人实验报告：[report/README.md](report/README.md)

## 目录结构

```text
.
├── .github/workflows/deploy.yml   # 推送 main 后自动构建并部署
├── docs/                          # 文档源码（4 页）
├── mkdocs.yml                     # MkDocs 配置与导航
├── requirements.txt               # 构建依赖
└── report/                        # 实验报告与截图
```

## 本地预览

```bash
python -m venv .venv
source .venv/Scripts/activate      # Windows Git Bash；PowerShell 用 .\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m mkdocs serve             # 打开 http://127.0.0.1:8000/
```

构建静态站点（产物在 `site/`，已被 `.gitignore` 忽略）：

```bash
python -m mkdocs build --strict
```
