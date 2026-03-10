# EchoLoom Website

这是 EchoLoom 的官方展示网站。网站旨在向用户展示 EchoLoom 的核心价值、技术架构、产品演示以及商业愿景。

## 目录结构

- `website/`
  - `index.html`: 网站的主入口文件，包含所有的页面内容、样式定义（基于 Tailwind CSS）以及交互逻辑。

## 核心特性

- **响应式设计**: 完美适配桌面端、平板端和移动端。
- **动态交互**: 包含 AI 工作流模拟、财务测算工具、市场调研问卷等交互模块。
- **视觉体验**: 
  - 使用 `Ma Shan Zheng` 艺术字体提升文化底蕴。
  - 基于 Canvas 的星空背景和动态粒子效果。
  - 玻璃拟态（Glassmorphism）设计风格。
- **性能优化**: 
  - 使用国内加速的字体镜像（fonts.font.im）。
  - 使用国内 CDN 加速 FontAwesome 图标库。

## 访问地址

- **官网**: [https://echoloom.cn](https://echoloom.cn) (示例地址)
- **控制台**: [https://hub.echoloom.cn](https://hub.echoloom.cn)

## 技术栈

- **HTML5**
- **Tailwind CSS** (通过 CDN 引入)
- **Chart.js** (数据可视化)
- **FontAwesome** (图标库)

## 开发与部署

该网站为纯静态页面，可以直接通过任何 Web 服务器（如 Nginx, Apache, Vercel, GitHub Pages 等）进行部署。

```bash
# 本地预览
# 如果安装了 live-server
live-server website/
```

## HTTPS 安全配置 (SSL)

如果在 Chrome 中看到“不安全”的提示，说明您的域名尚未配置正确的 SSL 证书。请尝试以下方案：

1.  **使用 Cloudflare (推荐)**:
    - 将域名的 DNS 解析托管到 Cloudflare。
    - 在 Cloudflare 后台开启 "SSL/TLS" 模式为 "Full" 或 "Flexible"。
    - Cloudflare 会自动为您提供免费的 HTTPS 证书。

2.  **Nginx + Let's Encrypt**:
    - 如果您使用 Nginx 自建服务器，可以使用 `certbot` 申请免费证书：
      ```bash
      sudo apt install certbot python3-certbot-nginx
      sudo certbot --nginx -d echoloom.cn
      ```

3.  **云厂商证书**:
    - 如果托管在阿里云/腾讯云/AWS，可以在控制台申请免费的 SSL 证书，并绑定到负载均衡 (SLB) 或 CDN 上。

---
Copyright © 2026 回声织造 EchoLoom. All Rights Reserved.
