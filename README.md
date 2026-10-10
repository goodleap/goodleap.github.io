# 项目导航首页

简洁的静态导航首页，无需安装依赖或构建，打开 `index.html` 即可查看。

## 项目入口

| 项目 | 相对链接 |
| --- | --- |
| 星辰大海 | `../stellar-voyage/` |
| 海风慢骑 | `../slow-coast-pelican/` |
| 星际闪避 | `../star-drift/` |
| 荒野回响 | `../wild-reaper/` |

首页仓库为 `goodleap/goodleap.github.io`，部署在域名根目录。以上链接分别指向同一域名下的 `/stellar-voyage/`、`/slow-coast-pelican/`、`/star-drift/` 和 `/wild-reaper/`。这些相对链接也兼容原先的 `/home/` 路径。页面不包含固定网站名，导航不绑定域名，也不使用以 `/` 开头的绝对路径。

各目标仓库需要分别配置 GitHub Pages；仅添加导航链接不会启用它的 Pages。使用自定义域名时，该域名下也需要能够访问四个目标项目的对应路径。

## 部署到 GitHub Pages

仓库已有 `.github/workflows/pages.yml` 工作流。将 `index.html` 的修改推送到 `main` 分支，会自动触发 GitHub Pages 部署；也可在 **Actions → Deploy GitHub Pages** 中手动运行。

部署过程将根目录的 `index.html` 复制到 `_site` 后上传。部署结果以对应 Actions 运行状态为准。

## 修改页面

`index.html` 是 GitHub Pages 使用的首页，`dist/index.html` 是供 Sites 使用的完全相同副本。修改根目录文件后，同步副本：

```sh
cp index.html dist/index.html
```

新增项目时，继续使用 `../项目仓库名/` 形式的相对链接。
