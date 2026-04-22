# mAb Stability Causal Network (v4d, GPT-5-mini)

mAb 안정성 인과관계 네트워크 시각화 — GPT-5-mini로 추출한 신규 버전.

## 배경

기존 버전은 GPT-4o-mini로 추출한 데이터(v4c)를 사용했으나, 추출 품질 개선을 위해 GPT-5-mini로 전체 파이프라인을 재실행한 결과(v4d)를 이 레포에 배포합니다.

## 파일

| 파일 | 설명 |
|------|------|
| `index.html` | D3.js 기반 인터랙티브 네트워크 시각화 |
| `step2c_v4d_causal_edges_summary.csv` | GPT-5-mini 추출 엣지 데이터 (frequency ≥ 2 필터) |

## 데이터 통계

- 노드 수: 962
- 엣지 수: 2,436
- 관계 유형: 22개
- 노드 카테고리: 6개 (sequence, structure, formulation, stress, stability, quality_outcome)

## 파이프라인

1. Step 1: PubMed 논문 수집 (62,300편)
2. Step 2: Relevance Filtering (GPT-5-mini, 9.0% 통과)
3. Step 3: Causal Relation Extraction (GPT-5-mini, 39,792건 raw → 32,939 unique edges)
4. Step 4: mAb-GATED 모델 학습 및 평가

## 이전 버전

- v4c (GPT-4o-mini): https://sdkparkforbi.github.io/mab-causal-network/
