# 비디오와 미디어

Video와 media workflow는 multi-step, multi-asset, expensive, continuity-sensitive하기 때문에
agentic structure가 특히 중요합니다.

## 공통 압력

- Story, shot composition, character continuity, audio, timing, style이 함께 정렬되어야 합니다.
- High-quality clip rendering은 비용이 큽니다.
- 작은 upstream change가 downstream asset을 무효화할 수 있습니다.
- Script, storyboard, keyframe, final render 단계마다 human approval이 필요할 수 있습니다.

## 유용한 패턴

- [크리에이티브 브리프 패킷 (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [생성-비평-개선 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [지속 세션 상태 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)
- [역할 계약 (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [도구 사용 계약 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)

## 후보 패턴

- Storyboard Gate.
- Asset Handoff.
- Continuity Ledger.
- Render Budget Gate.
- Provenance Ledger.
