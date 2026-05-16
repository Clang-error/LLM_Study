---
title: Autoregressive Models
created: 2026-05-17
updated: 2026-05-17
tags: [llm/autoregressive, llm/generation]
type: note
status: draft
source:
---

# Autoregressive Models

## 한 줄 요약

자기회귀 모델의 기본 개념과 장단점 정리.

## 핵심 내용

- 이전 출력들을 기반으로 다음 토큰을 예측하는 생성 방식
- GPT시리즈, [LLaMA](LLaMA.md) 등 대부분의 [LLM](LLM.md)이 이 방식 사용
- 장점: 시퀀스 길이 무제한, 문맥 이해력 높음
- 단점: 병렬 생성 어려움, 추론 속도 느림

## 관련 노트

- [kv-cache](kv-cache.md)
- [self-attention](self-attention.md)
- [tokenization](tokenization.md)
- [transformer](transformer.md)

## 참고

- 
