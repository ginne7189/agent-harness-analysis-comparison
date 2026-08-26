# Hybrid Workflow

```text
OTA 변경 요청
→ Router: 단순 조회 또는 출시 검토 구분
→ 출시 검토이면 법규·보안·품질 Specialist를 병렬 검토 대상으로 선택
→ Contract: 주장·문서 ID·버전·위치·원문 누락 검사
→ Verifier: 허용 문서·최신 버전·답변과 근거 일치 검사
→ pass: 담당자용 검토안 작성
→ reject: 재조사 또는 사람 확인
```

## 사용한 패턴과 이유

| 패턴 | 사용 위치 | 해결하는 문제 |
| --- | --- | --- |
| Routing | 요청 입구 | 단순 조회와 출시 검토의 처리 범위가 다름 |
| Parallelization | 법규·보안·품질 검토 | 서로의 결과 없이 같은 변경안을 검토 가능 |
| Custom Workflow | 전체 실행 순서 | 검증과 승인 경계를 항상 같은 순서로 적용 |
| Verifier | Specialist 결과 뒤 | 출처·버전·근거 누락을 자동 완료 전에 차단 |
| Human Approval | 최종 단계 | AI가 출시 승인과 위험 수용을 대신하지 않음 |

Evaluator-Optimizer를 추가하려면 Verifier의 거절 이유를 해당 Specialist에 돌려보내 재조사하게 하고, 최대 재시도 횟수를 정합니다.
