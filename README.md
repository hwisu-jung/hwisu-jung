![header](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:161b22&height=250&section=header&text=On-Device%20AI&fontSize=50&fontColor=58a6ff&fontAlignY=35&desc=Android%20Development%20%C2%B7%20LLM%20Inference%20%C2%B7%20Kotlin&descSize=18&descColor=8b949e&descAlignY=55)

### 정휘수 · Hwisu Jung

삼육대학교 컴퓨터공학부 소프트웨어전공 4학년 · 온디바이스 LLM

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

복약·혈당·생활습관 기록을 하나의 루틴으로 묶고, 기기 안에서 AI 리포트를 만드는 안드로이드 앱

`Kotlin` `Jetpack Compose` `MVVM + Clean Architecture` `Room` `Firestore` `WorkManager` `LiteRT-LM`

- 건강 데이터를 서버로 보내지 않기 위해 Gemini API 대신 Gemma 3 270M 온디바이스 추론 채택
- 내분비·수면·영양 세 영역에 역할을 나눈 다중 에이전트 구조로 건강 리포트 생성
- 앱 실행 중 양자화 모델을 내려받아 로컬에서 추론, 외부 LLM API 호출 없음
- ML Kit 한국어 OCR로 처방전에서 약품 정보 자동 입력
- 오프라인 우선 구조로 Room을 기준 삼아 Firestore와 동기화, 로컬 DB는 SQLCipher로 암호화

SW융합아이디어톤 1위 아이디어를 앱으로 개발해 학회 우수논문상 수상

### Gemma 3 270M IT Weights

앱에서 런타임에 다운로드하는 온디바이스용 양자화 모델 저장소 · [Repository](https://github.com/hwisu-jung/gemma3-270m-it-weights)

### 맞춤형 복지정책 추천 앱

복지로(보건복지부) 공공 API에서 전국 17개 시·도 복지서비스를 모아 Firestore에 저장하고, 사용자의 연령·성별·지역·소득분위와 후보 정책을 Gemini API에 넘겨 맞춤 정책을 추천하는 안드로이드 앱

`Kotlin` `Retrofit` `OkHttp` `Firestore` `Gemini API`

- 공공 API 연동 및 JSON 응답 파싱
- OkHttp 캐시를 걸어 오프라인에서도 정책 목록 조회 가능하도록 구성
- Firestore 스키마 설계 및 배치 저장 로직 구현
- 홈·지역별 정책 목록 화면 데이터 연동

백엔드·데이터 연동 담당 · 2025 SW프로젝트 경진대회 최우수상 · 팀 비상구V2 · [Repository](https://github.com/cjm0423/2025SW)

## Open Source

**[PyTorchKR/tutorials-kr](https://github.com/PyTorchKR/tutorials-kr)** — PyTorch 공식 튜토리얼 한국어 번역 저장소 Contributor

- [Intel Neural Compressor 양자화 레시피](https://github.com/PyTorchKR/tutorials-kr/blob/master/recipes_source/intel_neural_compressor_for_pytorch.rst) 전문 번역 · Merged ([#1033](https://github.com/PyTorchKR/tutorials-kr/pull/1033), 2025.10)

2025 오픈소스 컨트리뷰션 아카데미 (과학기술정보통신부 주최 · 정보통신산업진흥원 주관)

## Awards

| 수상 | 대회 | 주관 | 일자 |
| --- | --- | --- | --- |
| 우수논문상 | 제74차 하계학술대회 | 한국컴퓨터정보학회 | 2026.07 |
| 최우수상 | 2025학년도 SW프로젝트 경진대회 | 삼육대학교 SW중심대학사업단 | 2025.10 |
| 1위 | 2025학년도 동계 SW융합아이디어톤 | 삼육대학교 SW중심대학사업단 | 2026.03 |

논문 「제2형 당뇨병 진단 초기 성인의 통합 자기관리를 위한 모바일 애플리케이션 '당연' 개발: 건강기록 기반 다중 에이전트 AI 리포트를 중심으로」 공동저자 · 과학기술정보통신부 SW중심대학사업 (2021-0-01440)

## Certificates & Activities

정보처리기사 · SQLD · GDGoC Sahmyook University Member (2025–2026)

![GitHub Streak](https://streak-stats.demolab.com?user=hwisu-jung&theme=dark&hide_border=true)
