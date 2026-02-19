钦天监｜Binance Smart Chain上首个周期预测应用，币安黑客松大赛落地项目。币安AI Agent上架，获得Flap创始人关注。在当前预测市场兴起时，专注于周期理论研究与应用，理论师承鬼谷子，融合天文、历史、经济，易经等多学科视角，揭示事物发展的内在规律，为决策提供科学依据。
官网:www.qintianjian.fun
DAPP:dapps.qintianjian.com
演示链接：dapps.qintianjian.fun
交易哈希：0x3fca5b1326c8f275377131871c43fa321ce5d9b3a2479d5dc02bfc9a77900eb8
BAP-578逻辑合约：0x02aDF991D570512A812D109674Ba6A9B89e815b0
项目核心定位师承鬼谷子纵横家思想，融合易经、天文、历史、经济等多学科视角。
致力于揭示事物发展的内在周期规律，为投资、决策提供更科学的参考依据。
在当下预测市场（Prediction Markets）快速兴起的背景下，钦天监主打“周期理论+数据+古今结合”的独特赛道。
主要周期理论框架:
1、三元九运（宏观180年大周期）
每180年一轮大循环，每60年为一元，每20年为一运。当前处于下元九运（2024–2043）的九紫离火运，象征科技爆发、文明跃迁、精神觉醒、离散与变革的时代特征。
2、康德拉季耶夫周期（康波周期） ≈50–60年一轮
由重大技术革命驱动，包含繁荣→衰退→萧条→回升四个阶段。现在是第五次康波（1990年代互联网起），已进入衰退后期，接近底部酝酿下一轮技术革命。
3、木星周期 ≈12年一轮
木星公转影响地球磁场、气候、人类集体情绪。2026年是丙午年（火旺），属于承上启下、由收缩转向扩张的节点年。
4、美林投资时钟（3–5年短周期）
衰退 → 复苏 → 过热 → 滞胀四个象限。当前处于衰退后期，建议配置防御性资产，后续逐步转向周期股/成长股。
2026年关键预测展望（官网重点内容）
农业：可能出现严重干旱，农产品价格剧烈波动，需关注粮食安全与相关期货。
经济：全球/中国经济面临较大下行压力，危机风险较高，但也是新一轮技术周期的酝酿期。
股市：上半年仍有惯性冲高，6月大概率成为牛熊重要分水岭，之后转入调整或熊市。
房地产：多数区域触底，后续缓慢回升，关注政策窗口与人口/金融周期叠加的机会。
预测领域覆盖：宏观经济、A股/美股/港股板块轮动、农产品价格与灾害、楼市区域趋势等。
钦天监 DApp 部署说明
本文档提供钦天监DApp的完整安装和部署教程，适用于各种部署平台。
￼
目录
• 项目概述
• 技术栈
• 环境要求
• 本地开发部署
• 生产环境部署
◦ Vercel部署
◦ Netlify部署
◦ 自托管服务器部署
• 环境变量配置
• 常见问题
￼
项目概述
钦天监DApp是一个基于BSC链的Web3应用，集成了：
• 钱包连接（MetaMask、TokenPocket、OKX等）
• 代币转账和质押功能
• AI占卜功能
• NFT市场
• Agent创建和管理
￼
技术栈
前端：
• React 19
• TypeScript
• Vite 6
• Tailwind CSS 4
• shadcn/ui
• wagmi (Web3连接)
• wouter (路由)
后端：
• Express 4
• tRPC 11
• Drizzle ORM
• MySQL/TiDB数据库
区块链：
• BSC (Binance Smart Chain)
• ethers.js
￼
环境要求
• Node.js: >= 18.0.0
• pnpm: >= 8.0.0
• 数据库: MySQL 8.0+ 或 TiDB
• 操作系统: Linux / macOS / Windows (WSL推荐)
￼
本地开发部署
1. 克隆或下载项目
# 如果从Git仓库克隆
git clone 
<repository-url>
cd
 qintianjian-dapp

