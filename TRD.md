# 기술 설계

- index.html: MediaPipe 사진 분류 화면. 브라우저 추론.
- weather.html: Open-Meteo GET 요청과 JSON 표시.
- PRD.md: 사용자 요구와 완료 조건.
- task.md: 구현 단위와 확인 절차.
- skill.md: AI에 전달하는 프로젝트 작업 규칙 문서.

## 데이터 흐름
사진 입력 → 브라우저 모델 추론 → 분류 이름과 점수 표시.
날씨 버튼 → 공개 날씨 API → JSON → 기온 표시.

## 저장과 서버 확장
후속 실습에서 Supabase observations(id, label, score, note, created_at)을 만든다. 비밀 키가 필요한 API는 서버에서 호출하고 환경 변수로 관리한다. GitHub Pages는 정적 파일을 제공하므로 서버 코드는 실행하지 않는다.