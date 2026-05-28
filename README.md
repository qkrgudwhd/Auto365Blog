# Auto365Blog EduTech — 수강 신청 랜딩페이지

> 33년 엔지니어의 AI 블로그 자동화 노하우를 12주 완성 커리큘럼으로 전달하는 평생교육 과정의 공식 랜딩페이지

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/docs/Web/JavaScript)
[![Three.js](https://img.shields.io/badge/Three.js-r128-000000?logo=three.js&logoColor=white)](https://threejs.org/)

---

## 📌 소개

**Auto365Blog EduTech** 는 박형종 대표(한국자아실현협회)가 운영하는 **AI 블로그 자동화 평생교육 과정**의 공식 랜딩페이지입니다.
복잡한 개발 환경 설정(Anaconda·VS Code) 없이 **Claude AI 를 파트너로 활용**해 파이썬 자동화 코드를 직관적으로 다루는 능력을 길러, 수강생이 **독립 개발자(지사 창업) + 개인 저서 출간**까지 완수하도록 설계된 12주 융합 과정입니다.

### 핵심 가치
- 🤖 **Claude AI × 파이썬** — 비전공자도 한글 대화로 자동화 코드 이해·제어
- 📚 **5종 저서 기반 교재** — 저자가 직접 출간한 Auto365Blog 시리즈 5권으로 학습
- 🌐 **4대 플랫폼 통합** — 네이버 / 티스토리 / Google Blogger / WordPress
- 💼 **수익 모델 + 저서 출간** — 라이선스 분양 + 부크크·교보문고 POD 자가출판

---

## ✨ 주요 기능

| 섹션 | 설명 |
|---|---|
| **HERO** | 스테인레스 스틸 비주얼 + 통계(33+ / 4 / 12 / 100%) + CTA |
| **강사소개** | 박형종 대표 5단 구성 (대표 키워드 · 걸어온 길 · 저서 11권 · 31+ 자격 · 비전) |
| **기능** | 4대 핵심 기능 카드 + YouTube 영상 2개 (썸네일 + 새 탭 재생) |
| **커리큘럼** | 12주 상세 표 + 4대 핵심 기술 + 핵심 요약 + 시사점 |
| **수강신청** | Google Form iframe 임베드 (자체 폼 → 구글폼 전환) |
| **커뮤니티** | 카카오 오픈채팅 / 네이버 블로그 / 이메일 / 푸터 |

### 디자인
- 🎨 **스테인레스 스틸 색상 시스템** — WCAG AAA 대비비 (11.7:1 ~ 16.5:1)
- 📱 **반응형** — 모바일 카드형 자동 전환 (`data-label` 속성 기반 테이블)
- ✨ **Three.js 배경** — 인터랙티브 3D 파티클
- 🌐 **Noto Sans/Serif KR + Orbitron** — 한국어 가독성 + 테크 감성

---

## 📁 폴더 구조

```
Auto365Blog_Landing/
├── index.html                          # 메인 랜딩페이지 (단일 파일)
├── README.md                           # 본 문서
├── .gitignore                          # 민감 정보 Git 제외 규칙
│
├── src/
│   ├── profile.png                     # 박형종 대표 프로필 이미지
│   └── config/
│       ├── user_data.json              # 공개 설정 (회사·강사·코스 정보)
│       ├── secrets.local.json.example  # 민감 정보 템플릿
│       └── secrets.local.json          # (gitignore) 실제 API 키 등
│
├── 시작가이드.txt                       # 별님 운영 가이드
└── 메일발송_설정가이드.md                # Web3Forms 설정 가이드
```

---

## 🚀 시작하기

### 1) 클론 또는 다운로드
```bash
git clone https://github.com/<your-username>/Auto365Blog_Landing.git
cd Auto365Blog_Landing
```

### 2) 민감 정보 파일 생성
```bash
# Windows PowerShell
copy src\config\secrets.local.json.example src\config\secrets.local.json

# macOS/Linux
cp src/config/secrets.local.json.example src/config/secrets.local.json
```

`src/config/secrets.local.json` 을 열어 실제 키 입력:
- `web3forms_access_key` — [Web3Forms](https://web3forms.com) 가입 후 발급
- `openai_api_key` — [OpenAI Platform](https://platform.openai.com) 콘솔
- `encryption_salt` — 32자 이상 무작위 문자열
- `client_id` — [Google Cloud Console](https://console.cloud.google.com) OAuth 2.0 클라이언트 ID

### 3) 로컬 실행
정적 HTML 사이트이므로 **별도 빌드 불필요**. 다음 중 한 가지:

```bash
# (옵션 A) Python 내장 서버
python -m http.server 8000

# (옵션 B) VS Code Live Server 확장
# index.html 우클릭 → "Open with Live Server"

# (옵션 C) 그냥 더블클릭
# index.html 을 브라우저에서 직접 열기
```

→ <http://localhost:8000> 접속

---

## 🌐 배포

정적 사이트라 어디든 배포 가능:

| 플랫폼 | 가이드 |
|---|---|
| **GitHub Pages** | Settings → Pages → main 브랜치 root 선택 |
| **Netlify** | 저장소 연결 후 자동 빌드 (build command 불필요) |
| **Vercel** | `vercel` CLI 또는 대시보드에서 import |
| **Cloudflare Pages** | 저장소 연결 → root output `/` |

⚠️ **배포 전 필수 확인**
- `src/config/secrets.local.json` 이 `.gitignore` 에 의해 제외되었는지 (`git status` 로 확인)
- 실수로 커밋한 적이 있다면 git history 정리 필요 (`git filter-repo` 등)

---

## 🔒 보안

### 민감 정보 분리 정책
- `user_data.json` — **공개 가능 정보만** (회사명·강사 소개·코스 정보)
- `secrets.local.json` — **API 키·OAuth 비밀·솔트** (gitignore 제외)
- `secrets.local.json.example` — 템플릿만 공개 (실제 값 없음)

### 정적 사이트의 한계
브라우저는 `.env`/`secrets.local.json` 을 직접 읽지 못합니다. 진정한 비밀(서버 측 API 키)이 필요하면 다음 중 하나를 사용하세요:
- **Cloudflare Workers** — 무료, 서버리스 함수
- **Vercel Functions / Netlify Functions** — 저장소 통합
- **Web3Forms** — 클라이언트에서 직접 호출 가능 (access_key 노출은 의도된 설계)

---

## 🧰 기술 스택

| 영역 | 사용 |
|---|---|
| 마크업 | HTML5 (semantic) |
| 스타일 | CSS3 (Custom Properties · Grid · Flexbox) |
| 인터랙션 | Vanilla JavaScript (의존성 없음) |
| 3D | [Three.js r128](https://threejs.org/) (HERO 배경) |
| 폼 | Google Forms (iframe 임베드) |
| 폰트 | Noto Sans KR · Noto Serif KR · Orbitron |
| 영상 | YouTube 썸네일 + 새 탭 (오류 153 회피) |

---

## 📚 강사 저서 (Auto365Blog 시리즈)

1. 《Auto365Blog 자동화 프로그램 통합편》 — 마스터 가이드
2. 《Naver 블로그 365 자동 글쓰기》 — 스마트에디터 제어
3. 《Tistory 블로그 365 자동 글쓰기》 — 애드센스 수익형
4. 《Google 블로그 365 자동 글쓰기》 — Blogger API 연동
5. 《Wordpress 블로그 365 자동 글쓰기》 — REST API·JWT

### 인문 에세이
- 《인생을 고치고 별을 품다》 (2024, 유아이북스)
- 《AI 이후의 인간: 초지능 시대, 인간의 미래를 묻다》 (2024, 부크크)
- 《사계(四季) 시리즈》 — 봄꽃·여름꽃·가을꽃·겨울꽃

---

## 📞 문의

- 📧 **Email** — phjcom3@gmail.com
- 💬 **카카오톡 오픈채팅** — <https://open.kakao.com/o/gwcemGqi>
- 📝 **블로그** — <https://blog.naver.com/com-365/224254785153>
- 🏢 **주소** — 경남 김해시 주촌면 선지로85

---

## 📜 라이선스

© 2026 한국자아실현협회 · Auto365Blog EduTech. All rights reserved.

본 랜딩페이지의 코드·디자인·콘텐츠는 박형종 대표의 지적 재산이며, 사전 동의 없는 복제·배포·상업적 이용을 금합니다.

---

<p align="center">
  <em>"기계를 고치는 일은 기술이지만, 기계 너머의 삶을 고치는 일은 예술입니다."</em><br>
  — 박형종, 인생을 고치고 별을 품다 中
</p>
