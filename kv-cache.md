---
title: KV-cache 정리
created: 2026-05-14
updated: 2026-05-14
tags: [llm/inference]
type: note
status: published
---

KV cache가 정확히 뭔지 정리해두자

추론할 때 [self-attention](self-attention.md) 계산에서 이전 토큰들의 Key/Value를 매번 다시 계산하는 건 비효율적임.
한 번 계산한 K, V를 메모리에 저장해두고 새 토큰만 추가하는 방식.

- 메모리: 토큰 수에 비례해서 늘어남 (context length 길수록 큼)
- 속도: 매번 O(n^2) → O(n) 으로 줄어듦
- 한계: 메모리 압박이 본격 병목. 그래서 [sliding-window-attention](sliding-window-attention.md), [paged-attention](paged-attention.md) 같은 기법들 나옴

관련: [self-attention](self-attention.md) [sliding-window-attention](sliding-window-attention.md) [inference](inference.md)
