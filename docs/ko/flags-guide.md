# 플래그 가이드: 단순하게 유지하기

**중요**: SuperClaude의 자동 활성화 기능은 매우 잘 작동합니다! 대부분의 경우 수동으로 플래그를 설정할 필요가 없습니다. 시스템이 여러분의 요구에 따라 적절한 도구와 전략을 자동으로 선택합니다.

## 플래그를 사용할 때

플래그는 Claude에게 특정 지시를 내리는 것과 같습니다. 시스템이 보통 여러분의 요구를 이해하지만, 때로는 명확한 지시가 도움이 될 수 있습니다:

- 특정 동작을 원할 때 (예: "매우 상세한 분석이 필요해요")
- 자동 선택을 무시하고 싶을 때 (예: "이번엔 MCP 서버를 사용하지 마세요")
- 특정 성능 요구사항이 있을 때 (예: "간결하게 유지해주세요")

## 가장 유용한 플래그

### 계획과 분석
- `--plan` - 실행 전에 실행 계획 표시
- `--think` - 심층 분석 수행 (약 4K 토큰)
- `--think-hard` - 매우 심층적인 분석 수행 (약 10K 토큰)

### 효율성과 압축
- `--uc` / `--ultracompressed` - 더 간결한 응답 사용 (30-50% 토큰 절약)
- `--answer-only` - 답변만 제공하고 작업이나 워크플로우 생성하지 않음
- `--verbose` - 완전하고 상세한 설명 제공

### MCP 서버 제어
- `--no-mcp` - 모든 MCP 서버 비활성화 (40-60% 속도 향상)
- `--c7` - 문서 조회를 위해 Context7 활성화
- `--seq` - 복잡한 분석을 위해 Sequential 활성화
- `--magic` - UI 컴포넌트 생성을 위해 Magic 활성화

### 페르소나 활성화
- `--persona-frontend` - UI/UX 전문가 모드
- `--persona-backend` - 백엔드 및 API 전문가 모드
- `--persona-architect` - 시스템 아키텍처 전문가 모드
- `--persona-scribe=ko` - 한국어 전문 작성 모드

## 일반적인 패턴

### "빠른 답변을 원해요"
```
질문 --uc --answer-only
```

### "이 복잡한 문제를 깊이 분석해주세요"
```
/analyze 문제 --think-hard --seq
```

### "React 컴포넌트 만들기"
```
/build 컴포넌트명 --magic
```

### "외부 도구가 필요 없어요"
```
작업 --no-mcp --uc
```

## 기억하세요: 적을수록 좋습니다

SuperClaude의 자동 감지 기능은 보통 올바른 선택을 합니다. 플래그 없이 시작하고, 특정 동작이 필요할 때만 추가하세요.

**프로 팁**: 확실하지 않다면, 시스템이 자동으로 처리하도록 두세요. 정말 똑똑합니다! 🎯