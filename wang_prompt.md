# Wang Prompt Log

## 2026-10-12-15-53
**Model:** longcat-2.5-preview-free

**Prompt 1:**
> Create or update `AGENTS.md` for this repository.
>
> The goal is a compact instruction file that helps future OpenCode sessions avoid mistakes and ramp up quickly. Every line should answer: "Would an agent likely miss this without help?" If not, leave it out.
>
> User-provided focus or constraints (honor these):
>
> ## How to investigate
>
> Read the highest-value sources first:
> - `README*`, root manifests, workspace config, lockfiles
> - build, test, lint, formatter, typecheck, and codegen config
> - CI workflows and pre-commit / task runner config
> - existing instruction files (`AGENTS.md`, `CLAUDE.md`, `.cursor/rules/`, `.cursorrules`, `.github/copilot-instructions.md`)
> - repo-local OpenCode config such as `opencode.json`
>
> If architecture is still unclear after reading config and docs, inspect a small number of representative code files to find the real entrypoints, package boundaries, and execution flow. Prefer reading the files that explain how the system is wired together over random leaf files.
>
> Prefer executable sources of truth over prose. If docs conflict with config or scripts, trust the executable source and only keep what you can verify.
>
> ## What to extract
>
> Look for the highest-signal facts for an agent working in this repo:
> - exact developer commands, especially non-obvious ones
> - how to run a single test, a single package, or a focused verification step
> - required command order when it matters, such as `lint -> typecheck -> test`
> - monorepo or multi-package boundaries, ownership of major directories, and the real app/library entrypoints
> - framework or toolchain quirks: generated code, migrations, codegen, build artifacts, special env loading, dev servers, infra deploy flow
> - repo-specific style or workflow conventions that differ from defaults
> - testing quirks: fixtures, integration test prerequisites, snapshot workflows, required services, flaky or expensive suites
> - important constraints from existing instruction files worth preserving
>
> Good `AGENTS.md` content is usually hard-earned context that took reading multiple files to infer.
>
> ## Questions
>
> Only ask the user questions if the repo cannot answer something important. Use the `question` tool for one short batch at most.
>
> Good questions:
> - undocumented team conventions
> - branch / PR / release expectations
> - missing setup or test prerequisites that are known but not written down
>
> Do not ask about anything the repo already makes clear.
>
> ## Writing rules
>
> Include only high-signal, repo-specific guidance such as:
> - exact commands and shortcuts the agent would otherwise guess wrong
> - architecture notes that are not obvious from filenames
> - conventions that differ from language or framework defaults
> - setup requirements, environment quirks, and operational gotchas
> - references to existing instruction sources that matter
>
> Exclude:
> - generic software advice
> - long tutorials or exhaustive file trees
> - obvious language conventions
> - speculative claims or anything you could not verify
> - content better stored in another file referenced via `opencode.json` `instructions`
>
> When in doubt, omit.
>
> Prefer short sections and bullets. If the repo is simple, keep the file simple. If the repo is large, summarize the few structural facts that actually change how an agent should work.
>
> If `AGENTS.md` already exists at `E:\goajiwangyesheji-1`, improve it in place rather than rewriting blindly. Preserve verified useful guidance, delete fluff or stale claims, and reconcile it with the current codebase.

**Prompt 2:**
> 新建12-1.html.展示web前端的长度单位。

**Prompt 3:**
> 所有css类名，id名、js变量都以wang_开始，所有的提示词都在执行之前写入文件wang_prompt.md，以附加的方式写入，不覆盖之前的内容，写入的内容包括时间yyyy-mm-dd-hh-mm、使用的模型、提示词内容。

---

## 2026-10-12-15-55
**Model:** longcat-2.5-preview-free

**Prompt 4:**
> 所有css类名，id名、js变量都以wang_开始，所有的提示词都在执行之前写入文件wang_prompt.md，以附加的方式写入，不覆盖之前的内容，写入的内容包括时间yyyy-mm-dd-hh-mm、使用的模型、提示词内容。

