# 第九梦工作室网站部署说明

## 项目结构
```
GameWebsite/
├── index.html          # 主页
├── games/              # 游戏作品板块
│   └── index.html
├── apps/               # 应用作品板块
│   └── index.html
├── blog/               # AI技术博客板块
│   └── index.html
├── other/              # 其他作品板块
│   ├── index.html
│   └── particle-effects.html  # 原有的粒子效果页面
├── assets/             # 静态资源文件夹
│   └── images/         # 图片资源
├── netlify.toml        # Netlify部署配置
└── README_DEPLOY.md    # 部署说明文档
```

## Netlify部署步骤

1. **准备Git仓库**
   ```bash
   git init
   git add .
   git commit -m "初始化第九梦工作室网站"
   ```

2. **推送到GitHub/GitLab**
   ```bash
   git remote add origin <你的仓库地址>
   git push -u origin main
   ```

3. **在Netlify中部署**
   - 登录 [Netlify](https://app.netlify.com)
   - 点击 "New site from Git"
   - 选择你的Git服务提供商
   - 选择仓库分支（通常是main或master）
   - 构建设置保持默认（因为这是静态网站）
   - 点击 "Deploy site"

## 自定义配置

### 更换轮播图图片
1. 将新图片放入 `assets/images/` 文件夹
2. 修改 `index.html` 中的轮播图图片路径：
   ```html
   <img src="assets/images/your-image.jpg" alt="描述">
   ```

### 添加游戏作品
1. 在 `games/index.html` 中添加游戏卡片
2. 或者创建单独的游戏页面并在 `games/` 文件夹中管理

### 添加应用作品
1. 在 `apps/index.html` 中添加应用卡片
2. 可以添加应用截图和详细信息

### 添加博客文章
1. 在 `blog/` 文件夹中添加HTML或Markdown文件
2. 在 `blog/index.html` 中添加文章链接

### 添加其他作品
1. 在 `other/` 文件夹中添加项目文件
2. 在 `other/index.html` 中添加项目卡片

## 技术栈
- **前端**: HTML5, CSS3, JavaScript (ES6+)
- **样式**: 原生CSS，CSS Grid, Flexbox
- **动画**: CSS Transitions, JavaScript Animation
- **部署**: Netlify (静态网站托管)
- **CDN**: 使用Unsplash作为临时图片源

## 浏览器支持
- Chrome/Chromium 70+
- Firefox 65+
- Safari 12+
- Edge 79+

## 开发建议
- 所有页面都采用响应式设计
- 使用深色主题和扁平化设计风格
- 注重用户体验和页面性能
- 图片使用WebP格式以优化加载速度

## 维护说明
- 定期更新内容和图片
- 检查所有链接的有效性
- 优化SEO和页面性能
- 保持代码整洁和文档更新