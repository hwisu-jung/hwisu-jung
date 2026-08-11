![header](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:161b22&height=250&section=header&text=On-Device%20AI&fontSize=50&fontColor=58a6ff&fontAlignY=35&desc=Android%20Development%20%C2%B7%20LLM%20Inference%20%C2%B7%20Kotlin&descSize=18&descColor=8b949e&descAlignY=55)

### 정휘수 · Hwisu Jung

삼육대학교 컴퓨터공학부 소프트웨어전공 4학년

민감한 데이터는 서버로 보내지 않는다는 전제로, 경량 LLM을 기기에 올려 클라우드 없이 동작하는 헬스케어 앱을 만듭니다.
작은 모델의 환각과 형식 불안정을 다루는 데 대부분의 시간을 씁니다.

[![Gmail](https://img.shields.io/badge/hwisu8294@gmail.com-EA4335?style=flat-square&logo=Gmail&logoColor=white)](mailto:hwisu8294@gmail.com)

## Tech Stack

**Language**

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=Kotlin&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=C&logoColor=white)

**Android**

![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=Android&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![Room](https://img.shields.io/badge/Room-3DDC84?style=flat-square&logo=Android&logoColor=white)
![WorkManager](https://img.shields.io/badge/WorkManager-3DDC84?style=flat-square&logo=Android&logoColor=white)
![Retrofit](https://img.shields.io/badge/Retrofit-48B983?style=flat-square&logo=square&logoColor=white)

**On-Device AI**

![Gemma](https://img.shields.io/badge/Gemma%203-8E75B2?style=flat-square&logo=Google&logoColor=white)
![LiteRT-LM](https://img.shields.io/badge/LiteRT--LM-4285F4?style=flat-square&logo=Google&logoColor=white)
![ML Kit](https://img.shields.io/badge/ML%20Kit-4285F4?style=flat-square&logo=Google&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=PyTorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logoColor=black)

**Infrastructure**

![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=Firebase&logoColor=black)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=SQLite&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=Git&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=flat-square&logo=Figma&logoColor=white)

## Projects

### 당연 — 제2형 당뇨병 초기 진단자 자기관리 앱

복약·혈당·생활습관 기록을 하나의 루틴으로 통합하고, 기기 안에서 AI 리포트를 생성하는 네이티브 안드로이드 앱

`Kotlin` `Jetpack Compose` `MVVM + Clean Architecture` `Room` `Firestore` `WorkManager` `LiteRT-LM`

- 의료 데이터를 외부로 내보내지 않기 위해 Gemini API 대신 Gemma 3 270M 온디바이스 추론 채택
- 경량 모델의 환각을 막고자 리포트 생성을 8단계 선택 문제로 분해, 모델은 판단만 하고 문장은 앱이 조립
- 파싱 실패 시 temperature를 조절해 재시도, 그래도 실패하면 해당 영역만 제외하고 리포트 완성
- ML Kit 한국어 OCR로 처방전에서 약품 정보 자동 추출
- Room 단일 진실 공급원 + Firestore 동기화, 로컬 DB는 SQLCipher 암호화

아이디어톤 1위 아이디어를 제품화 → 학회 우수논문상 · 현재 앱 전용 파인튜닝 준비 중 · 비공개 저장소

### 맞춤형 복지정책 추천 앱

복지로 공공 API의 전국 17개 시·도 복지서비스를 수집·적재하고, 연령·성별·지역·소득분위를 반영해 정책을 추천하는 안드로이드 앱

`Kotlin` `Retrofit` `OkHttp` `Firestore` `Gemini API`

- 담당: 백엔드·데이터 연동
- 공공 API 연동 및 응답 파싱, OkHttp 오프라인 캐싱 구성
- Firestore 데이터 모델링과 동기화 파이프라인 설계
- 홈·지역별 정책 목록 화면 데이터 연동

2025 SW프로젝트 경진대회 최우수상 · 팀 비상구V2 · [Repository](https://github.com/cjm0423/2025SW)

### Gemma 3 270M IT Weights

앱이 실행 중 내려받는 온디바이스 배포용 양자화 모델 저장소 · [Repository](https://github.com/hwisu-jung/gemma3-270m-it-weights)

## Open Source

**[PyTorchKR/tutorials-kr](https://github.com/PyTorchKR/tutorials-kr)** — PyTorch 공식 튜토리얼 한국어 번역 저장소 Contributor

- [#1033](https://github.com/PyTorchKR/tutorials-kr/pull/1033) Intel Neural Compressor 양자화 레시피 전문 번역 · Merged (2025.10)
- [#987](https://github.com/PyTorchKR/tutorials-kr/pull/987) 번역 용어집에 `attribution` 용어 추가 · Merged (2025.11)
- [#983](https://github.com/PyTorchKR/tutorials-kr/pull/983) Captum 레시피 오탈자 수정

2025 오픈소스 컨트리뷰션 아카데미 (과학기술정보통신부 주최 · 정보통신산업진흥원 주관)

## Awards

| 수상 | 대회 | 일자 |
| --- | --- | --- |
| 우수논문상 | 한국컴퓨터정보학회 제74차 하계학술대회 | 2026.07 |
| 1위 | 2025학년도 동계 SW융합아이디어톤 | 2026.03 |
| 최우수상 | 2025학년도 SW프로젝트 경진대회 | 2025.10 |

논문 「제2형 당뇨병 진단 초기 성인의 통합 자기관리를 위한 모바일 애플리케이션 '당연' 개발: 건강기록 기반 다중 에이전트 AI 리포트를 중심으로」 공동저자 · 과학기술정보통신부 SW중심대학사업 (2021-0-01440)

## Etc

정보처리기사 · SQLD · GDGoC Sahmyook University Member (2025–2026)

![GitHub Streak](https://streak-stats.demolab.com?user=hwisu-jung&theme=dark&hide_border=true)
