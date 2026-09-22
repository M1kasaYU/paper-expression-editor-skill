# Paper Expression Editor Skill

English · [简体中文](README.md)

A Codex skill for reviewing and improving existing drafts of Chinese academic papers, theses, research proposals, and research reports. It locates observable AI-like writing patterns such as formulaic phrases, mechanical sentence structures, empty transitions, repetitive summaries, and vague claims; explains each issue; and provides meaning-preserving suggestions or ready-to-use replacements. Revisions protect research facts, data, citations, terminology, research stage, causal relations, and conclusion boundaries.

## What it does

- **Review only:** locate concrete issues by section, paragraph, or sentence, and explain why they matter.
- **Revise:** provide usable replacement text while checking terms, numbers, citations, comparison conditions, and the strength of conclusions.
- **Support manual edits:** return exact, continuous source text that can be searched in Word, together with complete replacement text.
- **Apply requested style preferences:** review repeated semicolons, empty perspective phrases, parallel paragraph openings, author-reference wording, and heading punctuation when the user or target style guide calls for it.
- **Audit meaning:** create a Meaning Lock before substantive edits and follow `Lock → Diagnose → Decide → Revise → Audit`.

The skill distinguishes wording edits from factual gaps. It does not invent experiments, results, sources, or limitations to make a passage sound more polished.

## Install

Copy the entire [`paper-expression-editor/`](paper-expression-editor/) directory into your Codex skills directory, usually `~/.codex/skills/`, so the entry point is `~/.codex/skills/paper-expression-editor/SKILL.md`. After this repository is published, you can also install that subdirectory with the Codex skill installer. Start a new session if the skill does not appear immediately.

## Use

```text
$paper-expression-editor Review the wording of this Chinese research proposal. Identify formulaic transitions and repetitive paragraph structures. Give me exact source text I can find in Word, a reason for each change, and complete replacement text. Preserve statements about work that is only planned.
```

```text
$paper-expression-editor Revise this section of my paper for clear, natural academic Chinese. Preserve every number, formula, citation, comparison condition, and conclusion boundary. List any claim that needs source verification.
```

For an AI tool that does not support Codex skills, copy the standalone [Chinese prompt](01-直接使用的主提示词.md) and provide the text to edit. Adapt the prompt's optional personal style preferences to your supervisor, institution, or target journal.

## Repository layout

```text
.
├── README.md
├── README_EN.md
├── LICENSE
├── 01-直接使用的主提示词.md
└── paper-expression-editor/
    ├── SKILL.md
    └── references/
        ├── review-checklist.md
        ├── revision-guide.md
        ├── fact-check.md
        ├── core-contract.md
        ├── meaning-audit.md
        ├── issue-taxonomy.md
        ├── output-formats.md
        └── style-profile.md
    └── examples/
        ├── sentence-cases.md
        ├── document-type-cases.md
        └── full-review-example.md
```

The skill loads references as needed. When using the standalone prompt elsewhere, attach any additional reference files you want the AI to follow; naming a file alone does not give the AI access to it.

## Scope

Review only the material actually provided. A passage cannot establish the style of a whole paper, and extracted text alone cannot verify figures or final layout. Common academic terms, parallel structure, semicolons, and phrases such as “from this perspective” are not errors by themselves. Follow the user's instructions and applicable institutional or journal requirements for wording, citation style, and disclosure of AI assistance.

## Method

1. **Lock:** record research stage, scope, numbers, citations, terminology, and conclusion strength.
2. **Diagnose:** locate evidence-based issues across facts, scope, logic, paragraphs, sentences, and wording.
3. **Decide:** choose `KEEP`, `REVISE`, `DELETE`, or `AUTHOR_CHECK` for each candidate.
4. **Revise:** make the smallest change that resolves the issue and keep sound sentences.
5. **Audit:** compare source and revision for factual, citation, stage, causal, and scope drift.

## Design and license

This project is an evidence-preserving expression editor for Chinese academic writing. It revises only on the basis of observable language and argumentation issues, while preserving research stage, facts, numbers, citations, causal direction, and conclusion boundaries.

Edits follow the priority “facts > scope > logic > paragraphs > sentences > wording”. Candidate patterns (e.g. perspective openers, semicolons, repeated frames) are review clues, not errors; keep or revise only after checking their semantic function.

This repository uses the MIT License; see [LICENSE](LICENSE).
