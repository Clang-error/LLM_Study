---
title: Self-Attention
created: 2026-05-15
updated: 2026-05-15
tags: [llm/architecture, llm/transformer]
type: note
status: draft
source:
---

# [self-attention](self-attention.md)

데이터 간의 관계도를 그리는 메커니즘으로
문장내에서 각 단어가 서로 어떤 관련이 있는지 스스로 계산하여
가중치를 부여하는 핵심 알고리즘이다.

## 한 줄 요약

[transformer](transformer.md)의 핵심. 토큰 간 관계를 거리와 무관하게 직접 계산하는 메커니즘.

## 세가지 핵심 벡터

- **Query (Q)**: "나는 무엇을 찾고 있는가?"
- **Key (K)**: "나는 무엇에 대한 정보를 갖고 있는가?"
- **Value (V)**: "실제로 전달할 내용은 무엇인가?"

## 동작 과정

**1. 선형 변환으로 Q, K, V 생성** 입력 토큰 벡터 X에 학습된 가중치 행렬(Wq, Wk, Wv)을 곱해 세 가지 벡터를 만듭니다.

**2. Scaled Dot-Product로 점수 계산** Query와 모든 Key를 내적한 후 `√d_k`로 나눕니다. `√d_k`로 나누는 이유는 차원이 커질수록 dot product 값이 폭발적으로 커지기 때문에 [gradient](gradient.md)를 안정시키기 위함입니다.

**3. [softmax](softmax.md) → Attention 가중치** 점수를 softmax에 통과시켜 합이 1인 확률 분포로 변환합니다. 이 값이 "어느 토큰을 얼마나 참고할지"를 결정합니다.

**4. Value의 가중합산** 가중치에 따라 각 Value 벡터를 합산해 **문맥이 담긴 새로운 표현 벡터**를 생성합니다.

---

**Self-Attention이 강력한 이유**는 토큰 간 거리에 상관없이 모든 쌍의 관계를 한 번에 계산하기 때문입니다. "나는 고양이가 매우 좋아요"에서 "좋아요"는 바로 옆 "매우"뿐 아니라 멀리 있는 "고양이가"와의 관계도 직접 학습할 수 있죠. 여기에 [multi-head-attention](multi-head-attention.md)(여러 개의 attention을 병렬로)과 [layer-normalization](layer-normalization.md), [feed-forward-network](feed-forward-network.md)가 쌓여 트랜스포머가 완성됩니다.

## 관련 노트

- [MOC-llm](MOC-llm.md)
- [kv-cache](kv-cache.md)
- [rope-reread](rope-reread.md)
- [pre-training](pre-training.md)
- [induction-head](induction-head.md)
- [CS229_Summary](CS229_Summary.md)
- [positional-encoding](positional-encoding.md)
- [attention-mechanism](attention-mechanism.md)

## 참고
