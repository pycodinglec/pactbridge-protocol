# PactBridge Protocol

**A Research Standard for Contracts between Delegating AI and Performing Humans**  
**위탁자 AI와 수탁자 인간의 계약을 위한 표준안 연구**

Author: **KYUHO LEE (pycodinglec)**

---

## EN (Primary)

PactBridge Protocol is an open research initiative that proposes a **minimum viable contract protocol** for AI-to-human task delegation in physical or semi-physical workflows.

This repository does **not** provide legal advice. It provides:
- A standard task specification schema
- A structured safety/risk assessment schema (Red/Yellow/Green)
- Execution evidence and audit-log design
- A jurisdiction adapter concept for country-specific compliance

### Why this project exists

Current “AI hires human” marketplaces are directionally interesting but often weak in trust primitives (identity, evidence, dispute resolution, accountability). PactBridge focuses on protocol-level interoperability and safety consistency before scaling marketplaces.

### Core principles

1. **Spec First, Risk Next**: force complete task description before risk labeling.
2. **Structured Decisions**: machine-readable decisions with reason codes.
3. **Human-side Safety by Design**: prioritize worker protection and informed consent.
4. **Jurisdiction-aware Extension**: keep a global core, adapt locally by policy packs.
5. **Auditability**: every decision must be explainable and reviewable.

### Repository map

- `docs/PROTOCOL_V0.1.md` — protocol draft (EN/KR)
- `docs/ETHICS_AND_LIMITS.md` — ethics, misuse boundaries, and non-goals
- `docs/JURISDICTION_ADAPTER.md` — legal variance adapter model
- `schemas/task_spec.schema.json` — required task input schema
- `schemas/risk_assessment.schema.json` — structured safety decision schema
- `prompts/safety-counsel.system.md` — system prompt template for consistent R/Y/G judgment
- `examples/` — sample requests and outputs

### Suggested use

- Research documentation
- Internal policy prototyping
- Simulation and benchmark setup for agent-to-human delegation systems

### Non-goals

- Replacing licensed legal counsel
- Enabling illegal, exploitative, or coercive work
- High-risk autonomous deployment without human oversight

---

## KR (요약)

PactBridge Protocol은 **AI가 인간에게 업무를 위탁하는 상황**을 위한 최소 표준안을 연구하는 공개 저장소입니다.

이 프로젝트는 법률 자문이 아니며, 아래를 제공합니다.
- 작업 명세 표준(JSON Schema)
- 구조화된 위험판정 표준(Red/Yellow/Green)
- 증빙/감사 로그 설계
- 국가별 규제 차이를 반영하는 어댑터 구조

핵심은 “플랫폼 확장”보다 먼저, **신뢰 가능한 거래 문법을 만드는 것**입니다.

---

## License

MIT License (see `LICENSE`)
