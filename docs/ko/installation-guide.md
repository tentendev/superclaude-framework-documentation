# SuperClaude 설치 가이드 📦

## 🎯 생각보다 쉬워요!

**솔직히 말하면**: 이 가이드가 길어 보이는 이유는 모든 세부사항을 다루고자 하기 때문입니다. 하지만 실제 설치는 정말 간단해요. 대부분의 사람들은 한 개의 명령어로 2분 안에 끝납니다!

### 1단계: 패키지 설치

**옵션 A: PyPI에서 설치 (권장)**
```bash
uv add SuperClaude
```

**옵션 B: 소스에서 설치**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```

### 🔧 UV / UVX 설정 가이드

SuperClaude v3은 [`uv`](https://github.com/astral-sh/uv) (더 빠르고 현대적인 Python 패키지 관리자) 또는 크로스 플랫폼 사용을 위한 `uvx`를 통한 설치도 지원합니다.

### 🌀 `uv`로 설치

먼저 `uv`가 설치되어 있는지 확인하세요:

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 또는 다음 지침을 따르세요: [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

`uv`가 사용 가능하면 다음과 같이 SuperClaude를 설치할 수 있습니다:

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx`로 설치 (크로스 플랫폼 CLI)

`uvx`를 사용하는 경우 다음을 실행하세요:

```bash
uvx pip install SuperClaude
```

### ✅ 설치 완료

설치 후 일반적인 설치 단계를 계속 진행하세요:

```bash
python3 -m SuperClaude install
```

또는 bash 스타일 CLI 사용:

```bash
SuperClaude install
```

### 🧠 참고:

* `uv`는 더 나은 캐싱과 성능을 제공합니다
* Python 3.8+와 호환되며 SuperClaude와 원활하게 작동합니다

---

### ⚠️ 중요 참고사항
**SuperClaude를 설치한 후,**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**

**방금 무슨 일이 일어났나요?** SuperClaude가 필요한 모든 것을 설정하려고 시도했습니다. 보통 복잡한 구성, 의존성 찾기, 설정 고민이 필요 없어요! 🎉

---

SuperClaude v3의 포괄적인 설치 가이드입니다. 하지만 기억하세요 - 대부분의 사람들은 위의 빠른 시작 이상을 읽을 필요가 없습니다! 😊

## 시작하기 전에 🔍

### 필요한 것들 💻

SuperClaude는 **Windows**, **macOS**, **Linux**에서 작동합니다. 필요한 것들:

**필수:**
- **Python 3.8 이상** - 프레임워크가 Python으로 작성되었습니다
- **Claude CLI** - SuperClaude는 Claude Code를 향상시키므로 먼저 설치해야 합니다

**선택사항 (하지만 권장):**
- **Node.js 16+** - MCP 서버 통합을 원할 때만 필요합니다
- **Git** - 개발 워크플로우에 도움이 됩니다

### 빠른 확인 🔍

설치하기 전에 기본 사항을 확인해 봅시다:

```bash
# Python 버전 확인 (3.8+ 이어야 함)
python3 --version

# Claude CLI가 설치되어 있는지 확인
claude --version

# Node.js 확인 (선택사항, MCP 서버용)
node --version
```

