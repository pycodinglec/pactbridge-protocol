# PactBridge Protocol (한국어)

**위탁자 AI와 수탁자 인간의 계약을 위한 표준안 연구**  
작성자: **KYUHO LEE (pycodinglec)**

원문(영문): [`README.md`](./README.md)

---

## “PactBridge” 이름의 의미

- **Pact**: 당사자 간의 명확하고 책임 가능한 합의
- **Bridge**: 서로 다른 주체와 제약을 연결하는 운영적 다리

이 프로토콜은 다음 간극을 연결하도록 설계되었습니다.
1. AI의 위탁 의도와 인간의 실제 수행
2. 글로벌 공통 표준과 지역별 법·규정 차이
3. 작업 요청과 검증 가능한 완료 결과

즉 **PactBridge**는 “명시적 합의, 안전성, 추적 가능성 위에 놓인 연결 다리”를 뜻합니다.

---

## 프로젝트 소개

PactBridge Protocol은 물리적 또는 준물리적 업무 맥락에서, **AI가 인간에게 업무를 위탁할 때 적용할 최소 실행 가능 계약 프로토콜(Minimum Viable Contract Protocol)**을 제안하는 공개 연구 프로젝트입니다.

본 저장소는 **법률 자문을 제공하지 않으며**, 아래 산출물을 제공합니다.
- 작업 명세 표준 스키마(JSON Schema)
- 구조화된 안전/위험 판정 스키마(Red/Yellow/Green)
- 수행 증빙 및 감사 로그 설계
- 국가/지역별 준수를 위한 관할 어댑터 개념

---

## 왜 이 프로젝트가 필요한가

현재의 “AI가 인간에게 일을 맡기는” 형태의 서비스들은 방향성은 유의미하지만, 신뢰의 핵심 요소(신원, 증빙, 분쟁 처리, 책임성)가 약한 경우가 많습니다.

PactBridge는 마켓플레이스 확장 이전에, **프로토콜 수준의 상호운용성**과 **안전 판정 일관성**을 먼저 확보하는 데 초점을 둡니다.

---

## 핵심 원칙

1. **명세 우선, 위험 판정 후행 (Spec First, Risk Next)**  
   위험 등급 부여 전에 작업 설명을 완전하게 강제합니다.

2. **구조화된 의사결정 (Structured Decisions)**  
   사유 코드가 포함된 기계 판독 가능한 판정만 허용합니다.

3. **인간 수행자 안전 중심 설계 (Human-side Safety by Design)**  
   수행자 보호와 충분한 사전 동의를 최우선으로 둡니다.

4. **관할 인지형 확장 (Jurisdiction-aware Extension)**  
   글로벌 코어를 유지하되, 로컬 정책 팩으로 지역별 차이를 반영합니다.

5. **감사 가능성 (Auditability)**  
   모든 판정은 설명 가능하고 사후 검토 가능해야 합니다.

---

## 저장소 구성

- `docs/PROTOCOL_V0.1.md` — 프로토콜 초안 (EN/KR)
- `docs/ETHICS_AND_LIMITS.md` — 윤리 원칙, 오용 금지 경계, 비목표 (EN/KR)
- `docs/JURISDICTION_ADAPTER.md` — 관할별 법·정책 차이 대응 모델 (EN/KR)
- `schemas/task_spec.schema.json` — 필수 작업 입력 스키마
- `schemas/risk_assessment.schema.json` — 구조화된 안전 판정 출력 스키마
- `prompts/safety-counsel.system.md` — 일관된 R/Y/G 판정을 위한 시스템 프롬프트 템플릿 (EN/KR)
- `examples/` — 요청/응답 예시

---

## 권장 사용처

- 연구 문서화
- 내부 정책 프로토타이핑
- 에이전트-인간 위탁 시스템 시뮬레이션 및 벤치마크 설계

---

## 비목표 (Non-goals)

- 자격 있는 법률 전문가를 대체하는 것
- 불법·착취·강압적 업무를 가능하게 하는 것
- 인간 감독 없이 고위험 자율 배치를 수행하는 것

---

## 라이선스

MIT License (see `LICENSE`)
