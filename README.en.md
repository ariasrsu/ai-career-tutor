# AI Career Tutor

[简体中文](README.md) · [AI learning resources](#ai-learning-resources)

AI Career Tutor is a local learning tool for people entering AI from backgrounds outside computer science. Work through a generative AI product case in the blackboard classroom, or use the standalone tutor skill to study concepts, practice exercises, and prepare for interviews.

| I want to… | Start here |
| --- | --- |
| Learn how generative AI product managers work | [Start the classroom](#start-the-classroom) |
| Practice with Codex, plan my learning, or do a mock interview | [Use the tutor skill on its own](#use-the-tutor-skill-on-its-own) |
| Find AI books, courses, and papers, and download searchable excerpts | [Browse AI learning resources](#ai-learning-resources) |

## Start the classroom

You need Node.js 18 or later and npm. Clone the repository with Git, or select **Code → Download ZIP** on GitHub, extract the archive, and open the `classroom` directory.

```bash
git clone https://github.com/ariasrsu/ai-career-tutor.git
cd ai-career-tutor/classroom
npm ci
npm run dev
```

Open [http://127.0.0.1:3000](http://127.0.0.1:3000). The server listens on your machine only. Lessons, built-in exercises, and notes work without signing in to a model.

For live tutoring, sign in to Codex on your machine and click **连接实时 AI 导师** (Connect to the live AI tutor). If you have the Codex CLI, use `codex login` to sign in and `codex login status` to check your session. Live tutoring requires a network connection and available usage. The classroom has no separate API key field.

## Eight-week curriculum

Across 24 original lessons, you design a marketing asset generator for small and midsize businesses. Each lesson has two blackboard pages, teaching notes, a comprehension check, a transfer exercise, and a deliverable. The classroom and lesson content are in Chinese.

| Week | Module | What you will make |
| --- | --- | --- |
| 1 | Users and product opportunities | A one-page user and problem definition |
| 2 | Generative AI foundations | A comparison of capabilities and limitations |
| 3–4 | Creative workflow design | A clickable workflow prototype |
| 5–6 | Evaluation, safety, and experimentation | An evaluation set, risk checklist, and experiment plan |
| 7 | Delivery and growth | A cost, funnel, and launch plan |
| 8 | Portfolio project | A generative AI product requirements document and an interview-ready case study |

Read the blackboard, try an exercise, then ask the tutor to review your own answer. Open **学习数据** (Learning data) to see your practice progress or export a JSON record.

## Use the tutor skill on its own

Copy the root [SKILL.md](SKILL.md) and the complete [references/](references/) directory into a skill folder named `ai-career-tutor`. In another Codex project, use this folder layout.

```text
.agents/skills/ai-career-tutor/
├── SKILL.md
└── references/
```

The standalone skill covers **AI product management, AI operations, and AI application development**. It can adapt a learning plan to your goals, experience, and available time. The classroom bundles the same tutor rules, which default to Chinese instruction.

- **Learn a concept.** Use `$ai-career-tutor` to explain RAG through a product search example. Ask one question, then wait for my answer before giving feedback.
- **Plan your learning.** I'm moving from content operations into AI product management and can study five hours a week. Give me a two-week plan with a deliverable for each week.
- **Practice an interview.** Use this job description and my actual project experience for a mock interview. Ask one question at a time and give feedback and a follow-up after I answer.

## AI learning resources

[Browse 34 AI learning resources](resources/README.md), including books, courses, papers, and practical guides. The catalog lists the author, official access link, and licensing notes for each source. Follow the official links to read the complete materials.

- [Download the excerpts and source index (JSONL.GZ)](https://raw.githubusercontent.com/ariasrsu/ai-career-tutor/main/resources/fragments.jsonl.gz). **3,557 entries include short excerpts**, and **24,895 contain source locations only**. Extract the file to search it with a tool that supports JSONL.
- [View the machine-readable source catalog (JSON)](resources/sources.json). Use `source_id` to look up the title, author, license, and access link.
- **Use your own materials in class.** Import Markdown or TXT notes into the classroom library. You can browse the download on its own. Searching textbooks inside the classroom requires a local index.

To connect a textbook index to the classroom, set `KNOWLEDGE_INDEX_SCRIPT` to a Python program that supports `status`, `search`, and `files` and returns JSON. See [classroom/server.mjs](classroom/server.mjs) for the interface.

## Data and privacy

- Practice progress, answers, and classroom notes are saved in the current browser. A learning record export includes progress and notes and excludes the original teaching materials. Export a backup before switching browsers.
- Markdown and TXT files imported through the local server go into `classroom/materials/`, which Git ignores by default.
- Live tutoring sends your question, lesson context, and matching excerpts from notes or the configured textbook index to the model. Only import material you have permission to use with the service. Restarting the local server may require you to start a new live tutoring session.

## Troubleshooting

| Problem | What to check |
| --- | --- |
| The server fails to start or the page won't open | Run `npm ci` and `npm run dev` in `classroom`, then open the address printed in the terminal. |
| Port 3000 is already in use | On macOS or Linux, run `PORT=3100 npm run dev`. In PowerShell, run `$env:PORT = "3100"`, then `npm run dev`. |
| Lessons open, but the live tutor can't connect | Check your Codex sign-in, network connection, and available usage. Lessons and exercises are still available. |
| The textbook citations are empty | You can download the public dataset separately. To search textbook citations inside the classroom, connect a local index. |

## Repository layout and licensing

| Path | Contents |
| --- | --- |
| [classroom/](classroom/) | Chinese classroom, curriculum data, and local server |
| [SKILL.md](SKILL.md) and [references/](references/) | Standalone tutor skill and rules for teaching, evidence, knowledge sources, and interviews |
| [resources/](resources/) | AI learning resources, downloadable excerpts and source index, and third-party licenses |

Teaching excerpts retain their original licenses. See the [source catalog](resources/README.md) for details. The repository currently has no declared project-wide open-source license for its code.