# 或者解压下载的项目文件
unzip qintianjian-dapp.zip
cd qintianjian-dapp
Copy
2. 安装依赖
# 安装pnpm（如果未安装）
npm install -g pnpm

# 安装项目依赖
pnpm install
Copy
3. 配置环境变量
创建 .env 文件：
cp .env.example .env
Copy
编辑 .env 文件，配置必要的环境变量（参见环境变量配置）。
4. 初始化数据库
# 推送数据库schema
pnpm db:push

# 或者运行迁移
pnpm db:migrate
Copy
5. 启动开发服务器
pnpm dev
Copy
服务器将在 http://localhost:3000 启动。
￼
生产环境部署
Vercel部署
Vercel是推荐的部署平台，支持自动构建和部署。
步骤：
1. 准备代码仓库
◦ 将代码推送到GitHub/GitLab/Bitbucket
2. 连接Vercel
◦ 访问 vercel.com
◦ 点击 "Import Project"
◦ 选择您的代码仓库
3. 配置构建设置
Framework Preset: Vite
Build Command: pnpm build
Output Directory: client/dist
Install Command: pnpm install
Copy
4. 配置环境变量
◦ 在Vercel项目设置中添加所有必要的环境变量
◦ 参见环境变量配置
5. 部署
◦ 点击 "Deploy"
◦ Vercel会自动构建和部署
6. 配置自定义域名（可选）
◦ 在Vercel项目设置的 "Domains" 中添加自定义域名
￼
Netlify部署
方式1：通过Git仓库
1. 访问 netlify.com
2. 点击 "New site from Git"
3. 选择代码仓库
4. 配置构建设置：
Build command: pnpm build
Publish directory: client/dist
Copy
5. 添加环境变量
6. 点击 "Deploy site"
方式2：手动部署
1. 本地构建项目：
pnpm build
Copy
2. 访问 netlify.com
3. 将 client/dist 文件夹拖拽到Netlify的部署区域
￼
自托管服务器部署
适用于VPS、云服务器等。
1. 服务器准备
# 更新系统
sudo apt update 
&&
 sudo apt upgrade -y

# 安装Node.js 18+
curl -fsSL https://deb.nodesource.com/setup_18.x 
|
 sudo -E bash -
sudo apt install -y nodejs

# 安装pnpm
npm install -g pnpm

# 安装PM2（进程管理器）
npm install -g pm2

# 安装Nginx（可选，用于反向代理）
sudo apt install -y nginx
Copy
2. 部署项目
# 上传项目文件到服务器
scp -r qintianjian-dapp user@your-server:/var/www/

# SSH登录服务器
ssh user@your-server

# 进入项目目录
cd
 /var/www/qintianjian-dapp

# 安装依赖
pnpm install

# 构建项目
pnpm build

# 配置环境变量
nano .env
Copy
3. 使用PM2启动应用
创建 ecosystem.config.js：
module.exports = {
  apps: [{
    name: 'qintianjian-dapp',
    script: 'server/index.js',
    instances: 'max',
    exec_mode: 'cluster',
    env: {
      NODE_ENV: 'production',
      PORT: 3000
    }
  }]
};
Copy
启动应用：
# 启动应用
pm2 start ecosystem.config.js

