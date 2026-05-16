---
title: Quantization (양자화)
created: 2026-05-15
updated: 2026-05-15
tags: [llm/inference]
type: note
status: draft
source:
---

# Quantization (양자화)

## 한 줄 요약

언어모델에서 가중치와 활성화 함수의 정밀도를 낮춰 모델 크기를 줄이고 연산 속도를 높이는 기술. 연속적인 값을 이산적인 값으로 끊어버리는 것.

## 핵심 내용

보통 딥러닝 모델들은 데이터를 FP32(32비트 부동소수점 형식)로 저장함. 소수점 아래 아주 정밀한 부분까지 기록하지만 메모리를 많이 차지하고 연산 부하가 크다.

Quantization은 다음과 같은 형태로 변환한다:

- **FP32**: 학습 시 기본값, 가장 정확하지만 무거움
- **BF16**: FP32와 범위는 같고 정밀도만 낮춤, 학습에 많이 사용
- **INT8**: 추론 시 많이 사용, 품질 손실 거의 없음
- **INT4**: 로컬 실행의 대세, 약간의 품질 손실
- **INT2**: —

장점: 압도적인 공간 절약 (32비트에서 8비트로 줄이면 메모리 사용량 1/4), 속도 향상 (CPU/GPU에서 정수 연산이 소수점 연산보다 빠르고 전력 소모 적음).

### Trade-off

압축하면 손실이 발생:
- 성능 저하: 정밀도를 지나치게 낮추면 모델이 멍청해짐. 문맥을 놓치거나 논리적 오류 확률 높아짐.
- INT4 이하 모델부터는 [perplexity](perplexity.md)가 눈에 띄게 낮아짐.

## 관련 노트

- [perplexity](perplexity.md)
- [kv-cache](kv-cache.md)
- [gpu-computing](gpu-computing.md)
- [low-precision-training](low-precision-training.md)
- [fp32](fp32.md)
- [int8](int8.md)

## 참고

-
