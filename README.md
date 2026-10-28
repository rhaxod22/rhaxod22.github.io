# rhaxod22.github.io

Personal academic homepage, served by GitHub Pages at <https://rhaxod22.github.io>.
빌드 도구 없이 HTML/CSS 파일만으로 이루어져 있습니다.

## 파일 구조

| 파일 | 내용 |
| --- | --- |
| `index.html` | 페이지 내용 전체. 내용 수정은 거의 여기서만 합니다 |
| `style.css` | 디자인. 맨 위 `:root` 의 색상/글꼴 값만 바꿔도 분위기가 바뀝니다 |
| `assets/profile.svg` | 프로필 사진 자리 (임시 그림) |
| `assets/favicon.svg` | 브라우저 탭 아이콘 |
| `.nojekyll` | GitHub Pages가 Jekyll 변환을 하지 않고 파일을 그대로 올리게 하는 빈 파일 |

## 채워 넣을 것

내용은 CV(2026년 기준)로 채워 두었습니다. `index.html` 에서 `TODO` 를 검색하면 남은 곳이 나옵니다.

- [ ] 프로필 사진 → `assets/profile.jpg` 로 넣고 `<img src=...>` 수정
- [ ] (선택) 한글 이름, 지도교수 홈페이지 링크, Google Scholar
- [ ] 새 논문·발표가 생기면 Publications / Talks 에 추가
- [ ] 고칠 때마다 footer 의 `Last updated` 날짜

## 게시하기 (GitHub Pages)

저장소 이름을 **정확히 `rhaxod22.github.io`** 로 만들어야 `https://rhaxod22.github.io` 주소가 됩니다.

### 방법 A — 웹에서 업로드 (가장 쉬움)

1. GitHub 에 로그인 → 오른쪽 위 **+** → **New repository**
2. Repository name: `rhaxod22.github.io`, **Public** 선택 → **Create repository**
3. 생성된 페이지에서 **uploading an existing file** 클릭 → 이 폴더의 파일과 `assets` 폴더를 끌어다 놓기 → **Commit changes**
4. **Settings → Pages** 에서 Source 가 *Deploy from a branch*, Branch 가 `main` / `(root)` 인지 확인
5. 1–2분 뒤 <https://rhaxod22.github.io> 접속

### 방법 B — git 명령어

이 폴더 안에서:

```bash
git init -b main
git add .
git commit -m "Initial homepage"
git remote add origin https://github.com/rhaxod22/rhaxod22.github.io.git
git push -u origin main
```

(먼저 GitHub 에서 빈 저장소 `rhaxod22.github.io` 를 만들어 두어야 합니다. 처음 push 할 때 로그인 창이 뜹니다.)

이후 수정할 때는:

```bash
git add .
git commit -m "Update publications"
git push
```

## 내 컴퓨터에서 미리보기

`index.html` 을 더블클릭해서 브라우저로 열어도 되고, 이 폴더에서 아래를 실행한 뒤 <http://localhost:8000> 을 열어도 됩니다.

```bash
python -m http.server 8000
```
