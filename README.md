![header](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:161b22&height=250&section=header&text=On-Device%20AI&fontSize=50&fontColor=58a6ff&fontAlignY=35&desc=Android%20Development%20%C2%B7%20LLM%20Inference%20%C2%B7%20Kotlin&descSize=18&descColor=8b949e&descAlignY=55)

## 👤 About Me

**정휘수** · 삼육대학교 컴퓨터공학부 소프트웨어전공 4학년

온디바이스 AI | 안드로이드 앱 개발 · LLM 경량화 · 모바일 추론

민감한 건강 데이터를 서버로 보내지 않고 기기 안에서 처리하는 방법에 관심이 많습니다.
경량 LLM(Gemma 3 270M)을 온디바이스로 구동해, 클라우드 API 없이 동작하는 헬스케어 앱을 만들고 있습니다.

- 한국컴퓨터정보학회 하계학술대회 **우수논문상** (2026.07)
- 온디바이스 Gemma 3 기반 다중 에이전트 리포트 파이프라인 설계·구현
- 헬스케어 안드로이드 앱 `당연` 개발 (Kotlin · Jetpack Compose · Clean Architecture)
- 정보처리기사 · SQLD

📮 hwisu8294@gmail.com

## 🔧 Tech Stack

### Language

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=Kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=C&logoColor=white)

### Android

