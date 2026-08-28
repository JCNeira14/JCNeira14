# GitHub Profile README Rework Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the outdated GitHub profile README with a concise, English, engineer-first Data Engineer profile grounded in Juan Cruz Neira's verified CV and public work.

**Architecture:** Keep the profile as one dependency-light `README.md` organized into identity, engineering focus, quantified impact, featured public work, core stack, and contact. Use native Markdown for structure and only two Shields.io contact badges so the page remains readable across GitHub themes and screen sizes.

**Tech Stack:** GitHub Flavored Markdown, minimal inline HTML for badges, Shields.io.

## Global Constraints

- Primary positioning: Data Engineer with 4+ years of experience at IBM building production Python and SQL systems for financial and banking operations.
- Language: natural professional English.
- Use only facts verified in the Data Engineer CV and canonical candidate profile.
- Preserve qualifiers such as `4+`, `approximately`, and explicit before-and-after values.
- Describe leadership as technical leadership, not formal people management.
- Do not include a banner, animation, photo, visitor counter, activity graph, streak card, GitHub statistics widget, or large wall of technology icons.
- Do not publish or push changes.

---

### Task 1: Rewrite the profile README

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: the approved design in `docs/superpowers/specs/2026-08-28-github-profile-readme-design.md` and the public `JCNeira14/pc-first-boot-assistant` repository.
- Produces: a self-contained GitHub profile page rendered from `README.md`.

- [x] **Step 1: Record the required and forbidden content checks**

Required terms:

```text
Data Engineer
4+ years
25 production pipelines and automations
technical leadership to 6 developers
approximately 100 to 200 daily transactions
PC First Boot Assistant
LangChain
LangGraph
AWS Bedrock
```

Forbidden legacy dependencies and claims:

```text
readme-typing-svg
github-readme-stats
streak-stats
activity-graph
komarev
people management
```

- [x] **Step 2: Replace the legacy README**

Write the agreed single-column structure in this exact order:

```text
Name and Data Engineer headline
Short professional introduction and contact badges
What I build
Impact
Featured project
Core stack
Connect
```

Use three bullets in `Impact`. Present `PC First Boot Assistant` as a personal, learning-focused project and link to `https://github.com/JCNeira14/pc-first-boot-assistant`.

- [x] **Step 3: Run content checks**

Run:

```bash
rg -n 'Data Engineer|4\+ years|25 production pipelines and automations|technical leadership to 6 developers|approximately 100 to 200 daily transactions|PC First Boot Assistant|LangChain|LangGraph|AWS Bedrock' README.md
rg -n 'readme-typing-svg|github-readme-stats|streak-stats|activity-graph|komarev|people management' README.md
```

Expected: every required term appears; the forbidden-content search returns no matches.

- [x] **Step 4: Check Markdown whitespace and review the diff**

Run:

```bash
git diff --check
git diff -- README.md
```

Expected: no whitespace errors, and the diff contains only the approved content replacement.

### Task 2: Verify links and final repository state

**Files:**
- Verify: `README.md`

**Interfaces:**
- Consumes: the completed `README.md` from Task 1.
- Produces: evidence that the README is link-complete, internally consistent, and ready for a local commit.

- [x] **Step 1: Extract every outbound URL**

Run a read-only parser that prints the URLs found in Markdown and HTML attributes:

```bash
python3 -c 'import pathlib,re; text=pathlib.Path("README.md").read_text(); print("\n".join(sorted(set(re.findall(r"https?://[^)\" ]+", text)))))'
```

Expected URLs: the LinkedIn profile, the public featured project, and the two Shields.io badge images. The email action uses `mailto:`.

- [x] **Step 2: Verify the featured project and social destinations**

Confirm these exact destinations:

```text
https://github.com/JCNeira14/pc-first-boot-assistant
https://www.linkedin.com/in/juancruzneira/
mailto:juancruzneira@gmail.com
```

Expected: the featured project is public, LinkedIn resolves to the intended profile even if it presents an authentication wall, and the mail link uses the existing CV address.

- [x] **Step 3: Perform the final claim audit**

Compare every number, employer reference, technology, and qualifier in `README.md` against the approved design and the canonical profile. Confirm that IBM work is described as professional experience and the featured project is explicitly described as personal and learning-focused.

- [x] **Step 4: Commit the README implementation**

Run:

```bash
git add README.md docs/superpowers/plans/2026-08-28-github-profile-readme.md
git commit -m "docs: rework GitHub profile README"
```

Expected: one local commit containing the new README and its implementation plan; nothing is pushed.
