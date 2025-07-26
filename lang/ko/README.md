# SuperClaude 프레임워크 문서 🚀

**SuperClaude Framework v3.0의 포괄적인 문서 - Claude Code에 전문 명령어, 전문가 페르소나, 지능형 라우팅을 제공하는 스마트 향상 시스템.**

**[Tenten.co - AI 우선 제품 에이전시](https://tenten.co/)** 제작

---

## 📖 개요

SuperClaude Framework의 공식 문서 저장소에 오신 것을 환영합니다! 이 포괄적인 가이드는 개발자가 SuperClaude v3.0을 이해하고 효과적으로 사용하는 데 도움이 됩니다. SuperClaude는 Claude Code를 지능형 라우팅, 17개의 전문 명령어, 11개의 전문가 AI 페르소나를 갖춘 강력한 개발 어시스턴트로 변환합니다.

### SuperClaude Framework란?

SuperClaude Framework는 다음 기능을 제공하여 Claude Code의 소프트웨어 개발 워크플로우를 향상시킵니다:

- **🛠️ 17개의 전문 명령어** - `/analyze`부터 `/implement`까지, 각 명령어는 올바른 도구와 전문가를 자동으로 활성화
- **🎭 11개의 전문가 페르소나** - AI 전문가(보안, 성능, 프론트엔드 등)가 언제 개입해야 하는지 파악
- **⚡ 지능형 라우팅** - 복잡성을 자동으로 처리하는 스마트 시스템
- **🔧 MCP 서버 통합** - Context7, Sequential, Magic, Playwright를 통한 고급 기능
- **📊 증거 기반 접근법** - 모든 권장 사항은 실제 측정과 모범 사례에 기반

가장 좋은 부분은? **복잡한 시스템을 배울 필요가 없습니다** - `/analyze`나 `/build` 같은 명령어를 사용하면 SuperClaude가 나머지를 처리합니다!

---

## 🗂️ 문서 구조

### 주요 가이드 (한국어)
- **[사용자 가이드](superclaude-user-guide.md)** - 전체 개요 및 시작하기
- **[명령어 가이드](commands-guide.md)** - 모든 17개 명령어와 예제
- **[플래그 가이드](flags-guide.md)** - 명령어 플래그와 자동 활성화
- **[페르소나 가이드](personas-guide.md)** - 11개의 AI 전문가
- **[설치 가이드](installation-guide.md)** - 설정 및 구성

### 다른 언어 문서

여러 언어로 완전한 문서를 제공합니다:

#### 🌏 아시아 언어
- **🇹🇼 [繁體中文 (Traditional Chinese)](../zh-TW/)** - 대만 지역
- **🇨🇳 [简体中文 (Simplified Chinese)](../zh-CN/)** - 중국 본토
- **🇯🇵 [日本語 (Japanese)](../ja/)** - 일본
- **🇰🇷 [한국어 (Korean)](../ko/)** - 한국

#### 🌍 유럽 언어
- **🇩🇪 [Deutsch (German)](../de/)** - 독일, 오스트리아, 스위스
- **🇪🇸 [Español (Spanish)](../es/)** - 스페인과 라틴 아메리카
- **🇫🇷 [Français (French)](../fr/)** - 프랑스와 프랑스어권
- **🇵🇹 [Português (Portuguese)](../pt/)** - 브라질과 포르투갈
- **🇹🇷 [Türkçe (Turkish)](../tr/)** - 터키

#### 🌏 기타 언어
- **🇻🇳 [Tiếng Việt (Vietnamese)](../vi/)** - 베트남
- **🇸🇦 [العربية (Arabic)](../ar/)** - 중동과 북아프리카

---

## 🚀 빠른 시작

**바로 시작하고 싶으신가요?** 2분 시작 가이드입니다:

```bash
# Claude Code에서 이 명령어들을 시도해보세요:
/sc:help                    # 사용 가능한 기능 보기
/sc:analyze README.md       # SuperClaude가 프로젝트 분석
/sc:implement user-auth     # 기능과 컴포넌트 생성
/sc:build                   # 자동 최적화로 스마트 빌드
/sc:improve messy-file.js   # 코드 자동 정리
```

**방금 무슨 일이 일어났나요?** SuperClaude가 자동으로:
- 🛠️ 각 작업에 맞는 도구 선택
- 🎭  적절한 전문가(보안, 성능 등) 활성화
- ⚡ 지능형 플래그와 최적화 적용
- 📊  증거 기반 권장 사항 제공

---

## 🎯 주요 기능

### 지능형 자동화
- **자동 감지** - 시도하려는 작업 인식
- **전문가 활성화** - 각 상황에 맞는 전문가
- **지능형 라우팅** - 복잡성 자동 처리
- **증거 기반** - 모든 권장 사항은 데이터 지원

### 17개의 전문 명령어
| 카테고리 | 명령어 | 목적 |
|----------|----------|---------|
| **개발** | `/workflow`, `/implement`, `/build`, `/design` | 기능 생성 및 프로젝트 빌드 |
| **분석** | `/analyze`, `/troubleshoot`, `/explain` | 코드 이해 및 조사 |
| **품질** | `/improve`, `/cleanup`, `/test` | 코드 품질 및 테스트 |
| **관리** | `/estimate`, `/task`, `/spawn` | 프로젝트 계획 및 조정 |
| **유틸리티** | `/document`, `/git`, `/load`, `/index` | 문서 및 워크플로우 지원 |

### 11개의 전문가 페르소나
- **🏗️ 아키텍트** - 시스템 설계 및 확장성
- **🎨 프론트엔드** - UI/UX 및 접근성
- **⚙️ 백엔드** - API 및 인프라
- **🛡️ 보안** - 위협 모델링 및 규정 준수
- **⚡ 성능** - 최적화 및 병목 현상
- **🔍 분석가** - 근본 원인 조사
- **🧪 QA** - 테스트 및 품질 보증
- **🔄 리팩토러** - 코드 품질 및 정리
- **🚀 DevOps** - 배포 및 자동화
- **👨‍🏫 멘토** - 학습 및 설명
- **✍️ 스크라이브** - 문서 및 작성

---

## 📚 언어별로 시작하기

선호하는 언어를 선택하여 시작하세요:

### 아시아 언어
- **[繁體中文使用指南](../zh-TW/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드
- **[简体中文使用指南](../zh-CN/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드
- **[日本語ユーザーガイド](../ja/superclaude-user-guide.md)** - SuperClaude 프레임워크 포괄적 가이드
- **[한국어 사용자 가이드](superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드

### 유럽 언어
- **[Deutscher Benutzerführer](../de/superclaude-user-guide.md)** - 완전한 SuperClaude 프레임워크 가이드
- **[Guía del Usuario en Español](../es/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드
- **[Guide Utilisateur Français](../fr/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드
- **[Guia do Usuário Português](../pt/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드
- **[Türkçe Kullanıcı Kılavuzu](../tr/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드

### 기타 언어
- **[Hướng dẫn Người dùng Tiếng Việt](../vi/superclaude-user-guide.md)** - SuperClaude 프레임워크 완전 가이드
- **[دليل المستخدم العربي](../ar/superclaude-user-guide.md)** - SuperClaude 프레임워크 포괄적 가이드

---

## 🤝 기여

문서를 개선하기 위한 기여를 환영합니다! 오류를 발견하거나 제안이 있거나 번역을 추가하려면:

1. **문제 보고** - 문제를 설명하는 이슈 열기
2. **개선 제안** - 더 나은 문서를 위한 아이디어 공유
3. **번역 제출** - 더 많은 글로벌 개발자에게 도달하도록 도움
4. **오류 수정** - 수정을 위한 풀 리퀘스트 제출

### 번역 가이드라인
- 친근하고 접근하기 쉬운 톤 유지
- 기술적 정확성 유지
- "오버씽킹 금지" 철학 유지
- 적절한 곳에 문화적 적응 포함

---

## 📖 추가 리소스

### Tenten.co 리소스
- **[개발자 블로그](https://developer.tenten.co/)** - 기술적 통찰과 튜토리얼
- **[Shopify 개발자 블로그](https://shopify.tenten.co/)** - 이커머스 개발 가이드
- **[Tenten AI 블로그](https://tenten.co/learning/)** - AI 및 자동화 통찰
- **[GEO (AI SEO)](https://geo.tenten.co/zh-tw)** - AI 기반 SEO 도구
- **[Webflow 에이전시](https://tenten.co/solution/webflow-agency)** - 선도적인 Webflow 개발
- **[Shopify Plus 에이전시](https://tenten.co/solution/shopify)** - 엔터프라이즈 이커머스 솔루션
- **[Tenten AI](https://tentenai.com/)** - AI 혁신 컨설팅

---

## 📞 비즈니스 AI 자동화 컨설팅

**AI로 비즈니스를 혁신할 준비가 되셨나요?**

**Dify**, **N8N** 또는 기타 **비즈니스 AI 자동화** 솔루션을 구현하려면, Tenten은 지능형 자동화 워크플로우를 전문으로 하는 선도적인 AI 에이전시 중 하나입니다. 저희 전문가들은 기업이 AI 기반 자동화를 통합하여 운영을 간소화하고, 비용을 절감하며, 성장을 가속화하도록 돕습니다.

**AI 자동화를 위해 Tenten을 선택하는 이유?**
- ✅ Dify 및 N8N 구현의 **검증된 전문성**
- ✅ 전략부터 배포까지 **엔드투엔드 컨설팅**
- ✅ 비즈니스 요구에 맞춘 **맞춤형 AI 워크플로우**
- ✅ **지속적인 지원** 및 최적화

**[📅 지금 상담 예약하기](https://tenten.co/contact)** - AI 자동화가 어떻게 비즈니스 운영을 혁신하고 전례 없는 효율성을 이끌어낼 수 있는지 논의해 봅시다.

---

## 🌐 Tenten과 연결하기

### 소셜 미디어
- **[Instagram](https://instagram.com/tenten.co)** - 일일 인사이트를 위해 팔로우
- **[YouTube](https://www.youtube.com/@tenten_ai)** - AI 튜토리얼 및 사례 연구
- **[LinkedIn](https://www.linkedin.com/company/tentenco)** - 전문적인 업데이트 및 인사이트
- **[Threads](https://www.threads.net/@tenten.co)** - 빠른 업데이트 및 토론
- **[TikTok](https://www.tiktok.com/@tenten.ai)** - 짧은 형식의 AI 콘텐츠
- **[X (Twitter)](https://x.com/tentencretaive)** - 실시간 업데이트 및 아이디어
- **[뉴스레터](https://tenten.co/page/company/newsletter)** - 주간 AI 및 기술 인사이트
- **[Linktree](https://linktr.ee/tenten.co)** - 모든 링크를 한 곳에

---

## 📄 라이선스

이 문서는 오픈 소스이며 MIT 라이선스 하에 사용할 수 있습니다. 필요에 따라 자유롭게 사용, 수정 및 배포하십시오.

---

**[Tenten.co - AI 우선 제품 에이전시](https://tenten.co/)**에서 ❤️으로 제작

*지능형 문서와 AI 기반 솔루션으로 전 세계 개발자들에게 힘을 실어줍니다.*