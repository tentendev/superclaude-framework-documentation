# SuperClaude 명령어 가이드 🛠️

## 💡 너무 생각하지 마세요 - SuperClaude가 도와드립니다

**이 17개 명령어에 대한 진실**: 기억할 필요가 없습니다. `/sc:analyze`나 `/sc:implement`부터 시작해서 무슨 일이 일어나는지 보세요!

**보통 작동하는 방식:**
- Claude Code에서 `/` 입력 → 사용 가능한 명령어들 확인
- `/sc:analyze`, `/sc:build`, `/sc:improve` 같은 기본 명령어들 사용
- **SuperClaude가 각 상황에 유용한 도구와 전문가를 선택하려고 노력합니다**
- 익숙해질수록 더 많은 명령어들이 유용해집니다

**자동 활성화가 꽤 멋집니다** 🪄 - SuperClaude는 당신이 무엇을 하려고 하는지 감지하고 당신이 관리할 필요 없이 관련 전문가들(보안 전문가, 성능 최적화기 등)을 활성화하려고 시도합니다. 보통 잘 작동합니다! 😊

---

## "먼저 이것들을 시도해보세요" 빠른 목록 🚀

**여기서 시작하세요** (읽을 필요 없음):
```bash
/sc:index                    # 사용 가능한 것들 확인
/sc:analyze src/            # 당신의 코드를 스마트하게 분석해봅니다
/sc:workflow feature-100-prd.md  # PRD에서 단계별 구현 워크플로우 생성
/sc:implement user-auth     # 기능과 컴포넌트 생성 (v2 /build 대체)
/sc:build                   # 스마트 프로젝트 빌드를 시도합니다
/sc:improve messy-file.js   # 코드를 정리해봅니다
/sc:troubleshoot "error"    # 문제 해결을 도와봅니다
```

**이것만으로도 정말 시작하기에 충분합니다.** 아래의 모든 것들은 사용 가능한 다른 도구들이 궁금할 때를 위한 것입니다. 🛠️

---

모든 16개 SuperClaude 슬래시 명령어의 실용 가이드. 무엇이 잘 작동하고 무엇이 아직 거친 상태인지 솔직하게 말씀드리겠습니다.

## 빠른 참조 📋

*(이것을 기억할 필요는 없습니다 - 유용해 보이는 것을 선택하기만 하세요)*

| 명령어 | 목적 | 자동 활성화 | 최적 용도 |
|---------|---------|-----------------|----------|
| `/sc:analyze` | 스마트 코드 분석 | 보안/성능 전문가 | 문제 찾기, 코드베이스 이해 |
| `/sc:build` | 지능형 빌드 | 프론트엔드/백엔드 전문가 | 컴파일, 번들링, 배포 준비 |
| `/sc:implement` | 기능 구현 | 도메인별 전문가 | 기능, 컴포넌트, API, 서비스 생성 |
| `/sc:improve` | 자동 코드 정리 | 품질 전문가 | 리팩토링, 최적화, 품질 수정 |
| `/sc:troubleshoot` | 문제 조사 | 디버그 전문가 | 디버깅, 문제 조사 |
| `/sc:test` | 스마트 테스트 | QA 전문가 | 테스트 실행, 커버리지 분석 |
| `/sc:document` | 자동 문서화 | 작성 전문가 | README 파일, 코드 주석, 가이드 |
| `/sc:git` | 향상된 git 워크플로우 | DevOps 전문가 | 스마트 커밋, 브랜치 관리 |
| `/sc:design` | 시스템 설계 도움 | 아키텍처 전문가 | 아키텍처 계획, API 설계 |
| `/sc:explain` | 학습 어시스턴트 | 교육 전문가 | 개념 학습, 코드 이해 |
| `/sc:cleanup` | 부채 감소 | 리팩토링 전문가 | 데드 코드 제거, 파일 정리 |
| `/sc:load` | 컨텍스트 이해 | 분석 전문가 | 프로젝트 분석, 코드베이스 이해 |
| `/sc:estimate` | 스마트 추정 | 계획 전문가 | 시간/노력 계획, 복잡성 분석 |
| `/sc:spawn` | 복잡한 워크플로우 | 오케스트레이션 시스템 | 다단계 작업, 워크플로우 자동화 |
| `/sc:task` | 프로젝트 관리 | 계획 시스템 | 장기 기능 계획, 작업 추적 |
| `/sc:workflow` | 구현 계획 | 워크플로우 시스템 | PRD에서 단계별 워크플로우 생성 |
| `/sc:index` | 명령어 탐색 | 도움말 시스템 | 작업에 적합한 명령어 찾기 |

**프로 팁**: 유용해 보이는 것들을 시도해보기만 하세요. SuperClaude는 보통 각 상황에 도움이 되는 전문가와 도구들을 활성화하려고 노력합니다! 🎯

## 개발 명령어 🔨

