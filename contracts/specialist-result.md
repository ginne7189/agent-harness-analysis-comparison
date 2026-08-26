# Specialist Result Contract

모든 Specialist는 다음 값을 전달합니다.

- `role`: 결과를 만든 역할
- `claim`: 확인한 내용
- `document_id`: 사용한 문서 ID
- `version`: 사용한 문서 버전
- `location`: 페이지 또는 절
- `evidence`: 주장을 직접 뒷받침하는 원문
- `missing`: 확인하지 못한 값
- `conflicts`: 다른 자료와 충돌한 내용

필수 값이 비어 있으면 Verifier로 넘기지 않고 해당 역할의 결과를 `incomplete`로 끝냅니다.
