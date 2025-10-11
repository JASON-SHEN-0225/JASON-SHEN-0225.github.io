# 光影集 - 申家铖摄影作品集网站

## 项目简介
这是一个个人摄影作品集静态网站，用于展示摄影师申家铖（Jason Shen）的照片和视频作品。网站支持中英文双语切换、媒体文件分页浏览、灯箱放大查看等功能，采用现代简约设计风格，适配移动端和桌面端。

### 核心功能
- 照片/视频作品分页展示（每页1项，支持键盘左右箭头导航）
- 中英文双语自动切换，包含页面标题、导航、描述等全量翻译
- 媒体文件灯箱放大查看（支持ESC关闭和背景点击关闭）
- 滚动动画效果（区域淡入、打字机文字动画、模态框过渡）
- 微信二维码模态框（含打开/关闭动画）
- 基于GitHub API动态加载媒体文件（按更新时间排序）

## 安装步骤
1. **克隆仓库**  
   执行命令 `git clone https://github.com/JASON-SHEN-0225/JASON-SHEN-0225.github.io.git`，将项目克隆到本地。

2. **环境准备**  
   无需额外安装依赖（核心资源通过CDN加载），仅需：
   - 现代浏览器（Chrome、Firefox、Safari等）
   - 本地服务器工具（如VS Code的Live Server插件，推测）用于预览。

3. **文件结构确认**  
   确保项目根目录包含以下关键文件：
   - `index.html`：网站主入口文件
   - `check.html`：状态检查页面（导航栏链接指向）
   - `favicon.ico`：网站图标
   - `photos/` 目录：存放摄影作品图片
   - `videos/` 目录：存放视频作品文件
   - `wechat.png`：微信二维码


## 运行方式
### 本地预览
1. 打开项目根目录，使用本地服务器工具启动服务（如VS Code右键选择“Open with Live Server”）。
2. 在浏览器中访问 `http://localhost:5500`（端口号以实际工具配置为准），即可查看网站效果。

### 线上部署
1. 将项目推送到GitHub仓库（需与代码中配置的`GITHUB_USER`和`REPO_NAME`一致）。
2. 在GitHub仓库设置中开启“GitHub Pages”，选择`main`分支作为源，等待部署完成。
3. 通过 `https://[GITHUB_USER].github.io/[REPO_NAME]/` 访问线上网站。

## 参数配置
核心配置项位于`index.html`的`<script>`标签内，可根据需求修改：

| 配置参数 | 说明 | 默认值 |
|----------|------|--------|
| `GITHUB_USER` | GitHub用户名（用于加载媒体文件） | `JASON-SHEN-0225` |
| `REPO_NAME` | GitHub仓库名 | `JASON-SHEN-0225.github.io` |
| `BRANCH` | 分支名称 | `main` |
| `IMAGE_EXTENSIONS` | 支持的图片格式 | `['jpg', 'jpeg', 'png', 'gif', 'webp']` |
| `VIDEO_EXTENSIONS` | 支持的视频格式 | `['mp4', 'webm', 'mov']` |

## 示例用法
### 1. 浏览作品
- 首页点击“浏览作品集”按钮，跳转至照片展示区。
- 点击照片可打开灯箱放大查看，点击“上一张/下一张”或使用键盘左右箭头切换作品。
- 切换至“视频”标签页，可播放视频作品（支持暂停、音量调节等默认控制）。

### 2. 切换语言
- 桌面端点击导航栏右侧“ENG/中”按钮，移动端点击菜单按钮旁的语言图标，可切换中英文显示。

### 3. 联系摄影师
- 滚动至“联系”区域，可查看邮箱、电话信息。
- 点击“微信”图标，弹出二维码模态框，扫描可添加联系方式。

## 注意事项
1. **媒体文件管理**  
   - 新增照片/视频需放入对应`photos/`或`videos/`目录，文件命名建议简洁（将作为作品标题显示）。
   - 媒体文件更新后，GitHub API可能存在缓存，需等待几分钟后刷新网站生效。

2. **API访问限制**  
   - 免费GitHub API存在访问频率限制，若出现“无法加载作品”提示，可等待10-15分钟后重试。

3. **浏览器兼容性**  
   - 不支持IE浏览器，建议使用Chrome 80+、Firefox 75+等现代浏览器以确保动画效果正常。

