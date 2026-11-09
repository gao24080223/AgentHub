# AgentHub

AgentHub 是一个基于 FastAPI、PostgreSQL 和 React 构建的 AI 智能体管理平台 Demo。

## 🛠️ 技术栈
- **前端**: React, Vite
- **后端**: Python, FastAPI, SQLAlchemy, Alembic
- **数据库**: PostgreSQL 16
- **包管理**: uv (后端), npm (前端)

## 🚀 快速启动指南

### 1. 环境准备
请确保你的电脑上已安装以下软件：
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (用于运行数据库)
- [Node.js](https://nodejs.org/) (用于运行前端)
- [uv](https://github.com/astral-sh/uv) (Python 包管理器，可通过 `pip install uv` 或官方脚本安装)

### 2. 启动后端与数据库
```bash
# 1. 进入后端目录
cd agenthub

# 2. 启动 PostgreSQL 数据库容器
docker compose up -d

# 3. 安装后端依赖
uv sync

# 4. 执行数据库迁移（自动建表）
uv run alembic upgrade head

# 5. 启动后端服务 (运行在 http://127.0.0.1:8000)
uv run uvicorn app.main:app --reload --app-dir .
启动前端
打开一个新的终端窗口，执行以下命令：

bash
# 1. 进入前端目录
cd frontend

# 2. 安装前端依赖
npm install

# 3. 启动前端服务 (运行在 http://localhost:5173)
npm run dev
💡 打开浏览器访问 http://localhost:5173 即可看到前端界面。
