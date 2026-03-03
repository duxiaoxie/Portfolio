# Portfolio

## 上传大文件 (Uploading Large Files)

本仓库已配置 **Git LFS（Large File Storage）**，支持上传视频、图片、音频等大文件。

### 前置准备

1. 安装 Git LFS：
   - **macOS**：`brew install git-lfs`
   - **Windows**：从 [git-lfs.com](https://git-lfs.com) 下载安装程序
   - **Linux（Ubuntu/Debian）**：`sudo apt-get install git-lfs`

2. 在本地仓库启用 Git LFS：
   ```bash
   git lfs install
   ```

### 上传大文件步骤

1. 克隆仓库（如尚未克隆）：
   ```bash
   git clone https://github.com/duxiaoxie/Portfolio.git
   cd Portfolio
   ```

2. 将大文件复制到仓库目录中。

3. 提交并推送文件，Git LFS 会自动处理已在 `.gitattributes` 中配置的文件类型：
   ```bash
   git add 你的大文件
   git commit -m "Add large file"
   git push origin main
   ```

### 追踪自定义文件类型

如需追踪 `.gitattributes` 中未包含的文件类型，可手动添加：

```bash
git lfs track "*.your_extension"
git add .gitattributes
git commit -m "Track *.your_extension with Git LFS"
```

### 已配置的文件类型

`.gitattributes` 文件已预先配置以下类型通过 Git LFS 追踪：

- **图片**：`.png`, `.jpg`, `.jpeg`, `.gif`, `.bmp`, `.tiff`, `.ico`, `.webp`
- **视频**：`.mp4`, `.mov`, `.avi`, `.mkv`, `.wmv`, `.flv`, `.webm`
- **音频**：`.mp3`, `.wav`, `.flac`, `.aac`, `.ogg`
- **压缩包**：`.zip`, `.tar`, `.tar.gz`, `.rar`, `.7z`
- **设计文件**：`.pdf`, `.psd`, `.ai`, `.sketch`
- **字体**：`.ttf`, `.otf`, `.woff`, `.woff2`
- **3D 资源**：`.fbx`, `.obj`, `.blend`

### 注意事项

- GitHub 免费账户的 Git LFS 存储空间为 **1 GB**，每月带宽为 **1 GB**。
- 如需更多空间，可在 GitHub 账户设置中购买额外的 LFS 存储包。
- 更多信息请参阅 [GitHub Git LFS 文档](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage)。