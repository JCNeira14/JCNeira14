# GitHub Profile README Rework - Design

Date: 2026-08-28

## Objective

Rework Juan Cruz Neira's GitHub profile README into an English, engineer-first profile that supports Data Engineer job searches. The first screen should communicate what Juan builds, the systems and technologies he works with, and verified evidence of professional impact.

## Audience and positioning

- Primary audience: recruiters and hiring managers evaluating Data Engineer candidates.
- Secondary audience: engineers reviewing Juan's technical interests and public work.
- Primary positioning: Data Engineer with 4+ years of experience at IBM building production Python and SQL systems for financial and banking operations.
- Supporting themes: ETL and data pipelines, data quality, backend APIs, enterprise integrations, fault tolerance, technical leadership, and applied AI.
- Language: natural professional English.

## Research direction

The design takes inspiration from the concise, purpose-led GitHub profiles of Charlie Marsh and Simon Willison. It adopts their emphasis on a clear identity, current technical focus, proof through work, and direct contact paths. It does not copy their wording or automated content.

## Content architecture

The README will use this order:

1. Name and role headline: `Data Engineer | Python · SQL · ETL`.
2. Two- or three-sentence introduction covering 4+ years at IBM, production data systems, and the financial and banking context.
3. `What I build`, with concise bullets for:
   - Python and SQL ETL/data pipelines;
   - data-quality validation and fault-tolerant enterprise integrations;
   - FastAPI backend services and relational data workflows;
   - Document Intelligence workflows using AWS Bedrock.
4. `Impact`, with exactly three verified proof points:
   - ownership of 25 production pipelines and automations;
   - technical leadership for 6 developers across 4 concurrent projects;
   - a 100% increase in invoice-processing capacity, from approximately 100 to 200 daily transactions.
5. `Featured project`, centered on `PC First Boot Assistant`:
   - identify it as a personal, learning-focused project;
   - state the problem it solves;
   - highlight Python, LangChain, LangGraph, stateful RAG, deterministic safety gates, human-in-the-loop controls, and offline tests;
   - link directly to the public repository.
6. `Core stack`, grouped by capability rather than shown as an undifferentiated logo wall:
   - Data: Python, SQL, Pandas, ETL, data modeling, data quality;
   - Backend: FastAPI, Pydantic, REST APIs, Alembic/ORM;
   - AI and delivery: AWS Bedrock, Document Intelligence, Docker, Kubernetes, CI/CD, GitHub Actions, Git.
7. `Connect`, with LinkedIn and the email address already present in the current README and CV.

## Visual design

- Left-aligned, single-column layout.
- Native Markdown for the main structure and content.
- A small number of Shields.io badges may be used for contact and the most important stack items.
- Compatible with GitHub light and dark themes.
- No banner, animated typing effect, synthetic or altered photo, visitor counter, activity graph, streak card, or GitHub statistics widget.
- No large wall of technology icons.
- Short sections, visible hierarchy, and mobile-friendly line lengths.

## Content constraints

- Use only facts verified in the Data Engineer CV and canonical candidate profile.
- Preserve qualifiers such as `4+`, `approximately`, and explicit before-and-after values.
- Describe leadership as technical leadership, not formal people management.
- Do not present all automation experience as exclusively Data Engineering or AI experience.
- Do not reproduce the full CV or list private employer projects as if their source code were public.
- Do not include GPA, age, phone number, compensation, relocation assumptions, or unconfirmed technologies.
- Clearly distinguish the featured personal project from production work at IBM.

## Verification

Before delivery:

- inspect the Markdown source for clarity, grammar, and unsupported claims;
- verify the LinkedIn, email, and featured-project links;
- confirm the featured repository is public;
- inspect the rendered README on GitHub-compatible Markdown or the live profile after publication is separately authorized;
- ensure there are no broken image dependencies or obsolete widget URLs;
- review the final diff to confirm only intended files changed.

## Out of scope

- Changing GitHub profile metadata, pinned repositories, repository visibility, or LinkedIn content.
- Publishing or pushing the README without explicit authorization.
- Creating a portfolio website, new project, banner, or profile photo.
