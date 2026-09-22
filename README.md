# Paper Expression Editor Skill（论文去AI化表述）

[English](README_EN.md) · 中文

一个面向**已有初稿**的中文学术表达审查与优化 Skill，适用于学术论文、学位论文、开题报告和研究报告。它可以逐段定位模板化套话、机械句架、无效过渡、重复总结、空泛评价等可观察的“AI 化表达痕迹”，说明具体问题及判断依据，并提供保留原意的优化建议或可直接使用的替换稿。修改过程中会保护研究事实、数据、引用、术语、研究阶段、因果关系和结论边界。

## 能做什么

- **只评阅：**按章节或段落指出有证据的表达问题，给出原句、位置与修改建议。
- **直接改写：**交付可使用的文字，并核对事实、术语、数字、引文和结论范围。
- **边查边改：**为需要手动修改的用户提供可在 Word 中搜索的连续原文和完整替换稿。
- **按要求统一写法：**可以检查分号堆叠、观察角度式起句、相邻段落同构、作者“等人”写法及标题标点。具体写法以用户、导师、学校或期刊的要求为准。
- **保真审计：**先建立 Meaning Lock，再按 `Lock → Diagnose → Decide → Revise → Audit` 工作流交付修改和语义审计。

改写前会区分研究事实、作者解释、尚待验证的计划和纯语言问题。资料不足时标明缺口，不补造实验结果、文献或结论。

## 安装与使用

本仓库的 Skill 目录是 [`paper-expression-editor/`](paper-expression-editor/)。将**整个目录**复制到 Codex 的个人技能目录（通常为 `~/.codex/skills/`），使路径成为 `~/.codex/skills/paper-expression-editor/SKILL.md`。也可以使用 Codex 的 Skill 安装器，从发布后的 GitHub 仓库路径安装 `paper-expression-editor` 子目录。安装后如未自动出现，可重新打开会话。

示例：

```text
$paper-expression-editor 请只评阅这份开题报告的正文表达，不修改图示。逐段定位空转起句、重复句架和同段多分号；给我可在 Word 中搜索的原文、修改理由与建议替换稿。保留“拟、计划、预期”等研究阶段。
```

```text
$paper-expression-editor 请改写这段论文，减少套话和重复总结。保留所有数据、公式、引文、比较条件与结论范围；材料不足之处单列待核验。
```

不使用 Codex Skill 时，也可复制根目录的 [`01-直接使用的主提示词.md`](01-直接使用的主提示词.md)，连同论文文本一起发给其他 AI。该文件包含一组可覆盖的个人中文写作偏好；使用时应按自己的导师和投稿规范修改。

## 目录

```text
.
├── README.md
├── README_EN.md
├── LICENSE
├── 01-直接使用的主提示词.md
└── paper-expression-editor/
    ├── SKILL.md
    └── references/
        ├── review-checklist.md   # 六层评阅清单
        ├── revision-guide.md     # 六层改写指南
        ├── fact-check.md         # 分级冻结复核
        ├── core-contract.md      # 语义保真与最小修改
        ├── meaning-audit.md      # 改写后语义审计
        ├── issue-taxonomy.md     # 问题分类
        ├── output-formats.md     # 输出协议
        └── style-profile.md      # 风格偏好档案
    └── examples/
        ├── sentence-cases.md
        ├── document-type-cases.md
        └── full-review-example.md
```

Skill 会按当前任务读取对应指南。独立使用主提示词时，它本身可以直接复制；如果想让其他 AI 参照 `references/` 中的指南，需要实际上传这些文件或提供文件访问权限。

## 使用边界

- 只评价实际看到的材料。片段不能代表全文，文字提取不能代替图示或最终版式检查。
- 正常的学术术语、平行结构、分号和“从……看”不应仅因形式而被判为问题。
- “等人”、标题顿号和分号偏好是可选写作要求，不是所有中文论文的统一规则。
- AI 辅助润色应遵守所在学校、期刊或项目适用的披露与学术规范。

## 工作方法

1. **Lock：**提取研究状态、范围、数字、引用、术语和结论强度等语义锚点。
2. **Diagnose：**按事实、范围、逻辑、段落、句式、词汇六层定位有证据的问题。
3. **Decide：**对候选表达作出 `KEEP`、`REVISE`、`DELETE` 或 `AUTHOR_CHECK` 决策。
4. **Revise：**使用与问题范围相称的最小修改，保留没有问题的句子。
5. **Audit：**比较原文与改写稿，核对事实、引用、研究阶段、因果关系和结论边界。

## 设计定位与许可

本项目是一个面向中文科研写作的 evidence-preserving expression editor：以可观察的语言和论证问题为依据进行审校，在改写中保护研究阶段、事实、数字、引用、因果关系和结论边界。

写作修改遵循“事实 > 范围 > 逻辑 > 段落 > 句式 > 词汇”的优先级；候选模式（如“从……看”、分号、重复句架）只作为复查线索，先判断语义功能再决定保留或修改。

本仓库采用 MIT License，详见 [LICENSE](LICENSE)。
