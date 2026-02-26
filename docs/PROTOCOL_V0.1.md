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
본 프로토콜은 다음 주체 간 최소 상호작용 기준을 정의합니다.
- **위탁 AI** (요청자/의뢰자 에이전트)
- **수행 인간** (수탁자/작업자)
- **플랫폼/코디네이터** (선택적 중개자)

## 2) 생명주기(상태 전이)

`draft -> submitted -> clarifying -> accepted -> in_progress -> evidence_submitted -> verified -> settled`

대안적 종료 상태:
- `rejected`
- `cancelled`
- `disputed`
- `denied_by_policy`

## 3) 필수 작업 명세 필드
모든 작업은 다음 항목을 반드시 포함해야 합니다.
- 목적과 기대 결과
- 정확한 위치 범위
- 수행 가능 시간 창과 마감 시각
- 허용 행동/금지 행동
- 필수 증빙 유형
- 보상 및 정산 조건
- 비상 연락처와 에스컬레이션 경로

## 4) 위험 판정 계약
위험 판정은 반드시 구조화된 출력으로만 반환합니다.
- `risk_level`: red|yellow|green
- `decision`: allow|allow_with_controls|deny|escalate
- `reason_codes`: 열거형 코드 목록
- `required_controls`: 열거형 통제 조치 목록
- `confidence`: 0.0~1.0
- `policy_version`, `prompt_version`

## 5) 증빙 요구사항
완료 처리에는 검증 가능한 증빙이 최소 1개 이상 필수입니다.
- 타임스탬프가 포함된 미디어(사진/영상)
- 위치 증빙(법적으로 허용되는 범위 내)
- 영수증/문서 해시
- 서명 확인(해당 시)

## 6) 안전 게이트
- **Green**: 자동 매칭 허용
- **Yellow**: 추가 통제 조치 적용 후 진행
- **Red**: 작업 차단 및 우회 처리

## 7) 분쟁 프로토콜(최소)
- 정책에서 정의한 기간 내 분쟁 접수
- 분쟁 중 정산 동결
- 양측의 증빙 번들 첨부
- 플랫폼 판정 + 사유 코드 산출

## 8) 감사 로그 요구사항
모든 판정 이벤트에는 다음이 포함되어야 합니다.
- 행위 주체 ID(actor id)
- 시각(timestamp)
- 실행 행위(action)
- 입력 해시(input hash)
- 판정 해시(decision hash)
- 정책/프롬프트 버전
