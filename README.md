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
![OkHttp](https://img.shields.io/badge/OkHttp-3E4348?style=flat-square&logo=square&logoColor=white)

**AI & LLM**

![Gemini API](https://img.shields.io/badge/Gemini%20API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![Multi-Agent](https://img.shields.io/badge/Multi--Agent-0A66C2?style=flat-square&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-1F6FEB?style=flat-square&logoColor=white)
![Structured Output](https://img.shields.io/badge/Structured%20Output-238636?style=flat-square&logo=json&logoColor=white)
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

복약·혈당·수면·생활습관 기록을 분석해 진료지침 근거와 함께 검증 가능한 건강 리포트를 제공하는 Android 앱

`Kotlin` `Jetpack Compose` `Gemini API` `Multi-Agent` `RAG` `Structured Output` `Room` `Firebase`

- 내분비·영양·심리/수면 전문 에이전트를 병렬 호출하고, 통합 코디네이터가 결과를 종합하는 4단계 리포트 생성 구조
- 벡터 검색 대신 항목 키로 임상 참고치를 조회해 Gemini 프롬프트에 주입하는 결정적 근거 조회 방식
- AI가 생성한 숫자를 사용자 원본 기록과 참고치에 다시 대조해 근거 없는 수치를 차단하는 검증 파이프라인
- 판정에 사용한 진료지침 문서와 연결 페이지를 리포트에 표시해 출처를 추적할 수 있도록 설계
- Structured Output으로 응답 형식을 고정하고 검증된 문장을 글자 단위로 작성하는 책 형태의 리포트 UI와 보관함 구현
- Gemini 기반 처방전 OCR, Firebase 인증·동기화, Room 기반 로컬 기록 관리
- 현재 대회 데모는 앱에서 Gemini API를 직접 호출하며 실제 서비스에서는 서버 경유 구조로 전환할 예정

SW융합아이디어톤 1위 아이디어를 앱으로 개발 · 설계와 구현 내용을 논문으로 발표해 학회 우수논문상 수상 ([Publications](#publications))

### 맞춤형 복지정책 추천 앱

복지로(보건복지부) 공공 API에서 전국 17개 시·도 복지서비스를 모아 Firestore에 저장하고, 사용자의 연령·성별·지역·소득분위와 후보 정책을 Gemini API에 넘겨 맞춤 정책을 추천하는 Android 앱

`Kotlin` `Retrofit` `OkHttp` `Firestore` `Gemini API`

- 공공 API 연동 및 JSON 응답 파싱
- OkHttp 캐시를 적용해 오프라인에서도 정책 목록을 조회할 수 있도록 구성
- Firestore 스키마 설계 및 배치 저장 로직 구현
- 홈·지역별 정책 목록 화면 데이터 연동

백엔드·데이터 연동 담당 · 2025 SW프로젝트 경진대회 최우수상 · 팀 비상구V2 · [Repository](https://github.com/cjm0423/2025SW)

## Publications

**[제2형 당뇨병 진단 초기 성인의 통합 자기관리를 위한 모바일 애플리케이션 '당연' 개발: 건강기록 기반 다중 에이전트 AI 리포트를 중심으로](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE12931707)**  
*Development of a Mobile Application for Integrated Self-Care in Adults With Early-Stage Type 2 Diabetes: Focusing on a Multi-Agent AI Report Based on Health Records*

이금선, **정휘수**, 권현석, 이회찬, 이지훈, 설미림 (삼육대학교)  
한국컴퓨터정보학회 학술발표논문집 — 2026년 하계학술대회 논문집 제34권 2호, pp. 461–464 · 2026.07 · **우수논문상**

진단 후 0–24개월 성인을 대상으로 복약 관리·알림, 혈당 기록, 생활습관 기록, 처방전 OCR, 다중 에이전트 리포트를 하나의 루틴으로 통합한 안드로이드 앱의 설계와 구현을 다룸. Kotlin·Jetpack Compose 기반 MVVM에 Room과 Firebase를 결합한 오프라인 우선 구조로 구현

`제2형 당뇨병` `자기관리` `모바일 헬스` `생성형 AI` `다중 에이전트 시스템`

## Open Source

**[PyTorchKR/tutorials-kr](https://github.com/PyTorchKR/tutorials-kr)** — PyTorch 공식 튜토리얼 한국어 번역 저장소 Contributor

- [Intel Neural Compressor 양자화 레시피](https://github.com/PyTorchKR/tutorials-kr/blob/master/recipes_source/intel_neural_compressor_for_pytorch.rst) 전문 번역 · Merged ([#1033](https://github.com/PyTorchKR/tutorials-kr/pull/1033), 2025.10)

2025 오픈소스 컨트리뷰션 아카데미  
과학기술정보통신부 주최 · 정보통신산업진흥원 주관

## Awards

| 수상 | 대회 | 주관 | 일자 |
| --- | --- | --- | --- |
| 우수논문상 | 제74차 하계학술대회 | 한국컴퓨터정보학회 | 2026.07 |
| 최우수상 | 2025학년도 SW프로젝트 경진대회 | 삼육대학교 SW중심대학사업단 | 2025.10 |
| 1위 | 2025학년도 동계 SW융합아이디어톤 | 삼육대학교 SW중심대학사업단 | 2026.03 |

과학기술정보통신부 SW중심대학사업 (2021-0-01440)

## Certificates & Activities

정보처리기사 · SQLD · GDGoC Sahmyook University Member (2025–2026)

<br>

<p align="center">
  <sub>Android Developer · AI-powered Mobile Applications</sub>
</p>
