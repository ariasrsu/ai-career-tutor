# AI 转行导师

[English](README.en.md) · [教材来源与片段](resources/README.md)

一套面向非计算机专业背景学习者的本地 AI 学习工具。你可以沿着黑板课堂完成一个 AIGC 产品案例，也可以单独使用导师 Skill 学概念、做练习和模拟面试。

| 你想做什么 | 从哪里开始 |
| --- | --- |
| 系统学 AIGC 产品经理的工作方法 | [启动黑板课堂](#启动黑板课堂) |
| 在 Codex 里练习、制定学习路线或模拟面试 | [独立使用导师 Skill](#独立使用导师-skill) |
| 找第二期视频里的教材、出处和短摘录 | [第二期教材资源](#第二期教材资源) |

## 启动黑板课堂

需要 Node.js 18 或更高版本和 npm。通过 Git 克隆仓库，或用 GitHub 的 **Code → Download ZIP** 下载并解压，然后进入 `classroom` 目录。

```bash
git clone https://github.com/ariasrsu/ai-career-tutor.git
cd ai-career-tutor/classroom
npm ci
npm run dev
```

打开 [http://127.0.0.1:3000](http://127.0.0.1:3000)。服务只监听本机。课程、课堂练习和笔记无需模型登录。

要使用实时辅导，在本机完成 Codex 登录，再点击 **连接实时 AI 导师**。已安装 Codex CLI 时，可以用 `codex login` 登录，用 `codex login status` 检查状态。实时对话需要网络和可用额度，课堂网页无需另外填写 API 密钥。

## 8 周课程

24 节原创课围绕「给中小商家做营销素材生成工作台」展开。每节课包含两页板书、讲课笔记、理解题、迁移题和一项可交付练习。课程界面和板书使用中文。

| 周次 | 模块 | 你会完成 |
| --- | --- | --- |
| 1 | 用户与产品机会 | 一页目标用户与问题定义 |
| 2 | 生成技术基础 | 一张生成能力与限制对照表 |
| 3–4 | 创作工作流设计 | 一个可点击的创作流程原型 |
| 5–6 | 评测、安全与实验 | 一套评测集、风险清单和实验方案 |
| 7 | 交付与增长 | 成本、漏斗和发布方案 |
| 8 | 作品集实战 | 一份 AIGC 产品 PRD 和可用于面试的项目案例 |

可以先读板书、做一道练习，再拿自己的答案向导师追问。做完一节课后，用 **学习数据** 查看练习进度，或导出学习记录 JSON。

## 独立使用导师 Skill

将仓库根目录的 [SKILL.md](SKILL.md) 和整个 [references/](references/) 目录一起复制到助手的 Skill 目录，命名为 `ai-career-tutor`。在另一个 Codex 项目中，可以使用下面的目录结构。

```text
.agents/skills/ai-career-tutor/
├── SKILL.md
└── references/
```

独立 Skill 可以覆盖 **AI 产品、AI 运营、AI 应用开发**，并按你的目标、已有能力和可投入时间制定路线。课堂内已包含同一套导师规则。

- **学概念。** 使用 `$ai-career-tutor`，用商品搜索讲清楚 RAG。出一道题，等我回答再批改。
- **定路线。** 我从内容运营转 AI 产品，每周能投入 5 小时。帮我定两周任务，写清每周要交付什么。
- **练面试。** 根据这份 JD 和我的真实项目经历做模拟面试。每次问一道题，等我回答再给反馈和追问。

## 第二期教材资源

[教材资源页](resources/README.md) 汇总 **34 组来源**，列出作者、官方获取入口和许可说明。公开数据覆盖 **28,452 条出处位置**，其中 **3,557 条带短摘录**，其余 **24,895 条提供出处位置**。

- [下载片段包（JSONL.GZ）](https://raw.githubusercontent.com/ariasrsu/ai-career-tutor/main/resources/fragments.jsonl.gz)，解压后可交给支持 JSONL 的工具检索。
- [下载来源清单（JSON）](resources/sources.json)，用 `source_id` 查书名、作者、许可和获取入口。全文从作者、出版社或项目官网获取。
- **课堂里的资料库**支持导入自己的 Markdown 或 TXT 笔记。正式教材索引需要自行接入，片段下载包可以独立查阅。

若要给课堂接入自己的正式教材索引，可将 `KNOWLEDGE_INDEX_SCRIPT` 指向一个支持 `status`、`search` 和 `files` 并返回 JSON 的 Python 程序。接口行为见 [classroom/server.mjs](classroom/server.mjs)。

## 数据与隐私

- 练习进度、答案和课堂笔记保存在当前浏览器。导出的学习记录包含进度和笔记，不附教材原文。更换浏览器前可先导出备份。
- 通过本地服务导入的 MD/TXT 资料存放在 `classroom/materials/`，默认被 Git 忽略。
- 使用实时导师时，当前问题、课堂状态和命中的笔记或教材摘录会发送给模型。请只导入你有权用于该服务的资料。重启本地服务后，实时对话会话可能需要重新开启。

## 常见问题

| 遇到什么 | 可以检查什么 |
| --- | --- |
| 启动报错或页面打不开 | 确认在 `classroom` 目录运行 `npm ci` 和 `npm run dev`，再打开终端显示的地址。 |
| 3000 端口已被占用 | macOS / Linux 可运行 `PORT=3100 npm run dev`。PowerShell 可先运行 `$env:PORT = "3100"`，再运行 `npm run dev`。 |
| 能读课，但导师连不上 | 查看 Codex 登录、网络和可用额度。课程和练习仍可使用。 |
| 教材出处为空 | 公开片段包可独立下载。要在课堂内查正式教材出处，需要接入本地索引。 |

## 仓库目录与许可

| 路径 | 内容 |
| --- | --- |
| [classroom/](classroom/) | 中文课堂页面、课程数据和本地服务 |
| [SKILL.md](SKILL.md) 和 [references/](references/) | 独立导师 Skill 及教学、证据、资料库和面试规则 |
| [resources/](resources/) | 第二期教材来源、片段包与第三方许可 |

教材摘录沿用各自的原始许可证，详见 [教材来源表](resources/README.md)。仓库目前没有为项目代码声明统一的开源许可证。
