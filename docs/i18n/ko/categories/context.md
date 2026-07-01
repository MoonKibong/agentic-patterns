# 컨텍스트 패턴

Context pattern은 agentic work에 필요한 정보를 packaging, reduction, preservation, handoff하는
방법을 정의합니다.

에이전트가 올바르게 행동하려면 충분한 정보가 필요하지만, 파일/히스토리/로그/chat 전체를
그대로 넣으면 중요한 signal이 묻힐 수 있습니다.

## 현재 패턴

- [컨텍스트 패킷 (Context Packet)](../../../../patterns/context/context-packet.md): planning, execution, review, handoff 전에 bounded task context를 제공합니다.
- [크리에이티브 브리프 패킷 (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md): creative intent, constraint, reference, deliverable, evaluation criteria를 묶습니다.

## 패턴 아이디어

- Handoff Summary.
- Constraint Header.
- Evidence Bundle.
- Resume Capsule.

## 관련 카테고리

- [프롬프트 패턴](prompt.md)
- [메모리 패턴](memory.md)
