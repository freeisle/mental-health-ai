# 心理健康 AI 助手

一个面向心理健康支持场景的全栈应用，包含 Vue 3 前端和 Spring Boot 后端，提供 AI 对话、情绪记录与知识内容管理等功能。

## 项目结构

```text
.
├── ai-springboot/   # Spring Boot 后端（Java 17）
└── ai-vue/          # Vue 3 + Vite 前端
```

## 功能概览

- 用户注册、登录及 JWT 身份验证
- AI 心理支持对话
- 情绪日记和情绪趋势相关页面
- 心理健康知识文章浏览与管理
- 管理端仪表板及咨询会话管理

## 环境要求

- Java 17
- Maven（也可使用项目内的 `ai-springboot/mvnw`）
- Node.js 与 npm
- MySQL
- 可兼容 OpenAI API 的模型服务凭据（当前后端配置使用 SiliconFlow）

## 配置

后端配置位于 `ai-springboot/src/main/resources/application.yml`。运行前请按本地环境配置 MySQL 数据库连接、模型服务地址和 API Key，以及 JWT 密钥。不要将真实密码或密钥提交到公开仓库。

前端 API 请求默认使用 `/api` 前缀，开发代理配置位于 `ai-vue/vite.config.js`；如部署环境不同，请按实际后端地址调整代理或前端配置。

## 本地运行

先启动并配置 MySQL，然后在一个终端启动后端：

```bash
cd ai-springboot
./mvnw spring-boot:run
```

Windows PowerShell 可运行：

```powershell
cd ai-springboot
.\mvnw.cmd spring-boot:run
```

在另一个终端启动前端：

```bash
cd ai-vue
npm install
npm run dev
```

前端开发服务器会输出本地访问地址。生产构建可在 `ai-vue` 目录执行：

```bash
npm run build
```

## 技术栈

- 前端：Vue 3、Vite、Vue Router、Pinia、Element Plus、Axios、ECharts
- 后端：Spring Boot、Spring Security、MyBatis-Plus、MySQL、JWT、Spring AI
