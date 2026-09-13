# Git + Spring Cloud 前后端学习项目

这是一个适合初学者的前后端练习项目：

- `backend`：Spring Boot 后端，使用 Maven 管理依赖
- `frontend`：Vue 3 + Vite 前端，使用 npm 管理依赖

## 环境要求

- JDK 17+
- Maven 3.9+
- Node.js 18+
- npm

## 启动后端（IDEA）

1. 使用 IDEA 打开 `backend` 文件夹。
2. 等待 Maven 下载依赖。
3. 运行 `src/main/java/com/example/demo/DemoApplication.java`。
4. 后端默认地址：<http://localhost:8080>
5. 测试接口：<http://localhost:8080/api/hello>

## 启动前端（VS Code）

在 VS Code 中打开 `frontend` 文件夹，然后在终端执行：

```bash
npm install
npm run dev
```

按照终端提示打开前端地址，通常是 <http://localhost:5173>，点击“测试后端接口”即可看到后端返回的消息。

## 第一次 Git 练习

在项目根目录 `testgit` 中执行：

```bash
git init
git status
git add .
git commit -m "初始化前后端学习项目"
```

后续可以继续练习创建分支、修改文件、查看差异和合并分支。
