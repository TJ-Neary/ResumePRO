![ResumePRO](assets/social-preview.png)

![Showcase](https://img.shields.io/badge/type-showcase-purple?style=flat-square)
![Python](https://img.shields.io/badge/python-3.12+-blue?style=flat-square)
![Anthropic](https://img.shields.io/badge/LLM-Claude-orange?style=flat-square)
![Tests](https://img.shields.io/badge/tests-2%2C656%20passing-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red?style=flat-square)

# ResumePRO

**A comprehensive, AI-empowered career search ecosystem that builds genuine contextual understanding of a user's professional experience through conversational AI interviews, then produces precisely targeted, ATS-optimized resumes matched to specific job postings.**

This is not keyword insertion. ResumePRO conducts extensive AI-led interview sessions to construct a semantic model of a user's career history, then applies multi-framework job analysis and evidence-verified experience matching to generate resumes that authentically represent qualifications aligned with each role's requirements. Built for career transitions, including military-to-civilian, across 16 professional role families.

> **This is a showcase repository.** It demonstrates the system architecture, design decisions, and capabilities of a private project. Source code is not included. For technical inquiries, open an [issue](../../issues/new?template=inquiry.yml).

---

## Architecture Highlights

### 1. Two-Phase Strategic Resume Pipeline

The flagship capability: a two-phase LLM-driven pipeline that acts as a master career coach. **Phase A** (Strategy Development) analyzes the full experience library, job requirements, and role family profile to produce a reviewable positioning strategy: narrative arc, experience selection with rationale, per-section bullet directives, keyword distribution, and gap mitigation plans. **Phase B** (Targeted Bullet Writing) takes the approved strategy and writes custom bullets grounded in real STAR data, with a verification gate ensuring every claim traces to documented evidence. The mechanical pipeline (keyword-based scoring and pre-generated bullet selection) remains as an offline fallback.

### 2. Semantic Experience Understanding

The system goes beyond keyword matching by constructing a rich semantic representation of each experience. Embedding-based similarity scoring compares job requirements against verified professional experiences across six dimensions (keyword match, competency alignment, recency, metric strength, semantic similarity, and personalized assessment signals), while a grounding verification layer ensures every claim traces to documented evidence with explicit confidence levels (Verified, Calculated, Estimated).

### 3. Conversational STAR Interview Engine

A multi-turn interview orchestrator guides users through structured experience extraction using the STAR methodology (Situation, Task, Action, Result). The system manages interview phases, validates completeness, links evidence artifacts, and stores sessions with full conversation history. Each interview produces structured, reusable experience entries that feed the generation pipeline.

### 4. Multi-Framework Job Analysis

Job postings are analyzed through three complementary frameworks simultaneously: MoSCoW prioritization (Must/Should/Could/Won't requirements), the Iceberg Model (visible requirements vs. hidden organizational needs), and semantic clustering (grouping related requirements into competency themes). This layered analysis produces a nuanced understanding that drives both experience matching and content generation.

---

## Feature Overview

| Feature | Technical Approach | Business Value |
|---------|-------------------|----------------|
| **Strategic Resume Pipeline** | Two-phase LLM generation: positioning strategy then targeted bullet writing with grounding verification | Resumes read like they were written by a career strategist, not assembled by a keyword matcher |
| **AI-Led STAR Interviews** | Multi-turn LLM orchestration with phase management and evidence linking | Captures rich, verified experiences through natural conversation |
| **Semantic Experience Matching** | Embedding-based similarity with multi-dimensional scoring | Surfaces the most relevant experiences for each job posting |
| **Job Posting Analysis** | MoSCoW, Iceberg Model, and semantic clustering frameworks | Understands both explicit requirements and implicit expectations |
| **Evidence Verification** | Claim grounding against source documents with confidence labeling | Every metric traces to evidence: no fabricated numbers |
| **ATS Optimization** | Clean DOCX export with keyword-aware formatting | Resumes parse correctly through applicant tracking systems |
| **Cover Letter Generation** | LLM-powered with pain-point strategy engine | Aligned messaging across resume and cover letter |
| **Interview Preparation** | STAR story selection matched to likely interview questions | Consistent narrative from resume through interview |
| **Company Research** | Automated company profiling with culture and values analysis | Informed positioning for each application |
| **Human-in-the-Loop Editing** | Bullet swap, remove, reorder, undo history, draft versioning | Full control over generated content before export |
| **Assessment Integration** | Professional assessment data as a personalized scoring signal | Ranks experiences by alignment with individual strengths |
| **Data Standardization** | Automatic schema normalization across all experience entries | Consistent data quality regardless of input format |
| **16 Role Families** | Configurable role profiles with family-specific bullet libraries | Covers HR, PM, OD, L&D, Change Management, AI Transformation, and more |

---

## Screenshots

> *Screenshots and demo recordings coming soon.*
>
> Planned visuals: CLI job analysis output, generated resume sample, interview session flow, experience matching dashboard.

---

## By the Numbers

| Metric | Value |
|--------|-------|
| Passing Tests | 2,656 across 104 test files |
| Source Modules | 153 files across 25+ packages |
| CLI Commands | 31 (23 command groups + 8 standalone) |
| Role Families | 16 configurable career profiles |
| Experience Library | 36 verified STAR-format entries |
| Bullet Files | 42 role-family bullet libraries |
| Generated Bullets | ~2,474 role-specific resume bullets |
| Scoring Dimensions | 6 (keyword, competency, recency, metrics, semantic, assessment) |
| Prompt Templates | 18 YAML-based prompt templates |
| Development EPICs | 23 (233+ backlog items) |
| Resume Generation | Targeted resume in under 60 seconds |

---

## Technology Stack

| Layer | Technology | Role |
|-------|-----------|------|
| **Language** | Python 3.12+ | Core implementation |
| **LLM Provider** | Anthropic Claude (Sonnet/Opus) | Content generation, strategic positioning, analysis, interviews |
| **LLM Fallback** | Google Gemini | Alternative provider support |
| **CLI Framework** | Typer | Command-line interface |
| **Data Validation** | Pydantic v2 | Schema enforcement and serialization |
| **Embeddings** | sentence-transformers (all-MiniLM-L6-v2) | Semantic similarity computation |
| **Vector Storage** | SQLite | Embedding persistence and retrieval |
| **Document Export** | python-docx | ATS-optimized DOCX generation |
| **Prompt Management** | YAML templates with caching | Structured prompt loading and versioning |
| **Testing** | pytest | Unit, integration, and regression testing |
| **NLP** | spaCy, NLTK | Text processing and entity extraction |

---

## System Design

For the complete architecture including C4 diagrams, data flow, and design decision rationale:

**[View Full Architecture Documentation](ARCHITECTURE.md)**

---

## About

ResumePRO was designed to solve a real problem: career transitions require deeply personalized resumes that authentically represent transferable experience. Traditional resume tools rely on keyword stuffing or generic templates. ResumePRO takes a fundamentally different approach by first understanding the user's experience through structured interviews, then applying that understanding to each specific job opportunity.

The two-phase strategic pipeline represents the evolution from mechanical resume assembly to genuine career coaching: the system develops a positioning strategy that reads between the lines of job postings, then writes custom content grounded in verified experience data.

---

Copyright 2026 TJ Neary. All Rights Reserved.
