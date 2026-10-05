# Paper Expression Editor Skill

English · [简体中文](README.md)

A Chinese academic expression review and polishing skill for **graduate and undergraduate writers across disciplines**. It works with existing drafts of papers, theses, literature reviews, proposals, and research reports. Graduate-level rigor is the default editing goal: identify formulaic, mechanical, repetitive, or unnatural expression, explain concrete issues, and provide complete revisions. It improves accuracy, logic, coherence, and academic tone while preserving research facts, terminology, materials, data, citations, and conclusion boundaries. Target journal requirements can guide adaptation when actual guidelines or relevant samples are available.

## Capabilities

- **Evidence-based review:** distinguish confirmed issues, optional polishing, style preferences, and claims requiring verification. Keep sound academic wording.
- **Preserve useful information:** account for every task, argument, condition, relation, and deliverable property. Improve syntax, reference, collocation, transitions, and paragraph organization without mechanical deletion or excessive compression.
- **Adapt across disciplines:** select checks for experimental research, quantitative social science, qualitative work, humanities, and reviews. Do not require models or experiments in every manuscript.
- **Adapt to a journal:** use verified requirements and comparable writing samples to learn rhetorical functions while preserving the author's voice.
- **Deliver usable text:** review only, revise directly, or provide exact source strings for Word with explicit edit boundaries and complete replacements.
- **Audit twice:** follow `Lock → Diagnose → Decide → Revise → Audit`, checking information and meaning before paragraph coherence and completeness.

The Chinese label “去 AI 化表述” refers here to observable writing problems. Common openers, semicolons, parallel structures, and multiple verbs are review clues, not errors by themselves. Rigor comes from evidence and preservation, not the number of edits, longer terminology, or shorter output.

## Install and use

Copy the entire [`paper-expression-editor/`](paper-expression-editor/) folder to your Codex skills directory, usually `~/.codex/skills/`, so the entry point is `~/.codex/skills/paper-expression-editor/SKILL.md`. You can also install that subdirectory with the skill installer. Start a new session if the skill does not appear.

```text
$paper-expression-editor Review and polish the discussion in my Chinese education paper using graduate-level rigor. This is an interview study. Preserve materials, direct quotations, and interpretation boundaries. Separate required corrections from optional polish and give complete replacement text.
```

```text
$paper-expression-editor Improve this engineering section. You may split sentences and reorganize paragraphs. Preserve all research tasks, experimental conditions, metrics, citations, and claim strength. Give exact source text and complete replacements in a table without mechanical shortening.
```

```text
$paper-expression-editor Polish my Chinese abstract using the target journal guide and two comparable excerpts I provide. State the requirements actually applied, preserve facts and voice, and do not invent findings or contributions.
```

For other AI tools, copy the [standalone Chinese prompt](01-直接使用的主提示词.md) with the manuscript. A filename or repository link does not establish that the AI has read all files; attach any additional guides needed or provide file access.

## Style and scope

- Public defaults use applicable requirements and semantic function. Preferences for fewer semicolons, headings without enumeration punctuation, or “作者等人” are opt-in, not imposed on all writers.
- Light polish stays local. Paragraph optimization can split, reorder, or combine genuinely redundant content. Minimal sufficient intervention does not mean shortest output or a fixed length ratio.
- The abstract, body, and conclusion may repeat a topic for different purposes. Judge redundancy by section function. Preserve planned, ongoing, and completed research states.
- Review only material actually seen. Identify missing evidence; separate content or claim changes for author confirmation.
- Better expression can support submission to strong Chinese journals. Innovation, methods, evidence, journal fit, and peer review still require actual assessment; there is no acceptance or detection guarantee.
- Follow applicable institutional, journal, and project requirements, including disclosure of AI assistance.

## Repository layout

```text
.
├── README.md
├── README_EN.md
├── LICENSE
├── 01-直接使用的主提示词.md
└── paper-expression-editor/
    ├── SKILL.md
    ├── references/
    │   ├── core-contract.md
    │   ├── review-checklist.md
    │   ├── revision-guide.md
    │   ├── meaning-audit.md
    │   ├── fact-check.md
    │   ├── discipline-and-genre.md
    │   ├── journal-adaptation.md
    │   ├── issue-taxonomy.md
    │   ├── output-formats.md
    │   └── style-profile.md
    └── examples/
        ├── sentence-cases.md
        ├── paragraph-cases.md
        ├── document-type-cases.md
        └── full-review-example.md
```

The entry point loads relevant guides as needed. Examples are instructional text, not independently verified research claims.

## License

This repository uses the MIT License; see [LICENSE](LICENSE).