### `/workflow` - 구현 워크플로우 생성기 🗺️
**기능**: PRD와 기능 요구사항을 분석하여 포괄적인 단계별 구현 워크플로우를 생성합니다.

**도움이 되는 부분**: 당신의 PRD를 받아서 전문가 가이드, 의존성 매핑, 작업 오케스트레이션이 포함된 구조화된 구현 계획으로 분해합니다! 🎯

**언제 사용하나요**:
- PRD나 명세에서 새 기능 시작
- 명확한 구현 로드맵이 필요
- 구현 전략에 대한 전문가 가이드를 원함
- 여러 의존성이 있는 복잡한 기능 계획

**마법**: 당신의 기능 요구사항에 기반해 적절한 전문가 페르소나(아키텍트, 보안, 프론트엔드, 백엔드)와 MCP 서버(패턴을 위한 Context7, 복잡한 분석을 위한 Sequential)를 자동 활성화합니다.

**예시**:
```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "user authentication system" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**얻을 수 있는 것**:
- **로드맵 형식**: 타임라인이 포함된 단계별 구현 계획
- **작업 형식**: 정리된 에픽, 스토리, 실행 가능한 작업들
- **상세 형식**: 시간 추정이 포함된 단계별 지침
- **위험 평가**: 잠재적 문제와 완화 전략
- **의존성 매핑**: 내부 및 외부 의존성
- **전문가 가이드**: 도메인별 모범 사례와 패턴

### `/implement` - 기능 구현
**기능**: 지능적인 전문가 활성화로 기능, 컴포넌트, 기능을 구현합니다.

**도움이 되는 부분**: SuperClaude가 당신이 구현하고 있는 내용에 기반해 올바른 전문가(프론트엔드, 백엔드, 보안)와 도구들을 자동 활성화합니다! 🎯

**언제 사용하나요**:
- 새 기능이나 컴포넌트 생성 (v2의 `/build` 기능 대체)
- API, 서비스, 모듈 구현
- 모던 프레임워크로 UI 컴포넌트 구축
- 비즈니스 로직과 통합 개발

**기본 문법**:
```bash
/sc:implement user authentication system      # 완전한 기능 구현
/sc:implement --type component LoginForm      # 특정 컴포넌트 생성
/sc:implement --type api user-management      # API 엔드포인트 구축
/sc:implement --framework react dashboard     # 프레임워크별 구현
```

**유용한 플래그**:
- `--type component|api|service|feature|module` - 구현 타입
- `--framework react|vue|express|django|etc` - 대상 프레임워크
- `--safe` - 보수적인 구현 접근
- `--iterative` - 검증과 함께하는 단계별 개발
- `--with-tests` - 테스트 구현 포함
- `--documentation` - 코드와 함께 문서 생성

**실제 예시**:
```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

**자동 활성화 패턴**:
- **프론트엔드**: UI 컴포넌트, React/Vue/Angular → 프론트엔드 페르소나 + Magic MCP
- **백엔드**: API, 서비스, 데이터베이스 → 백엔드 페르소나 + Context7
- **보안**: 인증, 결제, 민감한 데이터 → 보안 페르소나 + 검증
- **복잡한 기능**: 다단계 구현 → Sequential MCP + 아키텍트 페르소나

---

### `/build` - 프로젝트 빌드
**기능**: 스마트 에러 처리로 프로젝트를 빌드, 컴파일, 패키지합니다.

**쉬운 방법**: `/sc:build`만 입력하면 SuperClaude가 당신의 빌드 시스템을 알아내려고 노력합니다! 🎯

**언제 사용하나요**:
- 프로젝트를 컴파일/패키지해야 할 때 (`/sc:build` 시도만 하면 됨)
- 빌드 프로세스가 실패하고 디버깅 도움을 원할 때
- 빌드 최적화 설정 (필요한 것을 감지하려고 시도함)
- 배포 준비

**기본 문법**:
```bash
/sc:build                          # 현재 프로젝트 빌드
/sc:build --type prod              # 프로덕션 빌드
/sc:build --clean                  # 클린 빌드 (오래된 아티팩트 제거)
/sc:build --optimize               # 최적화 활성화
/sc:build src/                     # 특정 디렉토리 빌드
```

**유용한 플래그**:
- `--type dev|prod|test` - 빌드 타입
- `--clean` - 빌드 전 클린
- `--optimize` - 빌드 최적화 활성화
- `--verbose` - 상세한 빌드 출력 표시

**실제 예시**:
```bash
/sc:build --type prod --optimize   # 최적화가 포함된 프로덕션 빌드
/sc:build --clean --verbose        # 상세 출력이 포함된 클린 빌드
/sc:build src/components           # 컴포넌트 폴더만 빌드
```

**주의사항**:
- 일반적인 빌드 도구(npm, webpack 등)에서 최적으로 작동
- 매우 커스텀한 빌드 설정에서는 어려움을 겪을 수 있음
- 빌드 도구가 PATH에 있는지 확인하세요