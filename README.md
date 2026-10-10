# goodleap · 项目导航

简洁的静态导航首页，无需安装依赖或构建，打开 `index.html` 即可查看。

## 项目入口

| 项目 | 相对链接 |
| --- | --- |
| 星辰大海 | `../stellar-voyage/` |
| 海风慢骑 | `../slow-coast-pelican/` |

首页部署到 GitHub Pages 的 `/home/` 后，以上链接会分别跳转到同一域名下的 `/stellar-voyage/` 和 `/slow-coast-pelican/`。导航不绑定域名，也不使用以 `/` 开头的绝对路径。

各目标仓库需要分别配置 GitHub Pages；尤其是 `slow-coast-pelican`，仅添加导航链接不会启用它的 Pages。

## 部署到 GitHub Pages

将文件推送到本仓库的 `main` 分支后，打开 **Settings → Pages**：

1. **Source** 选择 **Deploy from a branch**。
2. **Branch** 选择 **main**，目录选择 **/ (root)**。
3. 保存，等待 GitHub Pages 完成部署。

本说明不代表 Pages 已启用或部署已完成。

## 修改页面

`index.html` 是 GitHub Pages 使用的首页，`dist/index.html` 是供 Sites 使用的完全相同副本。修改根目录文件后，同步副本：

```sh
cp index.html dist/index.html
```

新增项目时，继续使用 `../项目仓库名/` 形式的相对链接。
