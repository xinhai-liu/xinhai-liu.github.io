# Xinhai Liu Personal Website V2 — 编辑与维护指南

这是一个纯静态 GitHub Pages 网站，不需要数据库，也不需要 Python。

## 1. 最重要的原则
每个页面里都已经加入 `<!-- EDIT HERE: ... START -->` 与 `<!-- EDIT HERE: ... END -->`。以后只修改这两个标记之间的内容即可。

## 2. 想改什么，就改哪个文件

| 想修改的内容 | 文件 |
|---|---|
| 首页简介、首页精选内容 | `index.html` |
| 英文个人简介 / Current Roles | `about.html` |
| 总体研究方向 | `research.html` |
| 论文、报告 | `publications.html` |
| 项目 | `projects.html` |
| 著作 | `books.html` |
| 媒体文章 / 采访 / 评论 | `media.html` |
| 演讲 / 会议 / 培训 | `speaking.html` |
| 邮箱 / LinkedIn / Google Scholar | `contact.html` |
| AI & Credit Technology 专题 | `ai-credit-technology.html` |
| 6C / Network Credit 专题 | `network-credit.html` |
| MyData 专题 | `mydata.html` |
| Cross-Border Credit 专题 | `cross-border-credit.html` |

## 3. 添加一篇论文
打开 `publications.html`，找到 `PUBLICATIONS START`。复制一个完整的 `<article class="list-row">...</article>`，然后修改年份、标题、作者、期刊、简介和链接。

## 4. 添加一个项目
打开 `projects.html`，复制一个 `<article class="list-row">...</article>`。建议统一写时间、项目名称、1–2句简介和类型标签。

## 5. 添加一本书
打开 `books.html`，复制一个 `<article class="card">...</article>`。以后若加入封面，可创建 `assets/images/` 并加入 `<img src="assets/images/book-cover.jpg" alt="Book cover">`。

## 6. 修改顶部导航
顶部导航统一在 `site.js` 的 `const navItems = [...]` 里维护。修改一次，所有页面同步。

## 7. 修改颜色 / 字体 / 页面宽度
都在 `styles.css` 顶部的 `:root { ... }` 中。

## 8. 上传到 GitHub Pages
把整个文件结构上传到仓库根目录。GitHub Pages 使用 `main` + `/(root)`。

## 9. 推荐补充顺序
1. Publications：先加 10–20 篇代表作
2. Books：补出版社、封面、链接
3. Contact：补 LinkedIn / Google Scholar / ORCID
4. Speaking：补重要会议
5. Media：补代表性评论
6. 四个专题页：逐步加入图、论文、案例和合作项目


---

## 10. Books 页面（V2.2）

`books.html` 已分为四个可维护区块：

- `FEATURED BOOKS`：当前最重要的著作
- `FOUNDATIONAL BOOKS`：征信、大数据、金融科技基础著作
- `REFERENCE WORKS`：译著、工具书、编著
- `LONGFORM RESEARCH`：博士论文等长篇研究

每个区域都有 `EDIT HERE` 标记。

目前中文著作的英文标题多数是网站用的描述性翻译；拿到出版社官方英文书名后，可直接替换标题，不需要改网页结构。

如果以后加入封面：
1. 建立 `assets/images/books/`
2. 把封面图放进去
3. 可将当前 CSS 生成的“模拟封面”替换为 `<img>` 标签


---

## 11. About 页面（V2.3）

`about.html` 是网站最重要的“职业叙事”页面之一，不建议把完整简历复制进去。

四个主要维护区：

- `BIOGRAPHY`：400–600 字左右英文职业简介
- `CURRENT ROLES`：只放最能帮助海外读者理解你当前身份的任职
- `CAREER TIMELINE`：重要职业节点
- `SERVICE`：学术服务、国际交流、校友与专业社群

首页 `index.html` 也同步增加了一个简短的 Profile 段落。

以后如果任职变化，优先修改 `CURRENT ROLES`，不需要重写整个 Biography。


## GitHub 当前目录结构说明

本修正版采用扁平目录：`styles.css` 和 `site.js` 与 `index.html` 放在同一层，适配当前 GitHub 仓库。
