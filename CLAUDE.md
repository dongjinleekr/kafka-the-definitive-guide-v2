# Project: 카프카 핵심 가이드 홍보 사이트
기술 번역서 "카프카 핵심 가이드 (개정증보판)" 홍보용 Jekyll 사이트

## 1. Requirements
- Ruby >= 3.1 (`.ruby-version`에 명시)
- Bundler >= 2.x
- GitHub Pages 호환 gem만 사용

## 2. Commands
- **Install**:  `bundle install`
- **Serve**:    `bundle exec jekyll serve --livereload`
- **Build**:    `bundle exec jekyll build`

## 3. Project Structure

```
_config.yml           # Jekyll 설정 (remote_theme, baseurl)
_layouts/
  default.html        # Slate 테마 오버라이드 (한국어 폰트, OG 메타)
assets/css/
  style.scss          # 커스텀 스타일 (Noto Sans KR, 반응형 레이아웃)
errata/               # 정오표 페이지
  index.md
  1st/                # 1쇄 정오표
  2nd/                # 2쇄/3쇄 정오표
example/              # 예제 코드 참조
images/               # 표지, 프리뷰 이미지
index.md              # 홈페이지
_site/                # 빌드 산출물 — .gitignore에 포함
```

## 4. GitHub Pages Deployment
- **Theme**: `pages-themes/slate@v0.2.0` (remote_theme)
- **Base URL**: `/kafka-the-definitive-guide-v2`
- **Build**: GitHub Actions 자동 처리 (push 시)
- **Live**: `https://dongjinleekr.github.io/kafka-the-definitive-guide-v2/`

## 5. Slate Theme Constraints
- **Override 가능**: `_layouts/default.html`, `assets/css/style.scss`
- **Override 불가**: remote theme 원본 파일 직접 수정
- **의존성 제약**: GitHub Pages 지원 gem만 사용 (`github-pages` gem)
- **스타일 제약**: Slate 테마의 기존 클래스명/구조 유지, 스타일만 override

## 6. Coding Convention
- **Liquid**: 들여쓰기 2 spaces; 불필요한 whitespace 출력 방지 (`{%-`, `-%}` 활용)
- **HTML**: 시맨틱 태그 우선; 인라인 스타일 금지
- **SCSS**: `@import "{{ site.theme }}"`로 Slate 스타일 로드 후 override
- **한국어**: Noto Sans KR 폰트 사용, 한국어 콘텐츠

## 7. Rules
- **Non-goals**: 검색 기능, 다국어 지원 (현재 단계)
- 업데이트는 `_posts`에 저장하고 `update_type: topic|other`로 구분하며, 모두 내부 상세 페이지로 연결한다.
- `_layouts/default.html`은 레이아웃 루트 — 삭제·rename 금지
- `assets/css/style.scss`의 front matter는 필수 (빈 front matter라도)
- `_site/`의 내용을 직접 수정하거나 커밋하지 말 것
- 토큰/키/개인정보를 코드·설정·로그에 절대 포함하지 말 것
- Git 커밋은 사람이 직접 함; Claude는 커밋 메시지 초안까지만 제안