![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=Android&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![Room](https://img.shields.io/badge/Room-3DDC84?style=flat-square&logo=Android&logoColor=white)
![WorkManager](https://img.shields.io/badge/WorkManager-3DDC84?style=flat-square&logo=Android&logoColor=white)
![Coroutines](https://img.shields.io/badge/Coroutines%20%2F%20Flow-7F52FF?style=flat-square&logo=Kotlin&logoColor=white)

### On-Device AI

![Gemma](https://img.shields.io/badge/Gemma%203%20270M-8E75B2?style=flat-square&logo=Google&logoColor=white)
![LiteRT](https://img.shields.io/badge/LiteRT--LM-4285F4?style=flat-square&logo=Google&logoColor=white)
![ML Kit](https://img.shields.io/badge/ML%20Kit-4285F4?style=flat-square&logo=Google&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=PyTorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logoColor=black)

### Infrastructure

![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=Firebase&logoColor=black)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=SQLite&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=Git&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=Figma&logoColor=white)

## 📌 Projects

### 💊 당연 — 제2형 당뇨병 초기 진단자 자기관리 앱

복약·혈당·생활습관 기록을 하나의 루틴으로 통합하고, **기기 내부에서** AI 리포트를 생성하는 네이티브 안드로이드 앱

> `SW융합아이디어톤 1위(2026.03)` → `앱 개발` → `한국컴퓨터정보학회 우수논문상(2026.07)`
> 아이디어톤에서 1위한 「먹기전에, 약속」을 실제 제품으로 발전시키고, 그 결과를 논문으로 정리했습니다.

| 항목 | 내용 |
| --- | --- |
| 아키텍처 | Kotlin · Jetpack Compose(Material 3) · MVVM + Clean Architecture |
| 데이터 | Room(SQLite) + Firestore 오프라인 우선 하이브리드 · WorkManager 복약 알림 |
| AI | Gemma 3 270M IT 온디바이스 추론 (LiteRT-LM) · ML Kit 한국어 OCR |
| 보안 | SQLCipher 기반 DB 암호화 · EncryptedSharedPreferences · Firebase Auth(Google 로그인) · 외부 LLM API 미사용 |

**핵심 설계**

- **역할 기반 다중 에이전트 파이프라인** — 내분비 전문의·수면 전문의·종합 주치의 역할을 부여한 프롬프트 체인을 순차 호출해, 단일 경량 모델의 한계를 보완한 심층 리포트를 생성
- **처방전 OCR 자동 입력** — ML Kit 한국어 텍스트 인식으로 처방전에서 약품 정보를 추출해 수기 입력 부담 제거
- **환각(Hallucination) 제어** — 수치 생성 대신 엄격한 분류(Classification) 규칙을 강제하고, 파싱 실패 시 Temperature를 동적으로 조절해 재시도하는 폴백 로직으로 리포트 생성 안정성 확보
- **다중 데이터 스트림 최적화** — 혈당·복약·생활습관 Room Flow를 `combine`으로 단일 UI State에 통합해 불필요한 리컴포지션 제거

> Private Repository

### ⚙️ Gemma 3 270M IT Weights

모바일 배포용 Gemma 3 270M IT 웨이트 호스팅 및 경량화·배포 파이프라인 구성

**[GitHub →](https://github.com/hwisu-jung/gemma3-270m-it-weights)**

## 🏆 Awards

**우수논문상** · 한국컴퓨터정보학회 제74차 하계학술대회 (2026.07)
> 「제2형 당뇨병 진단 초기 성인의 통합 자기관리를 위한 모바일 애플리케이션 '당연' 개발: 건강기록 기반 다중 에이전트 AI 리포트를 중심으로」 · 공동저자
> 과학기술정보통신부 SW중심대학사업 지원 과제 (2021-0-01440)

**1위** · 2025학년도 동계 SW융합아이디어톤, 삼육대학교 SW중심대학사업단 (2026.03)
> 팀 뉴트리세이프 — 「먹기전에, 약속」 (→ `당연` 앱으로 발전)

**최우수상** · 2025학년도 SW프로젝트 경진대회, 삼육대학교 SW중심대학사업단 (2025.10)
> 팀 비상구V2 — **맞춤형 복지정책 추천 안드로이드 앱**
> 복지로(보건복지부) 지역별 복지서비스 공공 API에서 전국 17개 시·도 정책을 수집·정규화해 Firestore에 적재하고,
> 사용자의 연령·성별·지역·소득분위를 반영한 LLM 프롬프트로 개인 맞춤 정책을 추천하는 앱입니다.
> **담당: 백엔드 · 데이터 연동** — 공공 API 연동(Retrofit/OkHttp 오프라인 캐싱), Firestore 데이터 모델링 및 동기화 파이프라인, 정책 목록·홈 화면 데이터 바인딩
> **[GitHub →](https://github.com/cjm0423/2025SW)**

## 🌱 Open Source

### PyTorch 한국어 튜토리얼 — [PyTorchKR/tutorials-kr](https://github.com/PyTorchKR/tutorials-kr) ⭐379

PyTorch 공식 튜토리얼 한국어 번역 저장소 Contributor

- **[#1033](https://github.com/PyTorchKR/tutorials-kr/pull/1033)** · `Intel® Neural Compressor를 활용한 손쉬운 양자화(Quantization)` 레시피 전문 번역 — **Merged (2025.10)**
  FP8 · 가중치 전용(weight-only) 양자화, PT2E 백엔드 정적 양자화, 정확도 기반 자동 튜닝을 다루는 문서로,
  메인테이너 2인 리뷰를 거쳐 4회 수정 후 반영되었습니다. → [번역 문서 보기](https://github.com/PyTorchKR/tutorials-kr/blob/master/recipes_source/intel_neural_compressor_for_pytorch.rst)
- **[#987](https://github.com/PyTorchKR/tutorials-kr/pull/987)** · 번역 용어집(`TRANSLATION_GUIDE.md`)에 `attribution` 용어 추가 — **Merged (2025.11)**
  용어집 투표를 거쳐 공식 번역 용어로 등재
- **[#983](https://github.com/PyTorchKR/tutorials-kr/pull/983)** · `recipes/Captum_Recipe.py` 오탈자 수정

> 모델 경량화·양자화 문서를 번역하며 얻은 이해가 이후 온디바이스 LLM 작업으로 이어졌습니다.
> 2025 오픈소스 컨트리뷰션 아카데미(과학기술정보통신부 주최 · 정보통신산업진흥원 주관, 2025.09 – 10) 참여

**GDGoC Sahmyook University Member** (2025 – 2026)

## 📊 GitHub Stats

![GitHub Streak](https://streak-stats.demolab.com?user=hwisu-jung&theme=dark&hide_border=true)
