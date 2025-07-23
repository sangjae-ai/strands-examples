# Strands Agent 세션 데모

이 저장소는 **Strands Agent**에 대한 세션 발표를 위한 실습 코드와 데모를 포함하고 있습니다. Strands Agent는 AWS에서 개발한 차세대 AI 에이전트 프레임워크로, MCP(Model Context Protocol)를 활용하여 다양한 도구와 서비스를 통합할 수 있는 강력한 기능을 제공합니다.

## 📋 세션 개요

이 세션에서는 Strands Agent의 핵심 기능들을 단계별로 학습하고 실습해볼 수 있습니다:

- **기본 에이전트 사용법**: 도구 없이 기본 LLM 기능 체험
- **도구 통합**: 계산기, 시간, Python REPL 등 내장 도구 활용
- **대화 관리**: 세션 상태 및 메시지 히스토리 관리
- **MCP 통합**: 외부 서비스와의 연동 (웹 검색, Notion 등)
- **고급 활용**: 다중 MCP 서버를 활용한 복합 워크플로우

## 🚀 시작하기

### 사전 요구사항

- Python 3.8+
- Node.js (MCP 서버용)
- AWS 계정 (Strands Agent 사용)

### 설치

1. 저장소 클론
```bash
git clone <repository-url>
cd strands
```

2. Python 가상환경 생성 및 활성화
```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
# 또는 Windows의 경우: venv\Scripts\activate
```

3. Python 의존성 설치
```bash
pip install -r requirements.txt
```

4. Node.js 의존성 설치
```bash
npm install
```

5. 환경 변수 설정
```bash
cp .env.example .env
# .env 파일을 편집하여 필요한 API 키들을 설정하세요
```

## 📚 실습 가이드

### Lab 01: 기본 에이전트 체험
**파일**: `lab-01.ipynb`

Strands Agent의 기본 기능을 체험해봅니다. 도구 없이 LLM만으로 다음 질문들에 답변하는 과정을 관찰합니다:

- 현재 서울 시각 확인
- 수학 계산 (3111696 / 74088)
- 문자열 분석 ("strawberry"에서 'r' 개수)
- Python 스크립트 작성 및 검증

**학습 목표**: 
- 도구 없는 LLM의 한계점 이해
- 할루시네이션 및 부정확한 답변 관찰

### Lab 02: 대화 관리 및 도구 활용
**파일**: `lab-02.ipynb`

에이전트의 대화 상태 관리와 내장 도구들을 활용해봅니다:

- 대화 히스토리 관리
- 계산기 도구 사용
- 현재 시간 도구 활용
- Python REPL 도구 실행

**학습 목표**:
- 에이전트 상태 관리 이해
- 내장 도구의 효과적 활용법 습득

### Lab 03: MCP 기초
**파일**: `lab-03-mcp.ipynb`

MCP(Model Context Protocol)의 기본 개념과 활용법을 학습합니다:

- MCP 클라이언트 설정
- 외부 서비스 연동
- 웹 검색 기능 활용
- 실시간 정보 검색 및 활용

**학습 목표**:
- MCP의 개념과 장점 이해
- 외부 데이터 소스 통합 방법 습득

### Lab 04: 고급 MCP 활용
**파일**: `lab-04-mcp-adv.ipynb`

다중 MCP 서버를 활용한 복합 워크플로우를 구현합니다:

- 웹 검색 MCP 서버 활용
- Notion MCP 서버 연동
- 검색 → 분석 → 문서화 파이프라인 구축
- 자동화된 보고서 생성

**학습 목표**:
- 다중 MCP 서버 통합 방법
- 복합 워크플로우 설계 및 구현
- 실무 활용 사례 체험

## 🛠️ 주요 기술 스택

- **Strands Agent**: AWS의 AI 에이전트 프레임워크
- **MCP (Model Context Protocol)**: 외부 서비스 통합 프로토콜
- **Python**: 주요 개발 언어
- **Jupyter Notebook**: 실습 환경
- **Node.js**: MCP 서버 실행 환경

## 📁 프로젝트 구조

```
strands/
├── lab-01.ipynb              # 기본 에이전트 체험
├── lab-02.ipynb              # 대화 관리 및 도구 활용
├── lab-03-mcp.ipynb          # MCP 기초
├── lab-04-mcp-adv.ipynb      # 고급 MCP 활용
├── requirements.txt          # Python 의존성
├── package.json              # Node.js 의존성
├── .env                      # 환경 변수 (API 키 등)
├── results/                  # 실행 결과 저장
├── logs/                     # 로그 파일
└── streamlit_demo/           # Streamlit 데모 앱
```

## 🔧 환경 설정

### 필요한 API 키

`.env` 파일에 다음 API 키들을 설정해야 합니다:

```env
# AWS 자격 증명 (Strands Agent용)
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=us-east-1

# Notion API (Lab 04용)
NOTION_API_KEY=your_notion_api_key

# 기타 필요한 API 키들
BYPASS_TOOL_CONSENT=true
```

## 🎯 학습 목표

이 세션을 통해 다음을 학습할 수 있습니다:

1. **Strands Agent 기초**: 에이전트 생성, 설정, 기본 사용법
2. **도구 통합**: 내장 도구 및 커스텀 도구 활용
3. **MCP 활용**: 외부 서비스와의 효과적인 연동
4. **실무 적용**: 실제 업무에서 활용 가능한 워크플로우 구축
5. **모범 사례**: 에이전트 개발 및 운영 시 고려사항

## 🚨 주의사항

- 실습 진행 전 모든 의존성이 올바르게 설치되었는지 확인하세요
- API 키는 절대 공개 저장소에 커밋하지 마세요
- 각 Lab은 순서대로 진행하는 것을 권장합니다
- 실습 중 발생하는 오류는 로그를 확인하여 디버깅하세요

## 📞 지원

실습 중 문제가 발생하거나 질문이 있으시면:

1. 각 노트북의 주석과 설명을 먼저 확인해주세요
2. `logs/` 폴더의 로그 파일을 확인해주세요
3. AWS Strands Agent 공식 문서를 참조해주세요

---

**Happy Learning with Strands Agent! 🎉**
