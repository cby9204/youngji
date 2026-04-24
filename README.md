# 아이샵케어 CX 내부가이드

채널톡 도큐먼트를 기반으로 만든 정적 HTML 가이드북입니다.

## 📦 구성

```
.
├── index.html          # 메인 페이지 (1.8 MB)
└── images/             # 이미지 파일 472개 (약 89 MB)
```

- **92개 아티클** · **15개 카테고리** · **472개 이미지**
- 라이트/다크 모드, 실시간 검색, 반응형 디자인 지원

## 🚀 GitHub Pages 배포 방법

### 1. GitHub 저장소 생성

1. GitHub에서 새 저장소 생성 (예: `ishopcare-guide`)
2. **Public** 으로 설정 (Private은 Pro 계정 필요)

### 2. 파일 업로드

**방법 A — 웹에서 드래그앤드롭 (가장 쉬움)**

1. 생성된 저장소 페이지 접속
2. `Add file` → `Upload files`
3. `index.html` + `images` 폴더를 **통째로** 드래그앤드롭
4. 하단에 `Commit changes` 클릭

> ⚠️ 이미지가 472개라 업로드에 5~10분 소요될 수 있습니다.

**방법 B — Git 커맨드라인**

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/[사용자명]/[저장소명].git
git push -u origin main
```

### 3. GitHub Pages 활성화

1. 저장소의 `Settings` 탭
2. 좌측 메뉴 `Pages` 클릭
3. `Source` → `Deploy from a branch`
4. `Branch` → `main` + `/ (root)` 선택
5. `Save` 클릭

### 4. 접속

약 1~2분 후 아래 URL로 접속 가능:
```
https://[사용자명].github.io/[저장소명]/
```

## 🎨 커스터마이징

### 색상 변경

`index.html` 상단 `:root` CSS 변수 수정:

```css
:root {
    --accent: #0066ff;     /* 메인 컬러 */
    --bg: #ffffff;         /* 배경 */
    --text: #1a1a1a;       /* 본문 텍스트 */
}
```

### 카테고리 순서 변경

HTML 소스에서 `<section class="cat-section">` 블록의 순서를 조정하면 됩니다.

## 📝 업데이트 방법

원본 채널톡 도큐먼트가 업데이트되면:

1. 아까 실행했던 **채널톡 크롤링 스크립트 재실행**
2. 새로 다운로드된 `ishopcare_cx_guide.html` 으로 빌드 스크립트 다시 실행
3. `index.html` + 변경된 이미지만 GitHub에 재업로드

## ⚙️ 주요 기능

- ✅ **다크/라이트 모드** — 우측 상단 토글 (브라우저에 저장됨)
- ✅ **실시간 검색** — 모든 아티클 본문 검색
- ✅ **사이드바 네비게이션** — 카테고리별 접기/펼치기
- ✅ **스크롤 하이라이트** — 현재 읽는 아티클 자동 표시
- ✅ **모바일 반응형** — 960px 이하에서 햄버거 메뉴

## 📄 라이선스

내부 문서 — 외부 공개 시 주의
