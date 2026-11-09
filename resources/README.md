# 第二期 AI 导师教材片段

这份发布包含视频里的 **28,452 条位置记录**，覆盖 **34 组资料**。其中 **3,557 条**带短摘录，来自 **8 组**许可覆盖公开分享的资料。其他条目提供来源 ID 和原文位置。教材原文件请从下表的官方入口获取，PDF 位置是文件页序。版本不同可能导致页码变化。

- [下载片段包（JSONL.GZ）](https://raw.githubusercontent.com/ariasrsu/ai-career-tutor/main/resources/fragments.jsonl.gz)
- [来源、作者和许可（JSON）](sources.json)

下载并解压后，每行是一条 JSON 记录。使用 `source_id` 关联来源表，`locator` 是页序、Notebook 单元或行号。含 `excerpt` 的条目才有正文。部分上游 Git 项目还提供固定提交的 `source_file_url`。可以将文件交给支持 JSONL 的 Agent，先按 `excerpt` 检索，再按 `source_id` 查作者、书名和来源。课堂的内置教材库需要另外接入本地索引。

短摘录经过选段、去重和空白归一。每条至多 320 个字符，且至多占对应本地片段的四分之一。第三方内容沿用表中各自的许可，仓库未对这些摘录统一重新授权。来源条目中的 `license_file` 或 `license_evidence` 记录上游许可依据。

| ID | 资料及官方入口 | 作者或机构 | 许可或获取方式 | 位置记录 | 含摘录 |
| --- | --- | --- | --- | ---: | ---: |
| `book-01` | [Think Python, 3rd Edition](https://allendowney.github.io/ThinkPython/) | Allen B. Downey | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)。目录；保留原作的非商用和相同方式共享条件 | 1,070 | 0 |
| `book-02` | [Python for Everybody](https://www.py4e.com/book) | Charles R. Severance | [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/)。目录；采用本次所用 PDF 版权页的许可 | 384 | 0 |
| `book-03` | [Automate the Boring Stuff with Python, 3rd Edition](https://automatetheboringstuff.com/) | Al Sweigart | [作者官网在线阅读](https://automatetheboringstuff.com/)。目录；从作者网站阅读 | 747 | 0 |
| `book-06` | [Pro Git, 2nd Edition](https://git-scm.com/book/en/v2) | Scott Chacon、Ben Straub | [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/)。目录；保留原作的非商用和相同方式共享条件 | 833 | 0 |
| `book-08` | [Mathematics for Machine Learning](https://mml-book.github.io/) | Marc Peter Deisenroth、A. Aldo Faisal、Cheng Soon Ong | [作者提供 PDF](https://mml-book.github.io/)。目录；以官网所用版本的条款为准 | 869 | 0 |
| `book-09` | [OpenIntro Statistics, 4th Edition](https://www.openintro.org/book/os/) | David M. Diez、Mine Çetinkaya-Rundel、Christopher D. Barr | [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)。摘录；2019 年第四版，沿用原许可 | 950 | 790 |
| `book-10` | [Think Stats, 3rd Edition](https://allendowney.github.io/ThinkStats/) | Allen B. Downey | [正文 CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)。目录；正文与代码许可分开 | 923 | 0 |
| `book-11` | [Practical Statistics for Data Scientists, 2nd Edition](https://www.oreilly.com/library/view/practical-statistics-for/9781492072935/) | Peter Bruce、Andrew Bruce、Peter Gedeck | [保留所有权利](https://www.oreilly.com/library/view/practical-statistics-for/9781492072935/copyright-page01.html)。目录；出版社入口 | 592 | 0 |
| `book-12` | [Bayesian Methods for Hackers](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers) | Cameron Davidson-Pilon 与项目贡献者 | [MIT](licenses/book-12.txt)。摘录；取自上游项目 notebook | 280 | 199 |
| `book-13` | [Probabilistic Machine Learning: An Introduction](https://probml.github.io/pml-book/book1.html) | Kevin P. Murphy | [CC BY-NC-ND](https://probml.github.io/pml-book/book1.html)。目录；作者官方版本 | 1,741 | 0 |
| `book-15` | [An Introduction to Statistical Learning with Applications in Python](https://www.statlearning.com/) | Gareth James、Daniela Witten、Trevor Hastie、Robert Tibshirani、Jonathan Taylor | [作者提供 PDF](https://www.statlearning.com/)。目录；从官网获取 | 1,371 | 0 |
| `book-17` | [Machine Learning Yearning](https://info.deeplearning.ai/machine-learning-yearning-book) | Andrew Ng | [官网提供电子书](https://info.deeplearning.ai/machine-learning-yearning-book)。目录；从官方入口获取 | 154 | 0 |
| `book-18` | [Dive into Deep Learning](https://d2l.ai/) | Aston Zhang、Zachary C. Lipton、Mu Li、Alexander J. Smola | [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)。摘录；取自官方开源版，沿用原许可 | 2,155 | 1,820 |
| `book-19` | [Deep Learning](https://www.deeplearningbook.org/) | Ian Goodfellow、Yoshua Bengio、Aaron Courville | [作者官网在线阅读](https://www.deeplearningbook.org/)。目录；从作者网站阅读 | 1,416 | 0 |
| `book-20` | [Neural Networks and Deep Learning](https://neuralnetworksanddeeplearning.com/) | Michael Nielsen | [CC BY-NC 3.0](https://creativecommons.org/licenses/by-nc/3.0/)。目录；从作者网站阅读 | 427 | 0 |
| `book-21` | [Deep Learning for Coders with fastai and PyTorch](https://github.com/fastai/fastbook) | Jeremy Howard、Sylvain Gugger | [代码 GPL-3.0；正文禁止再分发](https://github.com/fastai/fastbook#copyright)。目录；上游 README 单列正文条款 | 1,507 | 0 |
| `book-22` | [Understanding Deep Learning](https://udlbook.github.io/udlbook/) | Simon J. D. Prince | [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)。目录；从作者网站获取对应版 PDF | 1,156 | 0 |
| `book-24` | [Speech and Language Processing, 3rd Edition Draft](https://web.stanford.edu/~jurafsky/slp3/) | Daniel Jurafsky、James H. Martin | [作者公开草稿](https://web.stanford.edu/~jurafsky/slp3/)。目录；本地位置对应 2026-01-06 草稿，后续版本页码可变 | 1,672 | 0 |
| `book-28` | [Foundations of Large Language Models](https://arxiv.org/abs/2501.09223) | Tong Xiao、Jingbo Zhu | [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)。目录；从作者 arXiv 页面获取 | 763 | 0 |
| `book-30` | [AI Engineering](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) | Chip Huyen | [出版社商业教材](https://huyenchip.com/books/#ai-engineering-oreilly-2025)。目录；出版社入口 | 985 | 0 |
| `alternative-16` | [Machine learning in Python with scikit-learn](https://inria.github.io/scikit-learn-mooc/) | Inria 与 scikit-learn MOOC 团队 | [CC BY 4.0](licenses/alternative-16.txt)。摘录；上游课程资料 | 1,521 | 541 |
| `alternative-25` | [Hugging Face LLM Course](https://github.com/huggingface/course) | Hugging Face 与课程贡献者 | [Apache-2.0](licenses/alternative-25.txt)。摘录；上游课程仓库文档 | 206 | 164 |
| `alternative-26` | [LLMs from Scratch companion repository](https://github.com/rasbt/LLMs-from-scratch) | Sebastian Raschka 与项目贡献者 | [Apache-2.0（配套仓库）](licenses/alternative-26.txt)。摘录；取自配套仓库，商业图书正文另有权利 | 1,330 | 23 |
| `alternative-31` | [Hugging Face Agents Course](https://github.com/huggingface/agents-course) | Hugging Face 与课程贡献者 | [Apache-2.0](licenses/alternative-31.txt)。摘录；上游课程仓库文档 | 28 | 1 |
| `alternative-36` | [LLM Course](https://github.com/mlabonne/llm-course) | Maxime Labonne 与项目贡献者 | [Apache-2.0](licenses/alternative-36.txt)。目录；本次仅发布位置记录 | 58 | 0 |
| `alternative-37` | [Made With ML](https://github.com/GokuMohandas/Made-With-ML) | Goku Mohandas / Made With ML | [MIT](licenses/alternative-37.txt)。摘录；上游项目文档 | 89 | 19 |
| `alternative-23` | [Introduction to Machine Learning Systems, Vol. I](https://github.com/harvard-edge/cs249r_book/releases/tag/vol1-v0.7.2) | Vijay Janapa Reddi | [CC BY-NC-ND；另有书内使用说明](https://github.com/harvard-edge/cs249r_book/releases/tag/vol1-v0.7.2)。目录；官方 v0.7.2 Release | 3,297 | 0 |
| `alternative-32` | [Agent Design Pattern Catalogue](https://arxiv.org/abs/2405.10467v4) | Yue Liu、Sin Kit Lo、Qinghua Lu、Liming Zhu、Dehai Zhao、Xiwei Xu、Stefan Harrer、Jon Whittle | [作者提供论文](https://arxiv.org/abs/2405.10467v4)。目录；从 arXiv 获取对应论文 | 104 | 0 |
| `alternative-48` | [Anatomy of an AI System](https://anatomyof.ai/) | Kate Crawford、Vladan Joler | [作者提供出版物](https://anatomyof.ai/)。目录；从项目网站获取 | 65 | 0 |
| `alternative-49` | [Introduction to AI Safety, Ethics, and Society](https://arxiv.org/abs/2411.01042v2) | Dan Hendrycks | [出版社开放获取版 CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)。目录；版本许可见作者和出版页面 | 1,516 | 0 |
| `alternative-38` | [Google People + AI Guidebook](https://pair.withgoogle.com/guidebook-v2/) | Google People + AI Research | [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)。目录；官方指南 | 136 | 0 |
| `alternative-39` | [Microsoft HAX Toolkit](https://www.microsoft.com/en-us/haxtoolkit/) | Microsoft Research | [官方 Toolkit；各材料条款以原站为准](https://www.microsoft.com/en-us/haxtoolkit/)。目录；官方工具包 | 35 | 0 |
| `anthropic-agent-guide` | [Anthropic Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) | Erik Schluntz、Barry Zhang / Anthropic | [官方网页在线阅读](https://www.anthropic.com/research/building-effective-agents)。目录；官方文章 | 13 | 0 |
| `google-pair-worksheets` | [Google People + AI Guidebook worksheets](https://pair.withgoogle.com/guidebook-v2/) | Google People + AI Research | [指南 CC BY-NC-SA 4.0；工作表以原件标示为准](https://creativecommons.org/licenses/by-nc-sa/4.0/)。目录；官方指南中的工作表 | 59 | 0 |
