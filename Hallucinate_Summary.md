---
title: Hallucinate Summary
created: 2026-05-14
updated: 2026-05-17
tags:
  - llm/hallucination
  - summary
type: note
status: draft
source:
  - "[Why_Hallucinate](Why_Hallucinate.md)"
---
# 언어 모델들은 왜 환각[hallucination](hallucination.md)을 일으키는가?
---
#### 요약목적: 대규모언어모델들의 환각이 왜 발생하는지에 대해서 간단히 알아보기 위함.

언어 모델의 환각은 이진 분류의 오류에서 기원함.
환각이라 표현하지만 인간지각 경험과는 다르다.

## 벤치마크에 대한 모델 최적화로 인한 환각조장
사람도 종종 그럴듯해 보이는 정보를 조작함.
불확실 할 때 객관식 시험에서 추측하거나, 서술형 시험에서 자신감이 낮음에도 불구하고 그럴듯한 답안을 제출하는 것처럼 언어모델도 이와 유사한 테스트를 통해 평가된다. 두 문제형식 경우 불확실할 때 추측하는 것이 정답에는 1점을 부여하고 공백이나 모름에는 0점을 부여하는 이진 점수 체계로 기대 점수를 최적화하는데, bluff는 종종 과도한 자신감과 구체성을 가지게된다. 많은 [LLM](LLM.md) 벤치마크는 정확도나 통과율과 같은 이진 지표를 사용하여 표준화된 인간 시험을 반영함. (보상관련모델정보 [[CS229_Summary#[reward-model](reward-model.md)]])
