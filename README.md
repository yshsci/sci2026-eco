# Climate × Ecosystem Class Site v2

한 GitHub Pages 사이트 안에서 상단 메뉴로 네 영역을 이동합니다.

- `index.html` : 🌿 환경 변화 탐구 — 환경 변인 조작 + 관련 실제 사례 주제 + 검색 키워드 + 메모
- `research-submit.html` : 📝 사례 조사 제출 — 실제 장소/시기/생물/영향/출처 2개/종합 정리 제출
- `art-submit.html` : 🎨 AI 명화 제출 — 이미지 + 명화 이름 + 설명
- `gallery.html` : 🖼 전시관 — 제출된 AI 명화 전시

## Apps Script 연결
1. Google Sheet 하나와 이미지 저장용 Google Drive 폴더 하나를 준비합니다.
2. `apps-script/Code.gs`의 `SHEET_ID`, `FOLDER_ID`를 수정합니다.
3. Apps Script를 웹 앱으로 배포합니다.
4. `config.js`의 `WEB_APP_URL`에 웹앱 URL을 넣습니다.

첫 제출 시 같은 Google Sheet 안에 다음 시트가 자동 생성됩니다.
- `환경변화_사례탐구`
- `AI명화`

## GitHub Pages
파일 전체를 repository 최상위에 올리고 Settings → Pages → Deploy from a branch → main / root 로 설정합니다.
