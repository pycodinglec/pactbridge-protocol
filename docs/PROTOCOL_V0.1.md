# PactBridge Protocol v0.1 (Draft)

## EN

## 1) Scope
This protocol defines the minimum interaction standard between:
- **Delegating AI** (principal/requester agent)
- **Performing Human** (contractor/worker)
- **Platform/Coordinator** (optional intermediary)

## 2) Lifecycle (State Machine)

`draft -> submitted -> clarifying -> accepted -> in_progress -> evidence_submitted -> verified -> settled`

Alternative terminal states:
- `rejected`
- `cancelled`
- `disputed`
- `denied_by_policy`

## 3) Mandatory Task Fields
Any task MUST provide:
- Purpose and expected outcome
- Exact location scope
- Time window and deadline
- Allowed/prohibited actions
- Required evidence types
- Compensation and settlement terms
- Emergency contact and escalation route

## 4) Risk Assessment Contract
Risk assessment returns structured output only:
- `risk_level`: red|yellow|green
- `decision`: allow|allow_with_controls|deny|escalate
- `reason_codes`: enum list
- `required_controls`: enum list
- `confidence`: 0.0~1.0
- `policy_version`, `prompt_version`

## 5) Evidence Requirements
At least one verifiable evidence item is mandatory for completion:
- timestamped media (photo/video)
- location proof (when legally permitted)
- receipt/document hash
- signed acknowledgment (if applicable)

## 6) Safety Gates
- **Green**: automatic matching allowed
- **Yellow**: additional controls required
- **Red**: blocked and rerouted

## 7) Dispute Protocol (Minimal)
- open dispute within policy-defined window
- freeze settlement on dispute
- attach evidence bundles from both sides
- produce platform decision + reason codes

## 8) Audit Log Requirements
Each decision event should include:
- actor id
- timestamp
- action
- input hash
- decision hash
- policy/prompt versions

---

## KR

## 1) 범위
본 프로토콜은 다음 주체 간 최소 상호작용 규칙을 정의합니다.
- **위탁 AI** (요청자 에이전트)
- **수행 인간** (수탁자)
- **플랫폼/중개자** (선택)

## 2) 상태 전이
`draft -> submitted -> clarifying -> accepted -> in_progress -> evidence_submitted -> verified -> settled`

종료 상태(대안):
- `rejected`
- `cancelled`
- `disputed`
- `denied_by_policy`

## 3) 필수 명세
모든 작업에는 아래 항목이 반드시 포함되어야 합니다.
- 목적/완료 기준
- 정확한 위치 범위
- 수행 시간/마감
- 허용/금지 행동
- 증빙 방식
- 보상/정산 조건
- 비상 연락/에스컬레이션 경로

## 4) 위험판정 출력
위험판정은 반드시 구조화된 출력(JSON)으로 반환합니다.
- `risk_level`: red|yellow|green
- `decision`: allow|allow_with_controls|deny|escalate
- `reason_codes`
- `required_controls`
- `confidence`
- `policy_version`, `prompt_version`

## 5) 증빙
완료 처리에는 검증 가능한 증빙이 최소 1개 이상 필요합니다.
- 시간정보 포함 사진/영상
- 위치 증빙(법적으로 허용되는 범위)
- 영수증/문서 해시
- 서명 확인(필요 시)

## 6) 안전 게이트
- **Green**: 자동 매칭 가능
- **Yellow**: 추가 보호조치 후 진행
- **Red**: 차단 및 대체안 안내
