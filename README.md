# 나의 시작페이지 (My Homepage)

시계, 검색창, 서울 날씨, 기술 뉴스를 한눈에 보여주는 개인 시작 페이지입니다.
순수 HTML/CSS/JS로만 작성되어 별도 설치나 빌드 과정 없이 바로 사용할 수 있습니다.

## 미리보기

- 🕐 실시간 시계 (시간대에 따라 배경이 새벽 → 낮 → 노을 → 밤으로 자연스럽게 전환)
- 🔍 검색창 (Google / Naver 전환 가능)
- ☀️ 서울 실시간 날씨 (Open-Meteo API, API 키 불필요)
- 📰 기술 뉴스 헤드라인 (Google 뉴스 RSS 기반)

## 로컬에서 바로 열어보기

`index.html` 파일을 다운로드한 뒤 더블클릭하거나 브라우저로 열면 바로 실행됩니다.
인터넷 연결만 있으면 날씨·뉴스가 자동으로 로드됩니다.

## GitHub Pages로 배포하기

1. GitHub에서 새 저장소를 만듭니다. (Public으로 설정)
2. 이 폴더의 `index.html`을 저장소 루트에 업로드합니다.
   - 웹에서: 저장소 페이지 → **Add file → Upload files** → 파일 드래그 후 Commit
   - 또는 아래 "Git으로 배포하기" 참고
3. 저장소 **Settings → Pages** 메뉴로 이동합니다.
4. **Source**를 `Deploy from a branch`로, 브랜치는 `main`, 폴더는 `/ (root)`로 설정 후 **Save**합니다.
5. 1~2분 후 아래 주소에서 접속할 수 있습니다.

   ```
   https://[사용자명].github.io/[저장소이름]/
   ```

## Git으로 배포하기 (터미널 사용 시)

```bash
cd my-homepage
git init
git add .
git commit -m "Initial commit: 나의 시작페이지"
git branch -M main
git remote add origin https://github.com/[사용자명]/[저장소이름].git
git push -u origin main
```

이후 GitHub 저장소 설정에서 위 "GitHub Pages로 배포하기" 3~5단계를 진행하면 됩니다.

## 다른 배포 방법

- **Netlify Drop**: [app.netlify.com](https://app.netlify.com) 가입 후 이 폴더를 드래그 앤 드롭하면 즉시 배포됩니다.
- **Vercel**: [vercel.com](https://vercel.com) 가입 후 이 폴더를 업로드하거나 CLI(`vercel`)로 배포할 수 있습니다.

## 브라우저 시작 페이지로 설정하기

배포한 주소(또는 로컬 파일 경로)를 브라우저의 "새 탭" 또는 "홈페이지" 설정에 등록하면
매번 브라우저를 열 때마다 이 페이지가 나타납니다. 크롬은 확장 프로그램(예: Custom New Tab URL)이 필요할 수 있습니다.

## 커스터마이징

- **날씨 지역 변경**: `index.html` 내 `loadWeather()` 함수의 `lat`, `lon` 값을 원하는 도시 좌표로 수정
- **뉴스 주제 변경**: `loadNews()` 함수의 `feedUrl`에서 `q=기술` 부분을 원하는 검색어로 수정
- **색상/폰트 변경**: `<style>` 블록 상단의 `:root` 변수(`--sun`, `--coral`, `--ink` 등) 수정

## 기술 스택

- 순수 HTML / CSS / JavaScript (프레임워크, 빌드 도구 없음)
- [Open-Meteo API](https://open-meteo.com/) — 날씨 데이터
- [Google News RSS](https://news.google.com/) + [rss2json](https://rss2json.com/) — 뉴스 데이터

## 라이선스

자유롭게 사용, 수정, 배포하세요.
