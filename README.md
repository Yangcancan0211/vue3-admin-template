# vue3-admin-template项目介绍
商城后台管理系统
基于 Vue 3 + Vite + Pinia + Element Plus 构建的现代化后台管理系统。集成了动态路由权限、图片管理模块及复杂的商品规格（SKU）编辑功能。

## 技术栈

- 核心框架: Vue 3.5.31 
- 构建工具: Vite 6.0.3
- 路由管理: Vue Router 5.0.4
- 状态管理: Pinia 3.0.4
- UI组件库: ElementPlus
- 网络请求: Axios
- 样式: Windi CSS

## 项目结构

```text
├── src/
│   ├── api/          # 接口请求模块
│   ├── assets/       # 静态资源 (图片、样式)
│   ├── axios.js/     # Axios 封装与拦截器
│   ├── components/   # 公共组件 (SKU、上传等)
│   ├── layout/       # 页面整体框架布局
│   ├── router/       # 路由配置与权限守卫
│   ├── stores/       # Pinia 状态管理
│   └── views/        # 业务页面 (商品、订单等)
├── .env.development  # 开发环境变量
├── .env.production   # 生产环境变量
├── vite.config.js    # Vite 核心配置
└── package.json      # 项目依赖与脚本
```
## 快速开始

### 环境准备

- Node.js >= 16.0.0
- npm >= 8.0.0

### 安装步骤

1.克隆项目
git clone https://github.com/Yangcancan0211/vue3-admin-template
cd vue3-admin-template

2.安装依赖
npm install

3.配置环境变量

复制环境变量文件
cp .env.development.example .env.development

编辑环境变量文件
- API 接口地址
VITE_API_BASE_URL=http://ceshi13.dishait.cn

- 应用标题
VITE_APP_TITLE=商城后台管理系统

4.启动项目
npm run dev

5.项目打包
npm run build

### 环境配置
- 开发环境(.env.development)
# API 基础地址
VITE_API_BASE_URL = http://ceshi13.dishait.cn

# 应用标题
VITE_APP_TITLE = 商城管理系统

# 是否开启 Mock
VITE_USE_MOCK = false

- 生产环境(.env.production)
# API 基础地址
VITE_API_BASE_URL = http://ceshi13.dishait.cn

# 应用标题
VITE_APP_TITLE = 商城管理系统

# 是否开启 Mock
VITE_USE_MOCK = false
## ❓ 常见问题

### 1. 生产环境登录无反应 / 跨域报错
由于 GitHub Pages 强制使用 HTTPS，而本项目接口服务器为 HTTP 协议，浏览器会触发“混合内容”拦截。
**解决方法：**
- 在浏览器地址栏左侧点击“网站设置”或“圆圈i图标”。
- 找到 **“不安全内容” (Insecure content)**。
- 选择 **“允许” (Allow)**，然后刷新页面即可正常登录。

### 2. 页面刷新 404
本项目已在 `router/index.js` 中处理了动态路由拦截，确保生产环境刷新页面时能正确重定向至 404 逻辑。
