---
title: Local Minima (로컬 미니마)
created: 2026-05-15
updated: 2026-05-15
tags: [llm/training, ml/optimization]
type: note
status: draft
source:
---

# Local Minima (로컬 미니마)

## 한 줄 요약

손실 함수([loss-function](loss-function.md))의 최적화 과정에서, 전체 최솟값(Global Minimum)은 아니지만 주변보다는 낮은 지점에 모델이 갇히는 현상.

## 핵심 내용

| 문제 | 설명 |
| :----- | ------------------------- |
| 학습 정체 | 손실 값이 더 이상 줄어들지 않아 학습이 멈춤 |
| 성능 한계 | 최적 성능에 도달하지 못한 채 수렴 |
| 일반화 실패 | 특정 데이터 패턴만 과적합됨 |

## 더 궁금한 포인트

- [saddle-point](saddle-point.md)(안장점)

## 관련 노트

- [loss-function](loss-function.md)
- [saddle-point](saddle-point.md)
- [gradient-descent](gradient-descent.md)
- [overfitting](overfitting.md)

## 참고

-
