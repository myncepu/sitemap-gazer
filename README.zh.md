# sitemap-gazer

[README 英文版](README.md)

一个帮你轻易监控网站变更的工具。

它爬取 sitemap，保存在本地，比对上一次爬取，并生成一个 README 报告方便你查看。支持一份报告同时监控多个 sitemap。

它也可以直接在 Github Action 运行，示例： [hackerqed/sitemap-gazer-example](https://github.com/hackerqed/sitemap-gazer-example)

## 安装

```bash
pip install sitemap-gazer

mkdir sitemap-gazer-report
cd sitemap-gazer-report

sitemap-gazer init
# 创建 sitemap-gazer.json

# 编辑 sitemap-gazer.json
# 例如增加一个目标站点 crazygames.com
# {
#   "sites": [
#     {
#       "name": "crazygames.com",
#       "url": "https://crazygames.com/"
#     }
#   ],
#   "genReadme": true,
#   "output_dir": "data"
# }

sitemap-gazer
# 爬取数据，保存到 ./data/
# README.md 会自动生成
```

## 开发

运行开发版：

```bash
poetry install
poetry run sitemap-gazer
```

打包并安装：

```bash
poetry build
pip install dist/sitemap_gazer-0.1.0-py3-none-any.whl
```
