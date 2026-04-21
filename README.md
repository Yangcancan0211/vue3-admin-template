# vue3-admin-template项目介绍
商城后台管理系统
基于 Vue 3 + Vite + Pinia + Element Plus 构建的现代化后台管理系统。集成了动态路由权限、图片管理模块及复杂的商品规格（SKU）编辑功能。

## 技术栈

- 核心框架: Vue 3.5.31 
- 构建工具: Vite 8.0.3
- 路由管理: Vue Router 5.0.4
- 状态管理: Pinia 3.0.4
- UI组件库: ElementPlus
- 网络请求: Axios
- 样式: Windi CSS

## 项目结构
├── src
│   ├── api          # 接口请求统一管理 (axios 实例及具体模块接口)
│   ├── assets       # 静态资源 (图片、全局样式)
│   ├── axios.js     # 网络请求封装 (拦截器、Token 校验、加载条)
│   ├── components   # 公共业务组件 (图标选择、图片上传、SKU规格组件)
│   ├── layout       # 页面整体框架布局 (侧边栏、顶栏、标签导航)
│   ├── router       # 路由配置 (包含动态路由权限校验逻辑)
│   ├── stores       # Pinia 状态管理 (用户信息、侧边栏状态、持久化配置)
│   └── views        # 业务页面模块 (商品管理、订单管理、权限管理等)
├── .env.development # 开发环境变量
├── .env.production  # 生产环境变量 (GitHub Pages 部署配置)
├── index.html       # 入口 HTML
├── vite.config.js   # Vite 核心配置 (含 base 路径及反向代理)
└── package.json     # 项目依赖及脚本命令

## 快速开始

### 环境准备

- Node.js >= 16.0.0
- npm >= 8.0.0

### 安装步骤

1.克隆项目
git clone https://github.com/Yangcancan0211/vue3-admin-template
cd mall-management-system

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
VITE_API_BASE_URL = https://api.yourdomain.com

# 应用标题
VITE_APP_TITLE = 商城管理系统

# 是否开启 Mock
VITE_USE_MOCK = false
