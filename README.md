# Personal Academic Page (GitHub Pages)

이 저장소는 GitHub Pages(Jekyll)로 빌드되는 **LLM 연구자용 개인 페이지** 초안입니다.  
News/Publication은 `_data/`의 YAML만 수정하면 자동으로 반영됩니다.

## How to run (local)
macOS 기준:

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve --livereload
```

브라우저에서 `http://127.0.0.1:4000` 접속.

> 로컬 실행은 선택 사항입니다. GitHub Pages에 올리면 GitHub가 자동으로 빌드해 줍니다.

## Deploy (GitHub Pages)
1. 이 폴더를 GitHub 레포로 만들고 푸시합니다.
2. GitHub 레포 Settings → **Pages**:
   - Source: **Deploy from a branch**
   - Branch: `main` / `(root)`
3. 잠시 후 `https://<username>.github.io/<repo>/` 또는 유저 페이지 레포(`<username>.github.io`)면 `https://<username>.github.io/`로 배포됩니다.

## Edit contents (recommended)
- **프로필/링크**: `_data/profile.yml`
- **뉴스**: `_data/news.yml`
- **논문**: `_data/publications.yml`
- **메인 페이지 문구/섹션**: `index.md`

## Notes
- 이 템플릿은 GitHub Pages 기본 Jekyll 빌드를 가정합니다. 별도 플러그인 없이 동작하도록 구성했습니다.

