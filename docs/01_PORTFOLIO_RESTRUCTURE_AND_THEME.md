# Portfolio Restructure & Theme Redesign (Gemini CLI Prompt)

## 역할 정의

너는 시니어 프론트엔드 엔지니어이자 UI 디자이너다.
목표는 단일 HTML 포트폴리오를
“밝고 정돈된 Technical PM 포트폴리오 웹사이트”로 재구성하는 것이다.

질문하지 말고, 합리적인 가정 하에 즉시 실행한다.

---

## 현재 상태

- HTML 파일 1개에 모든 내용이 들어 있음
- 다크 테마 기반으로 전체가 칙칙하고 상막함
- 프로젝트/공모전/역할 구분이 약함

---

## 최종 목표

- 화이트 기반이지만 가볍지 않은 톤
- 구조가 먼저 보이는 레이아웃
- 외부 평가(공모전·수상)가 명확히 드러나는 포트폴리오
- GitHub Pages에 바로 배포 가능한 구조

---

## 1. 파일 구조 재정의 (필수)

아래 구조로 프로젝트를 재구성한다.

portfolio/
├─ index.html # Hero + 요약
├─ projects.html # 프로젝트 상세
├─ competitions.html # 공모전 · 수상
├─ assets/
│ ├─ css/
│ │ ├─ reset.css
│ │ ├─ tokens.css # 디자인 토큰
│ │ ├─ layout.css # 공통 레이아웃
│ │ ├─ components.css # 카드, 버튼
│ │ └─ pages.css # 페이지별 보정
│ ├─ js/
│ │ └─ main.js
│ └─ images/
│ └─ projects/
└─ README.md (선택)

yaml
코드 복사

조건:

- 프레임워크 사용 금지
- 기존 콘텐츠는 삭제하지 말고 역할에 맞게 이동
- 공통 헤더/푸터 유지

---

## 2. 밝은 테마 디자인 토큰 정의

`assets/css/tokens.css`에 CSS 변수를 정의한다.

### 색상

- 배경: #f8fafc
- 섹션: #ffffff
- 카드 테두리: #e5e7eb

### 텍스트

- 메인: #111827
- 보조: #4b5563
- 약한 텍스트: #6b7280

### 포인트 컬러 (1개만)

- Primary: #2563eb
- 버튼 / 링크 / 강조에만 사용

### UI 공통

- border-radius: 12px
- shadow는 매우 부드럽게
- hover 시 명확한 상태 변화

---

## 3. index.html 역할 정의

index.html은 “표지” 역할만 수행한다.

포함:

- Hero 섹션
- Core Skills 요약
- 대표 프로젝트 2개 링크
- 공모전 요약 (최우수상 강조)
- Projects / Competitions 페이지 링크

금지:

- 프로젝트 상세 설명
- 긴 문단

---

## 4. Hero 섹션 구조

텍스트 구조:
김현중
Technical PM · 구조 설계형 서비스 기획자
아이디어를 실행 가능한 구조로 설계합니다.

yaml
코드 복사

조건:

- 이름 가장 크게
- 직무는 서브 타이틀
- 설명 문단은 2줄 이내
- 버튼은 Primary 컬러 사용

---

## 결과물 요구

1. 최종 파일 트리
2. 각 파일 역할 요약
3. 수정된 코드 (전체 또는 diff)
4. 적용 방법
