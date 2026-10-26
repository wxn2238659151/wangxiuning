# AGENTS.md

## Overview
Static HTML coursework site ("高级网页设计" class project). Pure HTML/CSS/JS — no build step, no package manager, no framework, no tests, no CI.

## Viewing
Open `index.html` directly in a browser, or serve the root with any static server (e.g. `python -m http.server`).

## Structure
- `index.html` — main landing page
- `1.html` … `15-1.html` — individual lesson/exercise pages
- `css.css` — global stylesheet (minimal; most pages use inline `<style>`)
- `font/` — iconfont 图标资源（iconfont.css / iconfont.js / iconfont.ttf / iconfont.woff / iconfont.woff2）
- `img/` — shared images referenced via `./img/<name>.png|jpg`
- `cdn/` — ⚠️ 历史遗留第三方资源（fontawesome、lucide），**后续不再新增或使用**，新功能必须改用 `font/iconfont`

## Naming Convention
- **所有变量名、CSS 类名、id 名统一以 `wxn_` 开头**（wxn = 王秀宁）。
- 例：`wxn_header`, `wxn_button-primary`, `let wxn_userName = '';`
- 历史文件中的 `wang_` 前缀属于遗留代码，后续修改该文件时一并替换。
- 禁止使用 `app_`, `page_`, `el_` 等其它前缀。

## HTML Head Comment
每一个 HTML 文件顶部（`<!DOCTYPE html>` 之后、`<html>` 之前）必须包含以下格式的注释：
```html
<!-- 姓名：王秀宁，日期：YYYY-MM-DD，功能名称：<本页功能简述> -->
```
- 日期使用创建/最近一次实质修改的日期。
- 功能名称用一句话描述本页做什么（如"JavaScript 基础语法练习"、"Flex 布局课后作业"）。
- 范例：`<!-- 姓名：王秀宁，日期：2026-10-22，功能名称：JavaScript 输出与交互练习 -->`

## Technology Stack
- 仅使用**原生 HTML / CSS / JavaScript**，不使用任何前端框架（Vue/React/Angular 等）。
- 不引入任何第三方 JavaScript / CSS 库（CDN 或本地副本均禁止），包括但不限于 jQuery、Bootstrap、Tailwind、Lodash 等。
- ⚠️ `cdn/` 目录下的 fontawesome / lucide 为历史遗留，**禁止在新代码中引用**。

## Icons
- 统一使用 `font/` 目录下的 iconfont 图标。
- 在 `<head>` 中引入 `<link rel="stylesheet" href="./font/iconfont.css">`。
- 使用 `<i class="iconfont icon-xxx"></i>` 渲染图标。
- 禁止使用 fontawesome、lucide、emoji 作为主要图标方案。

## Data Fetching
- 与服务器端（如有）交互**必须使用原生 `fetch` API**。
- 禁止使用 axios、jQuery.ajax、XMLHttpRequest（除非为了兼容性不得已）。
- `fetch` 调用示例：
  ```javascript
  fetch('/api/xxx', { method: 'GET' })
    .then(res => res.json())
    .then(data => { /* 使用 data */ })
    .catch(err => { /* 错误处理 */ });
  ```

## Prompt Logging (before every execution)
- 在**执行任何用户指令之前**，必须先把本次用户提示词追加写入项目根目录的 `wang_prompt.md`（append-only，绝不覆盖）。
- 每条记录格式如下（Markdown 标题为时间戳，使用 `---` 与上一条分隔）：
  ```markdown
  ## yyyy-mm-dd-hh-mm
  **Model:** Trae proprietary model

  **Prompt N:**
  > 完整的用户原始提示词，用 `>` 逐行 quote 包裹

  ---
  ```
- 字段说明：
  - 时间戳格式严格为 `yyyy-MM-dd-HH-mm`（24 小时制，本地时区），使用 `Get-Date -Format "yyyy-MM-dd-HH-mm"` 或等价方式获取。
  - `Model` 固定写 `Trae proprietary model`，历史遗留条目保持原样不改动。
  - `Prompt N` 的 N 递增，取文件中最大编号 + 1。
  - Prompt 内容为用户**原始消息**全文，不做翻译、不做摘要、不做改写。
- 如果 `wang_prompt.md` 不存在则创建，首行写 `# Wang Prompt Log` 作为标题。
- 执行写入后再开始真正的用户任务，保证日志与操作一一对应。

## General Conventions
- Pages are self-contained; each has its own inline `<style>` block.
- Image paths are relative (`./img/1.png`).
- Language is Chinese (`lang="zh-CN"`).
- Every new HTML file must be added to the homepage (`index.html`) page list.
