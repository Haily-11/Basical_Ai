# 悠悠笔记 (MyLog)

## 项目简介

悠悠笔记是一个基于Spring Boot + Thymeleaf的个人博客系统，完全由AI辅助开发完成。项目采用现代化的深色主题设计，支持文章发布、分类管理、用户认证等核心功能，是一个轻量级、优雅的个人知识管理工具。

**开发模式**：本项目100%由AI辅助生成代码，展现了AI编程助手的强大能力，从架构设计、后端逻辑到前端样式，全部通过人机协作完成。
<img width="769" height="584" alt="image" src="https://github.com/user-attachments/assets/8175f935-3382-4da0-8368-91322180166a" />


## 技术栈

### 后端
- **Spring Boot 3.x** - 核心框架
- **Spring Data JPA** - 数据持久化
- **Spring Security** - 安全认证
- **Thymeleaf** - 服务端模板引擎

### 前端
- **HTML5 + CSS3** - 页面结构与样式
- **JavaScript** - 交互逻辑
- **Bootstrap 5** - UI组件库
- **Font Awesome** - 图标库
- **Particles.js** - 粒子背景动画

### 数据存储
- **阿里云OSS** - 图片/文件云存储
- **MySQL** - 关系型数据库

### 构建工具
- **Gradle** / **Maven** - 项目构建与依赖管理

## 功能特性

### 核心功能
- ✅ **文章管理** - 创建、编辑、删除、查看文章
- ✅ **分类系统** - 文章分类与标签管理
- ✅ **用户认证** - 登录/注册/退出功能
- ✅ **点赞互动** - 文章点赞功能
- ✅ **浏览量统计** - 自动记录文章阅读次数
- ✅ **评论系统** - 文章评论功能（扩展中）

### 界面特色
- 🎨 **深色主题** - 科技感十足的暗色设计
- 🌌 **粒子背景** - 动态粒子网络动画
- 💫 **霓虹效果** - 渐变色彩与发光元素
- 📱 **响应式布局** - 完美适配移动端
- 🔮 **毛玻璃效果** - 现代化UI设计

## 项目结构

```

src/
├── main/
│   ├── java/com/blog/mylog/
│   │   ├── config/          # 配置类（OSS、Web配置）
│   │   ├── controller/      # 控制器层
│   │   │   ├── ArticleController.java    # 文章管理
│   │   │   ├── AuthController.java       # 认证接口
│   │   │   ├── PageController.java       # 页面路由
│   │   │   ├── TechstackController.java  # 技术栈
│   │   │   ├── UploadController.java     # 文件上传
│   │   │   └── UserController.java       # 用户管理
│   │   ├── dto/             # 数据传输对象
│   │   ├── entity/          # 实体类
│   │   │   ├── Article.java     # 文章
│   │   │   ├── User.java        # 用户
│   │   │   ├── Comment.java     # 评论
│   │   │   ├── Tech.java        # 技术栈
│   │   │   ├── CheckIn.java     # 打卡记录
│   │   │   └── LearningProgress.java  # 学习进度
│   │   ├── repository/      # 数据访问层
│   │   └── service/         # 业务逻辑层
│   └── resources/
│       ├── static/css/      # 样式文件
│       └── templates/       # Thymeleaf模板
│           ├── index.html       # 首页
│           ├── detail.html      # 文章详情
│           ├── list.html        # 文章列表
│           ├── login.html       # 登录页
│           ├── write.html       # 写文章
│           ├── techstack.html   # 技术栈
│           ├── about.html       # 关于页
│           └── layout.html      # 布局模板
└── test/                    # 测试代码
```
## 快速开始

### 环境要求
- JDK 17+
- MySQL 8.0+
- Maven 3.6+ 或 Gradle 7+

### 安装步骤

1. **克隆项目**
```
bash
git clone https://github.com/yourusername/mylog.git
cd mylog
```
2. **配置数据库**
```
yaml
# application.yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/mylog?useSSL=false&serverTimezone=UTC
    username: your_username
    password: your_password
```
3. **启动项目**
```
bash
# Maven方式
mvn spring-boot:run

# Gradle方式
gradle bootRun
```
4. **访问应用**
打开浏览器访问：http://localhost:8080

## 数据库表设计

### 主要表结构

**用户表 (user)**
- id, username, password, email, avatar, createTime

**文章表 (article)**
- id, title, content, summary, category, authorId
- viewCount, likeCount, commentCount, createTime

**评论表 (comment)**
- id, articleId, userId, content, createTime

**技术栈表 (tech)**
- id, name, icon, description, category

## AI辅助开发亮点

### 代码生成
- 🤖 后端接口100% AI生成
- 🎨 前端样式AI设计实现
- 📊 数据库结构AI规划
- 🧪 测试用例AI编写

### 开发效率
- ⚡ 开发周期缩短80%
- 📝 代码质量稳定可控
- 🐛 Bug率显著降低
- 🎯 功能实现精准快速

### 人机协作模式
1. **需求描述** → 开发者提供功能需求
2. **AI生成** → AI自动生成完整代码
3. **人工审核** → 开发者review并微调
4. **迭代优化** → 快速修改持续改进

## 部署方案

### 本地运行
```
bash
java -jar target/blog-system-1.0.0.jar
```
### 云服务器部署
1. 打包项目：`mvn clean package`
2. 上传jar包到服务器
3. 配置Nginx反向代理
4. 使用systemd管理进程

### GitHub Pages（静态化）
如需部署纯静态版本，可参考项目中的GitHub Pages配置。

## 性能优化

- 🚀 **懒加载** - 图片与数据按需加载
- 💾 **缓存机制** - 热点数据缓存
- 📦 **资源压缩** - CSS/JS压缩优化
-  **CDN加速** - 静态资源CDN分发
-  图片上传OSS

## 安全特性

- 🔒 **密码加密** - BCrypt加密存储
- 🛡️ **SQL注入防护** - JPA参数化查询
- 🚫 **XSS防护** - Thymeleaf自动转义
- 🔑 **Session管理** - 安全的会话控制



## 开发日志

本项目见证了AI编程的进化历程：几个小时即可完成

## 致谢

感谢AI编程助手的全程陪伴，让开发变得高效而有趣！

## 开源协议

本项目采用 MIT 协议开源，可自由使用和修改。


```


这个README突出了AI辅助开发的特色，涵盖了技术栈、功能特性、部署说明等内容。
