# 张暖阳 · 设计作品集

这是可直接部署到 GitHub Pages 的静态网站，无需安装 Node.js、运行构建命令或配置环境变量。

## 网站内容

- 主项目顺序：咕咕岛、灵馥、昆曲运动、GOODBOY、牙芽奇兵局。
- 包含高校官网 UI 作品、最新简历，以及联系页信箱中的开合动画、TD 音画海报和交互装置视频。
- 保留移动端适配、图片懒加载和按需加载的视频。

## 上传与发布

1. 新建 GitHub 仓库，例如 `portfolio`。个人免费账户可使用 Public 仓库发布 Pages。
2. 解压下载的 ZIP。**上传解压后的文件和文件夹，不要把 ZIP 本身上传到仓库。**
3. 确保仓库根目录直接包含以下内容，不要在外面再套一层 `website` 或 `portfolio` 文件夹：

   ```text
   index.html
   .nojekyll
   README.md
   assets/
   projects/
   ui/
   ```

4. 网页上传每次最多 100 个文件，单个文件最大 25 MiB。本站有 236 个文件；使用配套的 `portfolio-github-web-upload.zip` 时，按其中的说明分 3 批上传。也可以使用 GitHub Desktop 一次提交完整网站。
5. 上传完成后，进入仓库 **Settings → Pages → Build and deployment**。
6. 将 Source 设为 **Deploy from a branch**，Branch 选 **main**，目录选 **/ (root)**，点击 **Save**。如果实际上传分支名称不是 main，请选择包含这些文件的分支。
7. 等待部署完成，在 Pages 设置页面打开生成的网站链接。普通项目仓库的链接形如 `https://你的用户名.github.io/仓库名/`。

## 本版本的打包处理

- 仅打包当前页面实际使用的资源；未包含旧项目、未引用原图、开发工具或备份。
- 素材路径统一为区分大小写的平台可用的形式，包括小写 `assets/ui/`。
- 昆曲运动展示、灵馥 VR 概念、TD 音画海报使用网页压缩版 MP4，保留完整时长与音频。两个长视频的最大宽度为 1280 像素，TD 海报保留原分辨率；原始高码率视频未包含在上传包内。
- 每个文件均小于 25 MiB。页面使用相对路径，适配 GitHub Pages 的仓库子路径。
- 不需要 Git LFS；`.nojekyll` 让 Pages 直接发布静态文件。

## 常见问题

- **打开后只有 README，没有网站？** 请打开 Pages 生成的链接，不是 GitHub 仓库地址；检查根目录是否有 `index.html`。
- **页面出现了，但图片或视频缺失？** 检查 3 批是否全部上传、每批都已提交，且上传时始终在仓库根目录。不要把 `01-upload` 等批次文件夹本身传上去。
- **出现 404？** 检查 Pages 选择的分支和目录；首次部署需要等待完成。文件夹大小写不能随意改动。
- **本地预览？** 解压完整网站包后直接双击 `index.html` 即可；网页分批包需要先将三个批次的内容合并到同一文件夹。

发布前请确认愿意公开简历和联系信息。GitHub Pages 是公开网页；公开仓库里的文件也能被访问和下载。

官方说明：[上传文件与大小限制](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)、[配置 GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。
