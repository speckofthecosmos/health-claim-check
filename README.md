# health-claim-check

Published at https://github.com/speckofthecosmos/health-claim-check (MIT).

An agent skill that makes the assistant check its own causal and evidential claims before it says them in a health conversation: weighing a treatment, reading a study or a lab trend, preparing for an appointment, or drafting an appeal or prior-authorization letter. It runs seven questions (compared with what, in whom, which endpoint, mechanism or result, how big in absolute terms, who is claiming it, and would I say this if it cut against the user), and when a claim fails it states the weaker true claim instead of refusing or hedging. `references/fallacies.md` lists about 40 healthcare reasoning fallacies, each with the question that catches it.

It is patient-side and is not medical advice, a clinician tool, or a disclaimer generator.

## Install (Claude Code)

Copy the directory into your personal skills folder:

```sh
cp -r health-claim-check ~/.claude/skills/health-claim-check
```

or symlink it so updates follow the repo:

```sh
ln -s "$(pwd)/health-claim-check" ~/.claude/skills/health-claim-check
```

## Format

The skill uses the [Agent Skills](https://agentskills.io) format: a `SKILL.md` with YAML frontmatter (`name`, `description`) plus a `references/` folder loaded on demand. Any agent that reads that format can use it.

**Trigger tuning:** the description is deliberately broad (any conversation about health, medical care or coverage of care). If it fires on work that is not about a patient's care, such as claim-submission mechanics or payer-portal scripts, add an exclusion line to the description.

## License

The skill is released under the MIT License (see `LICENSE`), except for material adapted from CC BY 4.0 sources, which is included under the terms of [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

## Attribution

Changes were made to all borrowed material: it was paraphrased, rewritten for a patient-side conversation, and reorganised around the check questions.

Adapted under CC BY 4.0 ([license](https://creativecommons.org/licenses/by/4.0/)):

- **DrCatHicks/informed-patient** — the anti-confirmatory principle (alternatives stay on the table), "absence of evidence is a finding", and the citation-integrity rule. https://github.com/DrCatHicks/informed-patient
- **Informed Health Choices (IHC) Key Concepts** (Oxman et al., 2018; 2022 version) — claim labels and several catching questions, marked "(IHC)" in `references/fallacies.md`. https://zenodo.org/records/6611932 and https://pmc.ncbi.nlm.nih.gov/articles/PMC6290969/

Adapted from MIT-licensed sources ([MIT License](https://opensource.org/license/mit)); ideas paraphrased, no text copied:

- **aipoch/medical-research-skills** (`paper-to-claim-verifier`) — the list of forbidden evidence upgrades and the graded support scale. https://github.com/aipoch/medical-research-skills
- **K-Dense-AI/scientific-agent-skills** (`scientific-critical-thinking`) — the fallacy and bias roster, rewritten. https://github.com/K-Dense-AI/scientific-agent-skills
- **curiositech/some_claude_skills** (`clinical-diagnostic-reasoning`) — the "fresh eyes" reset question used for anchoring. https://github.com/curiositech/some_claude_skills

Concepts only, named and not copied: Croskerry's cognitive dispositions to respond; GRADE (indirectness, outcome importance); JAMA Users' Guides to the Medical Literature (surrogate validity); IPDAS (absolute-risk presentation); CASP checklists (CC BY-NC-SA 4.0, https://casp-uk.net). Linked only: Catalogue of Bias (https://catalogofbias.org) and the Ottawa Personal Decision Guide (https://decisionaid.ohri.ca/decguide.html).
