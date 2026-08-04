# Mofort Paper IBC 独立站 · 部署手册（GitHub + Vercel 免费部署）

> 项目：D:\CODEX工作台\project_05_paper-ibc-website
> 本地预览：http://127.0.0.1:8899/index.html

## 一、现状
- 站点已完整构建（5 个页面：Home / Products / Technology / Applications / Contact），英文 B2B 风格，Tailwind CSS，真实产品与 ISTA 测试实拍图；
- 已用便携 Git（C:\tmp\git-portable）在项目目录完成 `git init` 和首次 commit；
- agent.md（项目上下文记忆）与 .gitignore 已就位。

## 二、部署前需要你提供的两项凭据
1. **GitHub Token**（Fine-grained PAT，权限：Contents Read/Write，仓库范围选该项目或全部）——用于创建远程仓库并推送代码；
2. **Vercel Token**——用于免密部署（Vercel 后台 → Settings → Tokens → Create）。

> 提供方式：直接把 Token 粘贴到对话里即可（我会写入本地环境变量，不回显）。若不想提供 Token，可照下方“手动部署”操作。

## 三、自动部署步骤（拿到 Token 后由 Codex 执行）
1. `git remote add origin https://github.com/<你的账号>/paper-ibc-website.git`
2. 创建 GitHub 仓库并推送（用 Token 鉴权）。
3. 安装 Vercel CLI（npm i -g vercel）并以 `vercel --prod --token <VERCEL_TOKEN>` 从项目目录直接部署——**无需 GitHub 也能上线**（Vercel 会分配 https://paper-ibc-website-xxx.vercel.app）。
4. 若走 GitHub 集成：Vercel 后台 Import 该仓库，Vercel 自动检测静态站点并构建，之后每次 push 自动部署。

## 四、手动部署（不想提供 Token 时）
1. **GitHub**：浏览器登录 github.com → New repository（名字 paper-ibc-website）→ 按提示执行
   `git remote add origin ... && git branch -M main && git push -u origin main`（Git 凭据会要求登录）。
2. **Vercel**：vercel.com → Add New Project → Import GitHub 仓库 → Framework Preset 选 Other/静态 → Deploy。
3. 绑定域名：Vercel 项目 Settings → Domains → 添加自有域名，Vercel 自动配 SSL。

## 五、常见故障排查（手册 Pro-Tip）
- Vercel 鉴权失败/插件失效：通常是 Token 过期或账号切换 → 重新生成 Token 或删除并重装 Vercel CLI 后重登。
- GitHub push 超时：当前网络访问 github.com 不稳定（API 可达、下载/页面超时）。对策：使用镜像加速（如 ghproxy 类）或换网络环境；Token 推送走 https 一般比 git 协议更稳。
- 移动端错位：本站点已用 Tailwind 响应式栅格，若出现个别错位，直接对 Codex 说“请适配 H5 页面，确保手机端显示完美”。

## 六、上线后清单（手册建议）
1. WhatsApp 跳转与询盘邮箱实测：wa.me/8615866807268、wa.me/8615963287268、tengchengibc@gmail.com；
2. 图片已用真实实拍（非占位图），后续可替换为更高清工厂/产线图；
3. 修改参数或联系方式时，先读 agent.md，再让 AI 精准迭代。