---

# Light & Shadow - Jason Shen Photography Portfolio Website

## Project Introduction
This is a personal photography portfolio static website, designed to showcase photographer Jason Shen's photo and video works. The website supports bilingual switching (Chinese/English), paginated media browsing, lightbox zoom-in viewing, and adopts a modern minimalist design that is responsive to both mobile and desktop devices.

### Core Features
- Paginated display of photos/videos (1 item per page, supporting keyboard arrow navigation)
- Automatic bilingual switching (Chinese/English) with full translation of page titles, navigation, and descriptions
- Lightbox zoom-in for media files (supports ESC close and background click close)
- Scroll animation effects (section fade-in, typewriter text animation, modal transition)
- WeChat QR code modal (with open/close animations)
- Dynamic media loading via GitHub API (sorted by update time)

## Installation Steps
1. **Clone the Repository**  
   Run the command `git clone https://github.com/JASON-SHEN-0225/JASON-SHEN-0225.github.io.git` to clone the project to your local machine.

2. **Environment Preparation**  
   No additional dependencies are required (core resources are loaded via CDN), only:
   - A modern browser (Chrome, Firefox, Safari, etc.)
   - A local server tool (e.g., VS Code's Live Server extension, assumed) for preview.

3. **File Structure Check**  
   Ensure the project root directory contains the following key files:
   - `index.html`: Main entry file of the website
   - `check.html`: Status check page (linked from the navigation bar)
   - `favicon.ico`: Website icon 
   - `photos/` directory: Stores photography works 
   - `videos/` directory: Stores video works 
   - `wechat.png`: Wechat QRcode icon


## Running Methods
### Local Preview
1. Open the project root directory and start a service using a local server tool (e.g., right-click in VS Code and select "Open with Live Server").
2. Access `http://localhost:5500` in your browser (port number depends on the actual tool configuration) to view the website.

### Online Deployment
1. Push the project to a GitHub repository (must match `GITHUB_USER` and `REPO_NAME` configured in the code).
2. Enable "GitHub Pages" in the GitHub repository settings, select the `main` branch as the source, and wait for deployment to complete.
3. Access the online website via `https://[GITHUB_USER].github.io/[REPO_NAME]/`.

## Parameter Configuration
Core configuration items are located in the `<script>` tag of `index.html` and can be modified as needed:

| Configuration Parameter | Description | Default Value |
|-------------------------|-------------|---------------|
| `GITHUB_USER` | GitHub username (for loading media files) | `JASON-SHEN-0225` |
| `REPO_NAME` | GitHub repository name | `JASON-SHEN-0225.github.io` |
| `BRANCH` | Branch name | `main` |
| `IMAGE_EXTENSIONS` | Supported image formats | `['jpg', 'jpeg', 'png', 'gif', 'webp']` |
| `VIDEO_EXTENSIONS` | Supported video formats | `['mp4', 'webm', 'mov']` |

## Usage Examples
### 1. Browsing Works
- Click the "Browse Portfolio" button on the homepage to jump to the photo display section.
- Click a photo to open the lightbox for zoom-in viewing; click "Previous/Next" or use keyboard arrow keys to switch works.
- Switch to the "Videos" tab to play video works (supports default controls like pause and volume adjustment).

### 2. Switching Languages
- On desktop: Click the "ENG/中" button on the right side of the navigation bar.
- On mobile: Click the language icon next to the menu button to switch between Chinese and English.

### 3. Contacting the Photographer
- Scroll to the "Contact" section to view email and phone information.
- Click the "WeChat" icon to open a QR code modal; scan the code to add contact information.

## Notes
1. **Media File Management**  
   - New photos/videos must be placed in the corresponding `photos/` or `videos/` directory; file names are recommended to be concise (they will be displayed as work titles).
   - After updating media files, the GitHub API may have caching; wait a few minutes and refresh the website to take effect.

2. **API Access Limits**  
   - The free GitHub API has access rate limits. If a "Failed to load works" message appears, wait 10-15 minutes and try again.

3. **Browser Compatibility**  
   - IE browser is not supported; it is recommended to use modern browsers such as Chrome 80+ or Firefox 75+ to ensure normal animation effects.
