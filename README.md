# Climate Art Gallery

GitHub Pages + Google Apps Script 기반 학생 작품 전시 사이트입니다.

## 사이트 구성
- `index.html` : 작품 제출
  - 이미지 업로드
  - 명화 이름
  - 설명
- `gallery.html` : 전체 작품 전시
  - 카드형 갤러리
  - 클릭 시 크게 보기
- `styles.css` : 디자인
- `config.js` : Apps Script 웹앱 URL
- `apps-script/Code.gs` : Google Sheets + Drive 저장 및 작품 목록 제공

## 1. Google Drive 준비
1. 학생 이미지 저장용 폴더를 만듭니다.
2. 폴더 URL에서 폴더 ID를 복사합니다.

## 2. Google Sheets 준비
1. 새 Google Sheet를 만듭니다.
2. URL에서 Sheet ID를 복사합니다.
3. 첫 제출 때 헤더가 자동 생성됩니다.

## 3. Apps Script
1. Apps Script 프로젝트를 만듭니다.
2. `apps-script/Code.gs` 내용을 붙여넣습니다.
3. `SHEET_ID`, `FOLDER_ID`를 실제 값으로 바꿉니다.
4. `배포 → 새 배포 → 웹 앱`
5. 실행 사용자: 나
6. 액세스 권한: 링크가 있는 모든 사용자(학교 계정 정책에 따라 조정)
7. 배포 후 웹앱 URL을 복사합니다.

## 4. GitHub Pages
1. `config.js`의 `WEB_APP_URL`을 실제 Apps Script 웹앱 URL로 바꿉니다.
2. `index.html`, `gallery.html`, `styles.css`, `config.js`를 repository 최상위에 업로드합니다.
3. `Settings → Pages → Deploy from a branch → main / (root)`를 선택합니다.

## 특징
- 사이트 화면에는 Apps Script 설정 안내 문구가 노출되지 않습니다.
- 업로드 이미지는 브라우저에서 최대 약 1600px로 축소해 전송합니다.
- 학생이 제출한 이미지는 Drive에 저장되고, 제목/설명/이미지 URL은 Sheets에 저장됩니다.
- 전시관에서는 최신 제출 작품부터 카드형으로 보여주고, 클릭하면 크게 볼 수 있습니다.
- 전시를 위해 이미지 파일은 `링크가 있는 모든 사용자 보기`로 설정됩니다.
