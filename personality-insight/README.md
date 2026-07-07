# 真我洞察 · 全面人格评估

整合 **11 大权威心理学量表**、**188 道专业题目** 的多维人格与职业兴趣评估工具。

在线体验：将 `你的用户名.github.io/仓库名/` 替换为实际 GitHub Pages 地址。

## 功能概览

| 模块 | 量表 | 题数 |
|------|------|------|
| 大五人格 | IPIP-NEO | 50 |
| 人格精细面 | BFAS (DeYoung) | 20 |
| 道德人格 | HEXACO | 10 |
| 依恋风格 | ECR-R | 12 |
| 自我概念 | RSES + GSE | 16 |
| 情绪能力 | ERQ + TEIQue | 14 |
| 核心价值 | Schwartz PVQ | 8 |
| 动机取向 | RF + LoC + Growth | 14 |
| 人际风格 | TKI | 6 |
| **职业兴趣** | **Holland RIASEC** | **30** |
| 认知风格 | 实证推导 | 8 |

## 职业匹配

- 30 题 RIASEC 职业兴趣量表
- 75% 自陈 + 25% 人格交叉验证加权
- Holland 三字母代码（如 IAS、ECS）
- Top 8 推荐职业 + 理想工作环境 + 职业洞察

## 本地运行

```bash
cd personality-insight
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## 发布到 GitHub Pages

### 第一步：创建仓库并推送

```bash
cd personality-insight

git init
git add .
git commit -m "Initial commit: 真我洞察人格评估"
git branch -M main
git remote add origin https://github.com/你的用户名/仓库名.git
git push -u origin main
```

### 第二步：开启 GitHub Pages

1. 打开 GitHub 仓库 → **Settings** → **Pages**
2. **Source** 选择 **GitHub Actions**
3. 推送代码后，`.github/workflows/deploy.yml` 会自动构建并部署
4. 部署完成后访问：`https://你的用户名.github.io/仓库名/`

### 手动触发部署

仓库 → **Actions** → **Deploy to GitHub Pages** → **Run workflow**

## 项目结构

```
personality-insight/
├── index.html              # 入口页面
├── css/style.css           # 样式
├── js/
│   ├── app.js              # 交互逻辑
│   ├── scoring.js          # 计分引擎
│   ├── career.js           # 职业匹配
│   ├── profiles.js         # 人格原型与洞察
│   ├── questions.js        # 题库汇总
│   └── data/               # 量表数据
├── .github/workflows/      # GitHub Pages 自动部署
└── README.md
```

## 隐私

所有答题数据仅保存在浏览器 localStorage，不上传服务器。

## 免责声明

仅供自我探索参考，不能替代专业心理诊断或职业咨询。

## 参考文献

- Goldberg (1999) IPIP-NEO
- DeYoung et al. (2007) BFAS
- Holland (1997) RIASEC
- Ashton & Lee (2009) HEXACO
- Fraley et al. (2000) ECR-R
- Rosenberg (1965) RSES / Schwarzer (1995) GSE
- Gross & John (2003) ERQ
- Schwartz (1992) PVQ
