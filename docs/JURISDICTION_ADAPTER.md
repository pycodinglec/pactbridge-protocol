# Jurisdiction Adapter Model

## EN

Use a two-layer model:

1. **Global Core Protocol**
   - universal fields, state transitions, evidence envelope
2. **Local Policy Pack**
   - region-specific restrictions and obligations

Each request should carry:
- `jurisdiction_code` (e.g., KR-SEOUL)
- `policy_pack_version`

Policy packs can override:
- prohibited task classes
- identity verification level
- mandatory disclosures
- settlement/dispute timing

### Practical recommendation
Start with a narrow set of low-risk task classes and expand only after collecting sufficient evidence of safe operations and dispute handling quality.

---

## KR

2계층 구조를 권장합니다.

1. **글로벌 코어 프로토콜**
   - 공통 필드, 상태 전이, 증빙 봉투(evidence envelope)
2. **로컬 정책 팩**
   - 지역별 금지/의무 규정

각 요청에는 다음 필드를 포함해야 합니다.
- `jurisdiction_code` (예: KR-SEOUL)
- `policy_pack_version`

정책 팩은 다음 항목을 오버라이드할 수 있습니다.
- 금지 업무군
- 신원확인 수준
- 필수 고지사항
- 정산/분쟁 처리 시점

### 실무 권고
초기에는 저위험 업무군만 제한적으로 운영하고, 안전 운영 증빙과 분쟁 처리 품질 데이터가 축적된 뒤 범위를 단계적으로 확장하는 것이 바람직합니다.
