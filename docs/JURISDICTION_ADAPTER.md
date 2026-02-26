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

---

## KR

2계층 구조를 권장합니다.

1. **글로벌 코어 프로토콜**
   - 공통 필드/상태전이/증빙 포맷
2. **로컬 정책 팩**
   - 지역별 금지/의무 규정 반영

요청에는 반드시 아래를 포함합니다.
- `jurisdiction_code` (예: KR-SEOUL)
- `policy_pack_version`

정책 팩은 다음을 오버라이드할 수 있습니다.
- 금지 업무군
- 신원확인 수준
- 필수 고지사항
- 정산/분쟁 처리 기한
