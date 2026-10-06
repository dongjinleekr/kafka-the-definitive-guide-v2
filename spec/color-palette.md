# 시리즈 색상 페어

같은 형식으로 운영하는 도서 홍보 사이트들 (Kafka, Iceberg, 추후 추가될 책들) 의 accent color 페어 후보 모음.
각 사이트의 SCSS `$accent`와 `$accent-dark` 값을 책별로 다르게 적용하며, `$accent-dark`는 링크 hover·focus 색으로 사용한다.

## 페어 옵션 (Kafka × Iceberg)

| 번호 | Kafka | Hover | Iceberg | Hover | 톤 |
|---|---|---|---|---|---|
| 1 (적용) | Crimson Wine `#9F1239` | `#7F0E2E` | Glacier Teal `#0F766E` | `#0B5F59` | 와인 + 청록. 클래식, 차분한 무게감. 보색 가까운 대비. |
| 2 | Crimson Wine `#9F1239` | `#BE185D` | Ice Blue `#0284C7` | `#0EA5E9` | 와인 + 차가운 파랑. Kafka 무겁고 Iceberg 가볍게. 시각 비중 비대칭. |
| 3 | Warm Orange `#C2410C` | `#EA580C` | Glacier Teal `#0F766E` | `#14B8A6` | 주황 + 청록. 활기 + 차가움. 컨셉 직관 (흐름 vs 단단함). |
| 4 | Warm Orange `#C2410C` | `#EA580C` | Ice Blue `#0284C7` | `#0EA5E9` | 주황 + 차가운 파랑. 가장 전형적인 따뜻-차가움 보색. 다이내믹. |

## 적용 기록

- 2026-06-01: 페어 1 채택. Kafka `#9F1239` 즉시 적용. Iceberg `#0F766E` 는 사이트 셋업 후 적용 예정.
- 2026-08-05: 밝은 배경의 링크와 버튼에서 대비를 유지하도록 적용 페어의 hover 색상을 더 어두운 값으로 조정.

## 시리즈 확장용 색상 후보

다음 책이 추가될 때 위 색들과 가족이 너무 가깝지 않은 후보:

| 컬러 | 값 | Hover | 비고 |
|---|---|---|---|
| Indigo Purple | `#4F46E5` | `#6366F1` | 모던/디지털. 보라 계열은 시리즈 안에서 distinct. |
| Forest Green | `#15803D` | `#16A34A` | 진한 초록. Iceberg 청록과는 가족이라 같은 시리즈에는 비추. |
| Amber Gold | `#B45309` | `#D97706` | 따뜻한 황토. Warm Orange 와 가족이라 동시 사용 비추. |
| Slate Charcoal | `#475569` | `#64748B` | 회색 기반의 보수적 선택. 따뜻한 hover 강조 가능 (예: `#EA580C`). |

## 메모

- 모든 base color 는 WCAG AA (대비 4.5+) 통과 확인.
- 적용 페어의 hover 색은 밝은 배경에서 대비를 유지하도록 base 보다 어둡게 사용한다.
- 두 색 모두 진한 페어 (1, 3) 은 본문 link 가 시각적으로 강조됨. 본문이 답답하면 hover 색만 강조하고 base 를 한 단계 어둡게 조정.
