# 이미지 생성

Image generation은 단일 prompt를 넘어 reference, style continuity, variation, critique,
selection, downstream design/media handoff가 필요할 때 agentic pattern의 도움을 받습니다.

## 공통 압력

- Loose prompt는 시각적으로 그럴듯하지만 misaligned image를 만들 수 있습니다.
- Reference와 style word가 서로 충돌할 수 있습니다.
- Human taste가 중심이므로 automatic scoring 뒤에 숨기면 안 됩니다.
- Iteration은 비용이 들고 original intent에서 drift할 수 있습니다.

## 유용한 패턴

- [크리에이티브 브리프 패킷 (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [생성-비평-개선 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [지속 세션 상태 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)
- [도구 사용 계약 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)

## 후보 패턴

- Reference Board.
- Style Lock.
- Variation Ladder.
- Provenance Ledger.
- Human Approval Gate.
