# 中西天地分隔神话资料网站

一个专注于中国"绝地天通"和西方"巴别塔"神话研究资料的学术文献管理与分享平台。

## 项目简介

本项目是一个现代化的单页应用（SPA），用于收集、整理和分享关于中西方天地分隔神话的学术资料，包括论文、翻译、报告等多种类型的文献。网站采用前后端分离架构，通过腾讯云 CloudBase 提供实时数据存储和同步功能。

## 主要功能

### 📚 资料管理
- **添加资料**：支持添加标题、简介、分类、标签、链接等信息
- **删除资料**：带确认对话框的安全删除功能
- **实时搜索**：支持标题、简介、分类、标签的即时过滤
- **分类展示**：学术论文、翻译资料、行业报告、内部文档四大分类
- **神话标签**：绝地天通、巴别塔标签筛选

### 🎨 界面特性
- **轮播展示**：首页支持6张图片自动轮播（6秒自动切换）
- **响应式设计**：完美适配移动端、平板和桌面设备
- **毛玻璃效果**：现代化的玻璃态（Glassmorphism）设计风格
- **动态导航**：滚动时导航栏颜色自动切换
- **流畅动画**：卡片悬停、页面过渡等精美动画效果

### 🔄 实时同步
- 基于腾讯云 CloudBase 的实时数据库
- 多端数据自动同步
- 匿名用户快速访问

## 技术栈

### 前端技术
- **HTML5 + CSS3 + JavaScript (ES6+)**
- **Tailwind CSS**：快速响应式设计
- **Google Fonts (Inter)**：现代化字体支持

### 后端服务
- **腾讯云 CloudBase (TCB) v2.21.6**
  - 实时数据库
  - 匿名认证
  - 云端存储

## 项目结构

```
tiandiweb/
├── image/              # 轮播图片资源（6张，总计约8.2MB）
│   ├── home01.png
│   ├── home02.png
│   ├── home03.png
│   ├── home04.png
│   ├── home05.png
│   └── home06.png
├── index.html          # 主应用文件（单文件应用）
└── README.md          # 项目说明文档
```

## 快速开始

### 环境要求
- 现代浏览器（Chrome、Firefox、Safari、Edge 等）
- 无需 Node.js 或其他构建工具

### 本地运行

1. **克隆项目**
```bash
git clone <repository-url>
cd tiandiweb
```

2. **直接打开**
```bash
# 方式1：双击 index.html 文件
# 方式2：使用本地服务器
python -m http.server 8000
# 或
npx serve
```

3. **访问应用**
```
打开浏览器访问: http://localhost:8000
```

### 部署

本项目是纯静态网站，可以部署到任何静态托管服务：

- **Vercel / Netlify**：直接连接 Git 仓库自动部署
- **GitHub Pages**：推送到 gh-pages 分支
- **腾讯云 / 阿里云 OSS**：上传文件到对象存储
- **传统服务器**：上传到 Web 服务器目录

## 配置说明

### 腾讯云 CloudBase 配置

如需修改云服务配置，请在 `index.html` 中找到以下代码并修改：

```javascript
const app = cloudbase.init({
  env: 'your-env-id'  // 修改为你的环境ID
});
```

### 数据库集合结构

```javascript
{
  title: String,        // 资料标题
  description: String,  // 资料简介
  category: String,     // 分类（学术论文/翻译资料/行业报告/内部文档）
  mythTag: String,      // 神话标签（绝地天通/巴别塔）
  link: String,         // 资源链接
  date: Timestamp       // 创建日期
}
```

## 功能页面

- **首页**：展示全部资料，带轮播图和搜索功能
- **绝地天通**：筛选显示绝地天通相关资料
- **巴别塔**：筛选显示巴别塔相关资料
- **关于**：网站介绍和使用说明

## 浏览器兼容性

- Chrome/Edge 88+
- Firefox 85+
- Safari 14+
- 移动端浏览器（iOS Safari 14+, Android Chrome 88+）

需要支持：
- CSS Grid & Flexbox
- ES6+ JavaScript
- backdrop-filter（毛玻璃效果）

## 开发路线

- [x] 基础资料管理功能
- [x] 实时数据库集成
- [x] 响应式设计
- [x] 搜索和筛选功能
- [x] 导航栏和轮播图
- [ ] 用户认证系统
- [ ] 资料收藏功能
- [ ] 评论和讨论功能
- [ ] 数据导出功能

## 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 版本历史

- **v1.0** - 初版发布（2025-11-15）
  - 基础资料管理功能
  - 腾讯云数据库集成
  - 响应式界面设计
  - 搜索和分类功能

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 联系方式

如有问题或建议，请通过以下方式联系：
- 提交 Issue
- 发送邮件至 [your-email@example.com]

## 致谢

- 感谢腾讯云 CloudBase 提供云服务支持
- 感谢 Tailwind CSS 提供优秀的 CSS 框架
- 感谢所有贡献者和用户的支持

---

⭐ 如果这个项目对你有帮助，请给它一个星标！