# 设置开机自启
pm2 startup
pm2 save
Copy
4. 配置Nginx反向代理
编辑 /etc/nginx/sites-available/qintianjian:
server {
    listen 80;
    server_name your-domain.com;

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
Copy
启用配置：
sudo ln -s /etc/nginx/sites-available/qintianjian /etc/nginx/sites-enabled/
sudo nginx -t
sudo systemctl reload nginx
Copy
5. 配置SSL证书（推荐）
# 安装Certbot
sudo apt install -y certbot python3-certbot-nginx

# 获取SSL证书
sudo certbot --nginx -d your-domain.com

# 自动续期
sudo certbot renew --dry-run
Copy
￼
环境变量配置
创建 .env 文件并配置以下变量：
必需变量
# 数据库配置
DATABASE_URL=mysql://user:password@host:3306/database_name

# JWT密钥（用于会话）
JWT_SECRET=your-random-secret-key-here

# OAuth配置
VITE_APP_ID=your-manus-app-id
OAUTH_SERVER_URL=https://api.manus.im
VITE_OAUTH_PORTAL_URL=https://oauth.manus.im

# 所有者信息
OWNER_OPEN_ID=your-owner-open-id
OWNER_NAME=your-owner-name
Copy
可选变量
# Manus内置服务（如果使用）
BUILT_IN_FORGE_API_URL=https://forge-api.manus.im
BUILT_IN_FORGE_API_KEY=your-forge-api-key
VITE_FRONTEND_FORGE_API_KEY=your-frontend-api-key
VITE_FRONTEND_FORGE_API_URL=https://forge-api.manus.im

# 分析服务（如果使用）
VITE_ANALYTICS_ENDPOINT=https://analytics.example.com
VITE_ANALYTICS_WEBSITE_ID=your-website-id

# 应用配置
VITE_APP_TITLE=钦天监 QinTianJian
VITE_APP_LOGO=/logo.png
Copy
环境变量说明
变量名
说明
必需
DATABASE_URL
MySQL/TiDB连接字符串
✅
JWT_SECRET
会话签名密钥，建议使用随机字符串
✅
VITE_APP_ID
Manus OAuth应用ID
✅
OAUTH_SERVER_URL
OAuth服务器地址
✅
VITE_OAUTH_PORTAL_URL
OAuth登录门户地址
✅
OWNER_OPEN_ID
项目所有者OpenID
✅
OWNER_NAME
项目所有者名称
✅
BUILT_IN_FORGE_API_*
Manus内置服务配置
❌
VITE_ANALYTICS_*
分析服务配置
❌
￼
常见问题
1. 钱包连接失败
问题：点击连接钱包没有反应
解决方案：
• 确保浏览器已安装对应的钱包插件（MetaMask、TokenPocket、OKX等）
• 检查浏览器控制台是否有错误信息
• 尝试刷新页面或重启浏览器
• 确认钱包插件已启用且未被其他扩展阻止
2. 数据库连接失败
问题：应用启动时报数据库连接错误
解决方案：
• 检查 DATABASE_URL 配置是否正确
• 确认数据库服务正在运行
• 检查数据库用户权限
• 确认网络连接和防火墙设置
3. 构建失败
问题：pnpm build 失败
解决方案：
# 清理缓存
rm -rf node_modules .pnpm-store
pnpm install

# 检查Node.js版本
node -v  
# 应该 >= 18.0.0

# 检查TypeScript错误
pnpm tsc --noEmit
Copy
4. 端口被占用
问题：启动时报端口3000已被占用
解决方案：
# 查找占用端口的进程
lsof -i :3000

# 杀死进程
kill -9 <PID>

# 或者修改端口
PORT=3001 pnpm dev
Copy
5. MetaMask连接到错误的钱包
问题：点击MetaMask但连接到OKX钱包
解决方案：
• 这是多钱包插件冲突问题
• 当前版本已修复，确保使用最新代码
• 临时解决：禁用其他钱包插件，只保留需要使用的
6. 部署后环境变量不生效
问题：部署到Vercel/Netlify后功能异常
解决方案：
• 检查平台的环境变量配置
• 确保所有 VITE_ 前缀的变量都已添加
• 重新部署以应用新的环境变量
• 检查变量名是否拼写正确
￼
技术支持
如有问题，请：
1. 查看项目 README.md
2. 检查浏览器控制台错误信息
3. 查看服务器日志
4. 访问 https://help.manus.im 提交工单
￼
许可证
请查看项目根目录的 LICENSE 文件。
￼
最后更新: 2026-02-20
