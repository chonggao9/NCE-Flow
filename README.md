<div align="center">

# 🎧 NCE Flow  

[![Demo](https://img.shields.io/badge/Demo-online-green?logo=google-chrome&logoColor=white)](https://nce.luzhenhua.cn/)  
[![License](https://img.shields.io/github/license/iChochy/NCE?color=blue)](./LICENSE)  
![Static Badge](https://img.shields.io/badge/Deploy-Vercel-black?logo=vercel)  
![Static Badge](https://img.shields.io/badge/Deploy-Cloudflare-orange?logo=cloudflare)  
![Static Badge](https://img.shields.io/badge/Deploy-Tencent%20Cloud-blue?logo=tencentcloud)  
![Static Badge](https://img.shields.io/badge/Deploy-GitHub%20Pages-lightgrey?logo=github)  

简约 · 高效 · 专注的新概念英语在线点读（NCE1–NCE4）

</div>

---

## ✨ 功能特性  

- **句子级点读**：点击任一句，从该句开始连续播放，自动高亮并居中  
- **三态语言视图**：EN / EN+CN / CN 自由切换（自动记忆偏好）  
- **现代化 UI**：Apple 风格设计，支持浅/深色主题，流畅动效  
- **纯静态部署**：无需后端依赖，直接 HTML/CSS/JS 即可运行  
- **兼容 LRC**：支持双语同行 `英文|中文` 或同时间戳上下行格式  

---

## 🗂 项目结构  

```
assets/          # 样式与脚本（styles.css, app.js, lesson.js）
index.html       # 首页（书目 + 课程列表）
lesson.html      # 课文点读页
static/data.json # 书目与课程元数据
NCE1..NCE4/      # 音频与 LRC 资源（文件名与 data.json 一致）
```

---

## 🚀 部署方式  

本项目为 **零依赖静态应用**，可在任意支持静态站点的服务部署：  

- **本地调试**  
  ```bash
  python3 -m http.server 8080
  # 浏览器访问 http://localhost:8080
  ```

- **GitHub Pages**  
  将仓库推送到 GitHub，启用 Pages 即可。默认入口为根目录的 `index.html`。

- **Vercel**  
  直接 `import project`，选择 **静态资源部署**，数秒即可上线。

- **腾讯云（EO）**  
  上传整个项目至 **静态网站托管**，配置默认首页为 `index.html`。

- **Cloudflare Pages**  
  一键绑定仓库，构建命令设为空，输出目录设为 `/`。  

> 部署后即刻可用，适合个人学习与公开分享。

---

## 🎼 LRC 规范（兼容两种格式）  

**推荐：同行双语**  
```lrc
[mm:ss.xx]English sentence | 中文译文
```

**兼容：同时间戳上下两行**  
```lrc
[mm:ss.xx]English sentence
[mm:ss.xx]中文译文
```

播放端自动识别并处理，连续播放时会自动兜底时长，避免短句抖动。  

---

## 🙏 致谢  

- 灵感来源与原始项目：[iChochy/NCE](https://github.com/iChochy/NCE)  
- 在此对原作者与社区表达感谢 🙌  

> 本项目在此基础上进行了：  
> - 首页整合书目与课程列表  
> - 课文页三态语言视图  
> - 句子级点读 + 连续播放  
> - 深浅色自适应 UI 统一  

---

## 📄 协议  

- 代码遵循仓库内 **LICENSE** 文件所述协议  
- 音频与文本版权归原权利人所有，仅用于学习研究  
- 请勿用于商业用途，若有侵权请联系：openai.luzhenhua@gmail.com  
