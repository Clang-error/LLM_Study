---
title: Pre-training
created: 2026-05-15
updated: 2026-05-15
tags: [llm/training, llm/fundamentals]
type: note
status: draft
source:
---

# Pre-training

Pre-training은 **'범용적인 텍스트 예측 기계'를 만드는 과정이다. 이 무식할 정도로 거대한 데이터 학습을 통해 형성된 'Representational Power(표현력)'가 이후 진행될 [supervised-fine-tuning](supervised-fine-tuning.md)(SFT)나 [rlhf](rlhf.md)(RLHF)의 근간이 된다.

## 한 줄 요약

거대 데이터셋으로 언어모델의 기본 표현력을 학습하는 과정. 이후 모든 파인튜닝의 기반이 됨.

## 핵심 내용

- **목표**: 범용 텍스트 예측 기계 만들기
- **핵심 산물**: Representational Power (표현력)
- **다음 단계**: [supervised-fine-tuning](supervised-fine-tuning.md) (SFT), [rlhf](rlhf.md) (RLHF)
- **학습 방식**: [autoregressive](autoregressive.md) 다음 토큰 예측
- **데이터**: [training-data](training-data.md)

## 관련 노트

- [CS229_Summary](CS229_Summary.md)
- [MOC-llm](MOC-llm.md)
- [self-attention](self-attention.md)
- [scaling-laws](scaling-laws.md)
- [tokenization](tokenization.md)
- [cross-entropy](cross-entropy.md)

## 참고
