# Web‑MVC 轻量商城 / Web‑MVC Lightweight Shop

A lightweight B2C sample shop built with **ASP.NET Core 8 MVC** and **MySQL**.
一个使用 **ASP.NET Core 8 MVC** 与 **MySQL** 构建的本地轻量级 B2C 商城示例项目。

---

## Key Features / 关键特性

* User registration & login with cookie authentication
  Cookie 认证的用户注册与登录
* Product browsing, shopping cart, order placement, tracking
  商品浏览、购物车、下单与订单追踪
* Admin inventory and user management
  管理员角色的库存与用户管理
* End‑to‑end tests with Playwright and GitHub Actions CI
  Playwright 端到端测试与 GitHub Actions 持续集成

---

## Technology Stack / 技术栈

| Layer 层次 | Technology 技术                       |
| -------- | ----------------------------------- |
| Backend  | ASP.NET Core 8 · EF Core 8 (Pomelo) |
| Frontend | Razor View · Bootstrap 5            |
| Database | MySQL 8.x                           |
| Testing  | xUnit · Playwright                  |

---

## Prerequisites / 先决条件

| Software 软件 | Version 版本 | Notes 说明                                           |
| ----------- | ---------- | -------------------------------------------------- |
| .NET SDK    | 8.x        | `dotnet --version` to verify / 运行以验证               |
| MySQL       | 8.x        | `mysql --version` to verify                        |
| Node.js\*   | ≥ 18       | Needed only for Playwright HTML report / 仅在查看报告时需要 |

\*Node.js is required only when you want to open the Playwright HTML report locally.
仅在本地打开 Playwright HTML 报告时才需要 Node.js。

---

## Quick Start / 快速开始

```bash
# Clone the repository / 克隆仓库
git clone https://github.com/herongcan139047/WebWVC.git
cd WVC-Web

# Windows PowerShell
./scripts/setup.ps1

# macOS / Linux
bash ./scripts/setup.sh

# Open the site / 打开网站
http://localhost:5000
```

---

## Database / 数据库

```bash
# Apply migrations (already included in the setup script)
# 应用迁移（setup 脚本已执行）
dotnet ef database update

# Seed sample data / 种子数据（可选）
dotnet run --seed
```

---

## Tests / 测试

```bash
# Unit tests / 单元测试
dotnet test

# End‑to‑end tests / 端到端测试
pwsh ./scripts/e2e.ps1

# View HTML report / 查看报告
open playwright-report/index.html   # macOS
start playwright-report\index.html  # Windows
```

---

## Project Structure / 项目结构

```
WebMVC/
 ├─ Controllers/
 ├─ Models/
 ├─ Views/
 ├─ Areas/
 │   └─ Admin/
 ├─ scripts/
 ├─ tests/
 └─ README.md
```


