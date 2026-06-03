# Boris-style minimal academic homepage

这是一个极简数学个人主页模板：

- 纯 HTML/CSS
- 无 JavaScript
- 无外部字体
- 无 Google Fonts / YouTube / Google Analytics / CDN
- 适合 GitHub Pages
- 可以后续绑定 `yourname.com` 或 `yourname.org`

## 文件结构

```text
.
├── index.html              # 首页
├── writing.html            # 论文、preprints、notes、slides
├── problems.html           # 可选：open problems / questions
├── teaching.html           # 可选：教学经历
├── cv.html                 # CV 页面
├── contact.html            # 联系方式
├── style.css               # 全站样式
├── robots.txt              # 搜索引擎抓取设置
├── sitemap.xml.example     # sitemap 示例；改好域名后再改名为 sitemap.xml
├── CNAME.example           # 自定义域名示例；买域名后再改名为 CNAME
├── .nojekyll               # 让 GitHub Pages 按普通静态文件发布
├── assets/                 # 放照片，例如 portrait.jpg
├── papers/                 # 放论文 PDF、讲义 PDF
├── slides/                 # 放报告 slides
└── cv/                     # 放 CV，例如 cv.pdf
```

## 第一步：先在本地改内容

至少替换这些内容：

```text
Your Name
yourname.com
your.email@example.com
your.email [at] example [dot] com
YOUR_GITHUB_USERNAME
YOUR_GOOGLE_SCHOLAR_ID
论文标题、合作者、期刊、arXiv、DOI、PDF 链接
```

可以直接用 VS Code、Cursor、Notepad++ 或任意文本编辑器打开 HTML 文件修改。

## 第二步：创建 GitHub Pages 仓库

假设你的 GitHub 用户名是：

```text
yourgithubname
```

创建一个 public repository，名字必须是：

```text
yourgithubname.github.io
```

然后把本文件夹中的所有文件上传到仓库根目录。

上传后，你的网站会是：

```text
https://yourgithubname.github.io
```

## 第三步：开启 GitHub Pages

进入仓库：

```text
Settings → Pages
```

选择：

```text
Deploy from a branch
Branch: main
Folder: /root
```

保存。

## 第四步：添加 CV 和论文 PDF

- 把你的 CV 放到：`cv/cv.pdf`
- 把论文 PDF 放到：`papers/your-paper-title.pdf`
- 然后在 `writing.html` 里改链接。

## 第五步：绑定自定义域名，等以后再做

如果你以后买了 `yourname.com`，再做这一步：

1. 把 `CNAME.example` 改名为 `CNAME`。
2. 把里面的 `yourname.com` 改成你的真实域名。
3. 在域名服务商那里设置 DNS。
4. 在 GitHub Pages 设置里填入 custom domain。

在没有买域名之前，不要把 `CNAME.example` 改名为 `CNAME`。

## 第六步：搜索引擎优化

等最终网址确定以后：

1. 把每个 HTML 文件里的 `https://yourname.com/` 改成你的真实网址。
2. 把 `sitemap.xml.example` 里的域名改成真实网址。
3. 将 `sitemap.xml.example` 改名为 `sitemap.xml`。
4. 在 `robots.txt` 中取消 sitemap 那一行的注释。
5. 在 Google Scholar、arXiv、ORCID、GitHub profile、学校主页里都放上这个主页链接。

## 中国大陆访问注意

为了尽量提高中国大陆直接访问的稳定性，这个模板故意没有使用：

- Google Fonts
- Google Analytics
- YouTube embed
- 外部 CDN
- JavaScript 框架

如果你托管在 GitHub Pages，中国大陆访问仍可能受 GitHub 本身影响；但纯静态、无外部依赖会比复杂模板更稳。
