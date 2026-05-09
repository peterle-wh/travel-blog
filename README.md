# Salt in our Hair - 旅行博客

🦞 一个基于 Astro + Tailwind CSS 的旅行博客网站

## 设计风格

- 🎨 配色：黑色 `#000` + 粉色 `#FF9398`
- 📝 字体：Space Grotesk (标题) + Noto Sans SC (中文正文)
- ✨ 风格：深色主题、现代简约、旅行摄影导向

## 页面结构

| 页面 | 路径 | 说明 |
|------|------|------|
| 首页 | `/` | Hero、目的地、精选文章、订阅 |
| 旅行攻略 | `/blog` | 文章列表 + 分类筛选 |
| 关于我们 | `/about` | 团队介绍、故事、联系方式 |
| 更新指南 | `/update-guide` | **找我就行！** |

## 🚀 部署到 Netlify

### 方法一：GitHub 部署（推荐）

1. **创建 GitHub 仓库**
   - 去 https://github.com/new
   - 仓库名：`travel-blog`
   - 选 Private 或 Public 都可以

2. **上传代码到 GitHub**
   ```bash
   cd /home/ubuntu/.openclaw/workspace/travel-blog
   git remote -v  # 查看当前 remote
   
   # 如果 remote 不是你的仓库，先移除：
   git remote remove origin
   
   # 添加你的仓库（把 USERNAME 换成你的 GitHub 用户名）：
   git remote add origin https://github.com/USERNAME/travel-blog.git
   
   # 推送代码：
   git push -u origin main
   ```

3. **连接 Netlify**
   - 登录 https://app.netlify.com
   - 点击 "Add new site" → "Import from Git"
   - 选择 GitHub 仓库
   - Netlify 会自动检测到 Astro 并构建

### 方法二：直接上传 dist 文件夹

1. **本地构建**
   ```bash
   npm run build  # 生成 dist 文件夹
   ```

2. **上传 dist 到 Netlify**
   - 去 https://app.netlify.com/drop
   - 直接拖拽 `dist` 文件夹

## 🦞 通过我更新网站

直接告诉我你要更新什么，我会生成完整内容给你复制粘贴。

### 可更新的板块

| 板块 | 说明 |
|------|------|
| 🏠 **首页** | Hero文案、精选文章、目的地标签 |
| ✈️ **旅行攻略** | 文章列表、分类标签 |
| 📝 **文章内容** | 新建文章、修改旧文章 |
| 👤 **关于我们** | 团队介绍、联系方式 |

### 使用示例

```
你：帮我写一篇厦门3日游攻略
我：生成完整 Markdown 文章
你：复制到 GitHub → Netlify 自动构建发布
```

## 技术栈

- **框架**：Astro 5.x
- **样式**：Tailwind CSS
- **字体**：Space Grotesk + Noto Sans SC
- **图片**：Unsplash (示例图)
- **部署**：Netlify

## 项目结构

```
travel-blog/
├── src/
│   ├── layouts/
│   │   └── Layout.astro      # 全局布局
│   ├── pages/
│   │   ├── index.astro       # 首页
│   │   ├── about.astro       # 关于我们
│   │   ├── update-guide.astro # 更新指南（找我就行）
│   │   └── blog/
│   │       └── index.astro   # 旅行攻略列表
│   └── styles/
│       └── global.css        # 全局样式
├── public/
│   └── favicon.svg
├── astro.config.mjs
├── package.json
└── README.md
```

## 本地开发

```bash
cd travel-blog
npm install
npm run dev     # 开发模式 http://localhost:4321
npm run build   # 构建生产版本
npm run preview # 预览生产版本
```

---

**有问题？直接问我！🦞**