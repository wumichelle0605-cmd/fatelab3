# FateLab 3.0 · 命理实验室

> 用回归分析验证「算命」到底准不准

🔗 **在线体验**: https://cowork.xiaohongshu.com/s/fatelab3/

## 简介

FateLab 是一个「命理双盲实验平台」，用统计学方法验证八字、占星、黄历、小六壬等命理流派的预测准确度：

- 🔮 **命盘综合测算** — 输入生辰信息，一键获取四大流派命理分析
- 🧪 **盲测实验** — 隐藏信息来源，根据真实情况作答，贡献实验数据
- 📊 **效力榜单** — 基于真实数据的回归分析看板，实时更新各流派命中率
- 🧬 **个人算法** — 完成足够盲测后，生成你专属的命理 Skill

## 本地运行

```bash
npm install
cp .env.example .env   # 填入你的 DeepSeek API Key
npm run dev            # 前端开发服务器
node server.cjs        # 后端代理（另开终端）
```

## 部署到 Railway

1. Fork 本仓库
2. 在 [Railway](https://railway.app) 新建项目 → Deploy from GitHub
3. 在 Variables 里添加：`DEEPSEEK_API_KEY=sk-xxx`
4. 自动构建部署完成后即可访问

## 技术栈

- **前端**: React + Vite + TypeScript
- **后端**: Node.js (CJS) 代理服务
- **AI**: DeepSeek API (`deepseek-chat`)
- **算命引擎**: lunar-typescript（八字按节气换月，与测测/万年历一致）
