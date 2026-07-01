# 디자인 생성

Design generation은 product design, interface concept, design-to-code, visual system, layout
exploration, asset handoff를 포함합니다.

## 공통 압력

- Design output은 aesthetics, usability, brand, constraint, implementation cost를 균형 있게 다뤄야 합니다.
- Agent는 아름답지만 구현하거나 유지하기 어려운 artifact를 생성할 수 있습니다.
- Design-to-code는 visual intent와 technical execution 사이의 엄격한 handoff가 필요합니다.
- 비용이 큰 downstream implementation 전에 human review가 필요합니다.

## 유용한 패턴

- [크리에이티브 브리프 패킷 (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [생성-비평-개선 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [도구 사용 계약 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [지속 세션 상태 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## 후보 패턴

- Design Constraint Packet.
- Artifact Handoff.
- Implementation Feasibility Review.
- Variation Ladder.
- Human Approval Gate.
