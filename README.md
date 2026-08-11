![header](https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:161b22&height=250&section=header&text=On-Device%20AI&fontSize=50&fontColor=58a6ff&fontAlignY=35&desc=Android%20Development%20%C2%B7%20LLM%20Inference%20%C2%B7%20Kotlin&descSize=18&descColor=8b949e&descAlignY=55)

## 정휘수 Hwisu Jung

삼육대학교 컴퓨터공학부 소프트웨어전공 4학년

건강 데이터처럼 민감한 정보를 서버로 보내지 않고 기기 안에서 처리하는 방법에 관심이 있습니다.
경량 LLM을 모바일에 올려 클라우드 없이 동작하는 헬스케어 앱을 만들고 있고,
그 과정에서 필요해진 모델 경량화와 양자화를 함께 공부하고 있습니다.

hwisu8294@gmail.com

## Tech

- Language — Kotlin, Java, Python, C
- Android — Jetpack Compose, Room, WorkManager, Coroutines/Flow, Retrofit
- On-Device AI — Gemma 3, LiteRT-LM, ML Kit, PyTorch, Hugging Face
- Infrastructure — Firebase, SQLite, MySQL, Git

## Projects

### 당연 — 제2형 당뇨병 초기 진단자 자기관리 앱

복약·혈당·생활습관 기록을 하나의 루틴으로 통합하고, 기기 안에서 AI 리포트를 생성하는 네이티브 안드로이드 앱입니다.
동계 SW융합아이디어톤에서 1위한 아이디어를 제품으로 발전시켰고, 개발 결과를 한국컴퓨터정보학회 하계학술대회 논문으로 정리해 우수논문상을 받았습니다.

Kotlin · Jetpack Compose · MVVM + Clean Architecture · Room · Firestore · WorkManager · LiteRT-LM

- 역할 기반 다중 에이전트 리포트 — 내분비, 수면·심리, 영양 세 영역에 각각 역할을 부여한 프롬프트를 여덟 단계로 나눠 순차 호출합니다. 경량 모델이 한 번에 처리하기 어려운 분석을 단계별 판단 문제로 분해한 구조입니다.
- 환각 제어와 폴백 — 모델이 수치를 지어내지 않도록 출력을 정해진 선택지 안으로 제한하고, 파싱에 실패하면 temperature를 조절해 재시도하도록 만들어 리포트 생성 안정성을 확보했습니다.
- 처방전 OCR — ML Kit 한국어 텍스트 인식으로 처방전에서 약품 정보를 추출해 수기 입력 부담을 줄였습니다.
- 오프라인 우선 저장 — Room을 단일 진실 공급원으로 두고 Firestore와 동기화하며, 로컬 DB는 SQLCipher로 암호화합니다.
- 외부 LLM API를 쓰지 않기 때문에 건강 기록이 기기 밖으로 나가지 않습니다.

비공개 저장소

### 맞춤형 복지정책 추천 앱

복지로 공공 API에서 전국 17개 시·도의 지역별 복지서비스를 수집해 Firestore에 적재하고,
사용자의 연령·성별·지역·소득분위를 반영해 맞춤 정책을 추천하는 안드로이드 앱입니다.
2025학년도 SW프로젝트 경진대회 최우수상, 팀 비상구V2.

담당은 백엔드와 데이터 연동입니다.

- 공공 API 연동 및 응답 파싱, Retrofit/OkHttp 오프라인 캐싱 설정
- Firestore 데이터 모델링과 동기화 파이프라인 구성
- 홈 화면과 지역별 정책 목록의 데이터 연동

[github.com/cjm0423/2025SW](https://github.com/cjm0423/2025SW)

### Gemma 3 270M IT Weights

온디바이스 배포용 Gemma 3 270M IT 가중치 저장소입니다. 앱이 실행 중에 내려받는 양자화 모델 파일을 호스팅합니다.

[github.com/hwisu-jung/gemma3-270m-it-weights](https://github.com/hwisu-jung/gemma3-270m-it-weights)

## Open Source

### PyTorch 한국어 튜토리얼

PyTorch 공식 튜토리얼 한국어 번역 저장소 [PyTorchKR/tutorials-kr](https://github.com/PyTorchKR/tutorials-kr) 컨트리뷰터입니다.

- [#1033](https://github.com/PyTorchKR/tutorials-kr/pull/1033) Intel Neural Compressor 양자화 레시피 전문 번역 (Merged, 2025.10)
  FP8과 가중치 전용 양자화, PT2E 정적 양자화, 정확도 기반 자동 튜닝을 다루는 문서로, 메인테이너 두 명의 리뷰를 거쳐 반영되었습니다.
- [#987](https://github.com/PyTorchKR/tutorials-kr/pull/987) 번역 용어집에 attribution 용어 추가 (Merged, 2025.11)
- [#983](https://github.com/PyTorchKR/tutorials-kr/pull/983) Captum 레시피 오탈자 수정

모델 경량화 문서를 번역하며 얻은 이해가 이후 온디바이스 작업으로 이어졌습니다.
2025 오픈소스 컨트리뷰션 아카데미(과학기술정보통신부 주최, 정보통신산업진흥원 주관) 참여.

## Awards

- 우수논문상 — 한국컴퓨터정보학회 제74차 하계학술대회 (2026.07)
  「제2형 당뇨병 진단 초기 성인의 통합 자기관리를 위한 모바일 애플리케이션 '당연' 개발: 건강기록 기반 다중 에이전트 AI 리포트를 중심으로」 공동저자
  과학기술정보통신부 SW중심대학사업 지원 과제 (2021-0-01440)
- 1위 — 2025학년도 동계 SW융합아이디어톤, 삼육대학교 SW중심대학사업단 (2026.03)
- 최우수상 — 2025학년도 SW프로젝트 경진대회, 삼육대학교 SW중심대학사업단 (2025.10)

## Etc

정보처리기사, SQLD
GDGoC Sahmyook University Member (2025–2026)

![GitHub Streak](https://streak-stats.demolab.com?user=hwisu-jung&theme=dark&hide_border=true)