이 중 하나라도 실패하면 아래의 [필수 구성 요소 설정](#필수-구성-요소-설정-🛠️) 섹션을 참조하세요.

## 빠른 시작 🚀

**🏆 "그냥 작동하게 하기" 접근법 (90%의 사용자에게 권장)**

**옵션 A: PyPI에서 설치 (권장)**
```bash
pip install SuperClaude

# 권장 설정으로 설치
SuperClaude install --quick

# 끝입니다! 🎉
```

**옵션 B: 소스에서 설치**
```bash
# 저장소 복제
git clone <repository-url>
cd SuperClaude
pip install .

# 권장 설정으로 설치
SuperClaude install --quick

# 끝입니다! 🎉
```

**⚠️ 중요 참고사항**
**SuperClaude를 설치한 후,**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**

**방금 얻은 것들:**
- ✅ 전문가를 자동으로 활성화하는 16개의 스마트 명령어
- ✅ 언제 도움을 줄지 아는 11개의 전문가 페르소나
- ✅ 복잡도를 자동으로 파악하는 지능형 라우팅
- ✅ 약 2분의 시간과 ~50MB의 디스크 공간

**진짜로, 끝났습니다.** Claude Code를 열고 `/help`를 입력한 다음 SuperClaude가 마법을 부리는 것을 보세요.

**뭘 할지 걱정되나요?** 먼저 확인해 보세요:
```bash
SuperClaude install --quick --dry-run
```

## 설치 옵션 🎯

세 가지 설치 프로필 중에서 선택할 수 있습니다:

### 🎯 최소 설치
```bash
SuperClaude install --minimal
```
- **내용**: 핵심 프레임워크 파일만
- **시간**: ~1분
- **공간**: ~20MB
- **적합한 용도**: 테스트, 기본 향상, 최소 설정
- **포함**: Claude를 안내하는 핵심 동작 문서

### 🚀 빠른 설치 (권장)
```bash
SuperClaude install --quick
```
- **내용**: 핵심 프레임워크 + 16개의 슬래시 명령어
- **시간**: ~2분
- **공간**: ~50MB
- **적합한 용도**: 대부분의 사용자, 일반 개발
- **포함**: 최소 설치의 모든 것 + `/analyze`, `/build`, `/improve` 같은 특수 명령어

### 🔧 개발자 설치
```bash
SuperClaude install --profile developer
```
- **내용**: MCP 서버 통합을 포함한 모든 것
- **시간**: ~5분
- **공간**: ~100MB
- **적합한 용도**: 파워 유저, 기여자, 고급 워크플로우
- **포함**: 모든 것 + Context7, Sequential, Magic, Playwright 서버

### 🎛️ 대화형 설치
```bash
SuperClaude install
```
- 구성 요소를 선택할 수 있습니다
- 각 구성 요소의 기능에 대한 자세한 설명을 표시합니다
- 설치 내용을 제어하고 싶다면 좋습니다

## 단계별 설치 📋

### 필수 구성 요소 설정 🛠️

**Python이 없나요?**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS
brew install python3

# Windows
# https://python.org/downloads/에서 다운로드
# 또는 명령 프롬프트나 PowerShell 열기
winget install python
```

**Claude CLI가 없나요?**
- https://claude.ai/code에서 설치 지침 확인
- SuperClaude는 Claude Code를 향상시키므로 먼저 필요합니다

**Node.js가 없나요? (선택사항)**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows
# https://nodejs.org/에서 다운로드
# 또는 명령 프롬프트나 PowerShell 열기
winget install nodejs
```

### SuperClaude 가져오기 📥

**옵션 1: PyPI에서 설치 (권장)**
```bash
pip install SuperClaude
```

**옵션 2: 최신 릴리스 다운로드**
```bash
# 최신 릴리스 다운로드 및 추출
# (URL을 실제 릴리스 URL로 교체)
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**옵션 3: Git에서 복제**
```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### 설치 프로그램 실행 🎬

설치 프로그램은 꽤 똑똑하며 프로세스를 안내해 줍니다:

```bash
# 사용 가능한 모든 옵션 보기
SuperClaude install --help

# 빠른 설치 (권장)
SuperClaude install --quick

# 먼저 무슨 일이 일어날지 보고 싶나요?
SuperClaude install --quick --dry-run

# 모든 것 설치
SuperClaude install --profile developer

# 조용한 설치 (최소 출력)
SuperClaude install --quick --quiet

# 강제 설치 (확인 건너뛰기)
python3 SuperClaude.py install --quick --force
```

### 설치 중 📱

설치할 때 일어나는 일:

1. **시스템 확인** - 필요한 종속성이 있는지 확인
2. **디렉토리 설정** - `~/.claude/` 디렉토리 구조 생성
3. **핵심 파일** - 프레임워크 문서 파일 복사
4. **명령어** - 슬래시 명령어 정의 설치 (선택한 경우)
5. **MCP 서버** - MCP 서버 다운로드 및 구성 (선택한 경우)
6. **구성** - 사용자 기본 설정으로 `settings.json` 설정
7. **유효성 검사** - 모든 것이 작동하는지 테스트

설치 프로그램은 진행 상황을 표시하고 문제가 있으면 알려줍니다.

## 설치 후 ✅

### 빠른 테스트 🧪

모든 것이 작동하는지 확인해 봅시다:

```bash
# 파일이 설치되었는지 확인
ls ~/.claude/

# CLAUDE.md, COMMANDS.md, settings.json 등이 표시되어야 합니다
```

**Claude Code로 테스트:**
1. Claude Code 열기
2. `/help` 입력해 보기 - SuperClaude 명령어가 표시되어야 합니다
3. `/analyze --help` 시도 - 명령어 옵션이 표시되어야 합니다

### 설치된 내용 📂

SuperClaude는 기본적으로 `~/.claude/`에 설치됩니다. 찾을 수 있는 내용:

```
~/.claude/
├── CLAUDE.md              # 메인 프레임워크 진입점
├── COMMANDS.md            # 사용 가능한 슬래시 명령어
├── FLAGS.md               # 명령어 플래그와 옵션
├── PERSONAS.md            # 스마트 페르소나 시스템
├── PRINCIPLES.md          # 개발 원칙
├── RULES.md               # 운영 규칙
├── MCP.md                 # MCP 서버 통합
├── MODES.md               # 운영 모드
├── ORCHESTRATOR.md        # 지능형 라우팅
├── settings.json          # 구성 파일
└── commands/              # 개별 명령어 정의
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... (13개 더)
```

**각 파일의 기능:**
- **CLAUDE.md** - Claude Code에 SuperClaude에 대해 알리고 다른 파일 로드
- **settings.json** - 구성 (MCP 서버, 후크 등)
- **commands/** - 각 슬래시 명령어의 자세한 정의

### 첫 단계 🎯

시작하기 위해 이 명령어들을 시도해 보세요:

```bash
# Claude Code에서 다음을 시도해 보세요:
/sc:help                    # 사용 가능한 명령어 보기
/sc:analyze README.md       # 파일 분석
/sc:build --help           # 빌드 옵션 보기
/sc:improve --help         # 개선 옵션 보기
```

**부담스럽게 느껴져도 걱정하지 마세요** - SuperClaude는 Claude Code를 점진적으로 향상시킵니다. 원하는 만큼 많이 또는 적게 사용할 수 있습니다.

## 설치 관리 🛠️

### 업데이트 📅

SuperClaude를 최신 상태로 유지:

```bash
# 업데이트 확인
SuperClaude update

# 강제 업데이트 (로컬 변경 사항 덮어쓰기)
SuperClaude update --force

# 특정 구성 요소만 업데이트
SuperClaude update --components core,commands

# 업데이트될 내용 확인
SuperClaude update --dry-run
```

**언제 업데이트할까:**
- 새로운 SuperClaude 버전이 출시될 때
- 문제가 있을 때 (업데이트에는 종종 수정 사항이 포함됩니다)
- 새로운 MCP 서버를 사용할 수 있을 때

### 백업 💾

주요 변경 전에 백업 생성:

```bash
# 백업 생성
SuperClaude backup --create

# 기존 백업 나열
SuperClaude backup --list

# 백업에서 복원
SuperClaude backup --restore

# 사용자 지정 이름으로 백업 생성
SuperClaude backup --create --name "before-update"
```

**언제 백업할까:**
- SuperClaude 업데이트 전
- 설정 실험 전
- 제거 전
- 많이 사용자 지정한 경우 주기적으로

### 제거 🗑️

SuperClaude를 제거해야 하는 경우:

```bash
# SuperClaude 제거 (백업 유지)
SuperClaude uninstall

# 완전 제거 (모든 것 제거)
SuperClaude uninstall --complete

# 제거될 내용 확인
SuperClaude uninstall --dry-run
```

**제거되는 것:**
- `~/.claude/`의 모든 파일
- MCP 서버 구성
- Claude Code의 SuperClaude 설정

**남는 것:**
- 백업 (`--complete`를 사용하지 않는 한)
- Claude Code 자체 (SuperClaude는 건드리지 않습니다)
- 프로젝트와 기타 파일

## 문제 해결 🔧

### 일반적인 문제 🚨

**"Python을 찾을 수 없습니다"**
```bash
# python3 대신 python 시도
python --version

# 또는 설치되었지만 PATH에 없는지 확인
which python3
```

**"Claude CLI를 찾을 수 없습니다"**
- Claude Code가 먼저 설치되었는지 확인
- `claude --version`으로 확인
- https://claude.ai/code에서 설치 도움말 참조

**"권한이 거부되었습니다"**
```bash
# 명시적 Python 경로로 시도
/usr/bin/python3 SuperClaude.py install --quick

# 또는 다른 권한이 필요한지 확인
ls -la ~/.claude/
```

**"MCP 서버가 설치되지 않습니다"**
- Node.js가 설치되었는지 확인: `node --version`
- npm이 사용 가능한지 확인: `npm --version`
- 먼저 MCP 없이 설치 시도: `--minimal` 또는 `--quick`

**"설치가 중간에 실패합니다"**
```bash
# 자세한 출력으로 무슨 일이 일어나는지 확인
SuperClaude install --quick --verbose

# 또는 먼저 dry run 시도
SuperClaude install --quick --dry-run
```

### 플랫폼별 문제 🖥️

**Windows:**
- "명령을 찾을 수 없음"이 표시되면 `python3` 대신 `python` 사용
- 권한 오류가 발생하면 관리자로 명령 프롬프트 실행
- Python이 PATH에 있는지 확인

**macOS:**
- 보안 및 개인 정보 설정에서 SuperClaude를 승인해야 할 수 있습니다
- Python 3.8+가 없으면 `brew install python3` 사용
- `python` 대신 명시적으로 `python3` 사용 시도

**Linux:**
- `python3-pip`가 설치되었는지 확인
- 일부 패키지 설치에는 `sudo`가 필요할 수 있습니다
- `~/.local/bin`이 PATH에 있는지 확인

### 여전히 문제가 있나요? 🤔

**문제 해결 리소스 확인:**
- GitHub Issues: https://github.com/NomenAK/SuperClaude/issues
- 유사한 기존 문제 찾기
- 해결책을 찾을 수 없으면 새 문제 생성

**버그 보고 시 포함할 사항:**
- 운영 체제 및 버전
- Python 버전 (`python3 --version`)
- Claude CLI 버전 (`claude --version`)
- 실행한 정확한 명령
- 전체 오류 메시지
- 예상했던 동작

**도움 받기:**
- 일반적인 질문은 GitHub Discussions
- 최신 업데이트는 README.md 확인
- 알려진 문제는 ROADMAP.md 참조

## 고급 옵션 ⚙️

### 사용자 지정 설치 디렉토리

```bash
# 사용자 지정 위치에 설치
SuperClaude install --quick --install-dir /custom/path

# 환경 변수 사용
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### 구성 요소 선택

```bash
# 사용 가능한 구성 요소 보기
SuperClaude install --list-components

# 특정 구성 요소만 설치
SuperClaude install --components core,commands

# 특정 구성 요소 건너뛰기
SuperClaude install --quick --skip mcp
```

### 개발 설정

SuperClaude에 기여하거나 수정할 계획이라면:

```bash
# 모든 구성 요소를 포함한 개발자 설치
SuperClaude install --profile developer

# 개발 모드로 설치 (복사 대신 심볼릭 링크)
SuperClaude install --profile developer --dev-mode

# 개발을 위한 git 후크 설치
SuperClaude install --profile developer --dev-hooks
```

## 다음은 무엇인가요? 🚀

**이제 SuperClaude가 설치되었습니다 (쉬웠죠?):**

1. **그냥 사용 시작** - `/analyze some-file.js`나 `/build`를 시도해보고 무슨 일이 일어나는지 보세요 ✨
2. **학습에 대해 스트레스 받지 마세요** - SuperClaude는 보통 당신이 필요한 것을 알아냅니다
3. **자유롭게 실험** - `/improve`와 `/troubleshoot` 같은 명령어는 꽤 관대합니다
4. **궁금하면 가이드 읽기** - 방금 무슨 일이 일어났는지 이해하고 싶을 때 `Docs/` 확인
5. **피드백 제공** - 무엇이 작동하고 무엇이 작동하지 않는지 알려주세요

**진짜 비밀**: SuperClaude는 새로운 것들을 많이 배우지 않고도 기존 워크플로우를 향상시키도록 설계되었습니다. 일반 Claude Code처럼 사용하되, 얼마나 똑똑해지는지 주목하세요! 🎯

**여전히 불확실한가요?** `/help`와 `/analyze README.md`로 시작하세요 - 실제로는 그렇게 무섭지 않다는 것을 알게 될 겁니다.

---

## 마지막 참고사항 📝

- **설치는 1-5분 걸립니다** (선택한 항목에 따라)
- **필요한 디스크 공간: 20-100MB** (많지 않아요!)
- **기존 도구와 함께 작동** - 설정을 방해하지 않습니다
- **쉽게 제거 가능** (마음이 바뀌면)
- **커뮤니티 지원** - 실제로 이슈를 읽고 응답합니다
- ### ⚠️ 중요 참고사항
**SuperClaude를 설치한 후,**
**`SuperClaude commands`, `python3 -m SuperClaude commands` 또는 `python3 SuperClaude commands`를 사용할 수 있습니다**

SuperClaude를 시도해 주셔서 감사합니다! 개발 워크플로우를 조금 더 원활하게 만들 수 있기를 바랍니다. 🙂

---

*마지막 업데이트: 2024년 7월 - 이 가이드에 잘못되거나 혼란스러운 부분이 있으면 알려주세요!*