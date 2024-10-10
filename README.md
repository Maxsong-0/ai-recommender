# AI Recommender System

## 项目介绍

AI Recommender System 是一个基于 Next.js 和 Prisma 的智能推荐系统。该系统利用用户历史数据和物品特征，为用户提供个性化的推荐。

### 主要特性

- 用户认证系统
- 物品管理（添加、编辑、删除）
- 基于用户历史的个性化推荐
- 响应式设计，适配各种设备

## 技术栈

- 前端：React, Next.js
- 后端：Next.js API routes
- 数据库：PostgreSQL
- ORM：Prisma
- 样式：Tailwind CSS
- 图标：Lucide React

## 安装指南

### 前置要求

- Node.js (v14 或更高版本)
- npm (通常随 Node.js 一起安装)
- PostgreSQL 数据库

### 安装步骤

1. 克隆仓库：

   ```bash
   git clone https://github.com/your-username/ai-recommender.git
   cd ai-recommender
   ```

2. 安装依赖：

   ```bash
   npm install
   ```

3. 环境配置：

   创建 `.env` 文件并添加以下内容：

   ```
   DATABASE_URL="postgresql://username:password@localhost:5432/ai_recommender?schema=public"
   ```

   请替换 `username`、`password` 和 `localhost:5432` 为你的实际数据库配置。

4. 数据库设置：

   ```bash
   npx prisma db push
   npm run seed
   ```

## 使用方法

### 开发模式

运行以下命令启动开发服务器：

```bash
npm run dev
```

访问 `http://localhost:3000` 查看应用。

### 生产模式

1. 构建项目：

   ```bash
   npm run build
   ```

2. 启动服务器：

   ```bash
   npm start
   ```

## API 文档

### 获取推荐

- 端点：`/api/recommendations`
- 方法：GET
- 参数：`userId` (查询参数)
- 响应：推荐物品列表

示例请求：
```
GET /api/recommendations?userId=1
```

示例响应：
```json
[
  {
    "id": 1,
    "title": "JavaScript: The Good Parts",
    "description": "A book about JavaScript best practices",
    "category": "Programming"
  },
  // ... 更多推荐项目
]
```

## 贡献指南

我们欢迎所有形式的贡献，包括但不限于：

- 报告 bug
- 提交功能请求
- 提交代码改进
- 改进文档

请遵循以下步骤：

1. Fork 项目仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的改动 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

## 许可证

本项目采用 MIT 许可证。详情请见 [LICENSE](LICENSE) 文件。

## 联系方式

项目维护者：Your Name - your.email@example.com

项目链接：[https://github.com/your-username/ai-recommender](https://github.com/your-username/ai-recommender)