---

## 2026-10-12-15-57-42
**Model:** longcat-2.5-preview-free

**Prompt 5:**
> 修改所有css类名，id名、js变量都以wang_开始，所有的提示词都在执行之前写入文件wang_prompt.md，以附加的方式写入，不覆盖之前的内容，写入的内容包括时间yyyy-mm-dd-hh:mm:ss、使用的模型、提示词内容。

---

## 2026-10-12-16-19-37
**Model:** longcat-2.5-preview-free

**Prompt 6:**
> 完成12-2.html.  展示css3 3d动画

---

## 2026-10-12-16-29-05
**Model:** longcat-2.5-preview-free

**Prompt 7:**
> 设置规则,写入agents.md：新建的html文件加入超链接到首页index.html

---

## 2026-10-12-16-30-15
**Model:** longcat-2.5-preview-free

**Prompt 8:**
> 设置规则,写入agents.md：新建的html文件加入超链接到首页index.html

---

## 2026-10-12-16-31-00
**Model:** longcat-2.5-preview-free

**Prompt 9:**
> 设置规则,写入agents.md：新建的html文件加入超链接到首页index.html

---

## 2026-10-12-16-48-51
**Model:** longcat-2.5-preview-free

**Prompt 10:**
> 新建12-3.html. css 3D 立体菜单网页和3D 透视效果演示页

---

## 2026-10-26-16-10
**Model:** Trae proprietary model

**Prompt 11:**
> 从现在开始，所有css类名，id名、js变量都以wxn_开始，所有的提示词都在执行之前写入文件wang_prompt.md，以附加的方式写入，不覆盖之前的内容，写入的内容包括时间yyyy-mm-dd-hh-mm、使用的模型、提示词内容。

---

## 2026-10-26-16-19
**Model:** Trae proprietary model

**Prompt 12:**
> 提交到github

---

## 2026-10-26-16-24
**Model:** Trae proprietary model

**Prompt 13:**
> 修改6.html,把所有css类名，id名、js变量都以wxn_开始，再次重新提交到github

---

## 2026-10-26-16-29
**Model:** Trae proprietary model

**Prompt 14:**
> 创建16-2.html，展示javascript程序结构:条件，循环。
> 然后提交到github。

---

## 2026-10-29-15-38
**Model:** Trae proprietary model

**Prompt 15:**
> 编写17-1.html,形象地展示javascript主要的数组方法。

---

## 2026-10-29-15-51
**Model:** Trae proprietary model

**Prompt 16:**
> 生成17-2.html,形象展示javascript的对象和字符串。

---

## 2026-10-29-15-56
**Model:** Trae proprietary model

**Prompt 17:**
> 把17-1.html和17-2.html,提交到GitHub

---

## 2026-10-29-16-07
**Model:** Trae proprietary model

**Prompt 18:**
> @".opencode\skills\gitee-push\SKILL.md" 根据该技能创建wokebuddy技能的创建。

---

## 2026-10-29-16-10
**Model:** Trae proprietary model

**Prompt 19:**
> 把17-1.html和17-2.html,提交到GitHub

---

## 2026-10-29-16-15
**Model:** Trae proprietary model

**Prompt 20:**
> 同步

---

## 2026-10-29-16-22
**Model:** Trae proprietary model

**Prompt 21:**
> @image#1:Clipboard_Screenshot.png 完成17-3.html，根据给定图片完成网页，尽可能和原图相似，图片去京东热卖商城的网页里挑

---

## 2026-10-29-16-33
**Model:** Trae proprietary model

**Prompt 22:**
> 创建17-4.html,是tab显示卡，@image#1:1.jpg @image#2:2.jpg @image#3:3.jpg 根据这三张图片实现多动态网页，尽可能和原图里的文字相似，三张图片可以互相点击转换。

---

## 2026-10-29-16-37
**Model:** Trae proprietary model

**Prompt 23:**
> 上传到GitHub

---
