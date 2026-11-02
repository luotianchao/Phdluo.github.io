# 知行｜个人学习博客

一个无构建依赖的静态个人博客，可直接部署到 GitHub Pages。

## 发布为 `luotianchao.github.io`

1. 在 `luotianchao` 的 GitHub 账户下新建一个**公开**仓库，仓库名必须是 `luotianchao.github.io`。
2. 将本地仓库关联到它：
   ```powershell
   git remote add origin https://github.com/luotianchao/luotianchao.github.io.git
   git add .
   git commit -m "创建个人博客"
   git push -u origin main
   ```
3. 打开仓库 **Settings → Pages → Build and deployment**，在 **Source** 选择 **GitHub Actions**。
4. 等待 Actions 工作流完成，访问 `https://luotianchao.github.io`。

> `luoziming.github.io` 不是 `luotianchao` 账户可设置的自定义域名：GitHub 用户站点必须使用仓库所有者的 `<用户名>.github.io` 地址。若必须使用该地址，需由 `luoziming` 账户或同名组织拥有 `luoziming.github.io` 仓库。

## 自定义内容

- 在 `index.html` 中替换“你的名字”、邮箱和首页文案。
- 在 `posts/` 新建文章页，并在 `posts/index.html`、首页的文章卡片中添加入口。
- 在 `assets/` 放置可下载的学习资料。

## 使用自定义域名（可选）

在仓库根目录创建名为 `CNAME` 的无扩展名文件，内容仅保留你的域名（如 `blog.example.com`），然后在域名服务商处按 GitHub Pages 的说明配置 DNS。
