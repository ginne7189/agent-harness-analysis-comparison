# Analysis Comparison Workflow

1. 의사결정 질문과 비교 목적을 한 문장으로 정합니다.
2. 비교 대상, 기준, 측정 방법, 가중치, 제외 범위를 먼저 정합니다.
3. Orchestrator가 이번 요청에 필요한 분석 역할을 선택합니다.
4. 각 역할이 근거, 수치, 위험을 독립적으로 분석합니다.
5. 모든 결과를 Comparison Contract로 정규화합니다.
6. Manager·Comparator가 같은 기준으로 차이, 장점, 단점, 불확실성을 비교합니다.
7. Evaluator가 기준 누락, 근거 없는 점수, 모순, 과도한 추천을 검사합니다.
8. 실패하면 최대 2회 수정하고, 그래도 실패하면 사람 검토로 끝냅니다.

## 실패와 종료

- 비교 질문이나 대상이 불명확: 분석 전 질문
- 기준이 합의되지 않음: `criteria_review`
- 핵심 데이터 없음: `insufficient_data`
- 평가 통과: `analysis_ready`
- 최종 선택·구매·투자·인사 결정 요청: `human_decision`
