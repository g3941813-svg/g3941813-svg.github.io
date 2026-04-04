---
title: "GitHub Pages에 Jekyll 블로그 개설하기"
date: 2025-04-04 18:00:00 +0900
categories: [블로그, Jekyll, GitHub Pages]
tags: [blog, jekyll, github-pages, tutorial]
---

처음으로 GitHub Pages에 Jekyll 블로그를 개설한 과정을 기록합니다.

## 목표

- 무료 GitHub Pages 호스팅
- Jekyll 정적 사이트 생성기 사용
- 빠르고 간단한 설정

## 단계별 설치 과정

### 1. Git 설치

먼저 Git을 설치했습니다. Homebrew를 사용:

```bash
brew install git
```

### 2. 레포지토리 클론

GitHub 저장소를 로컬로 클론:

```bash
git clone https://github.com/g3941813-svg/g3941813-svg.github.io.git blog
cd blog
```

### 3. Ruby 환경 확인

macOS에는 Ruby가 기본으로 설치되어 있었습니다:

```bash
ruby --version
# ruby 2.6.10p210
```

### 4. Jekyll 설치

RubyGems을 통해 Jekyll과 Bundler 설치:

```bash
sudo gem install jekyll bundler --no-document
```

### 5. Jekyll 사이트 생성

현재 폴더에 새 Jekyll 사이트를 생성했습니다:

```bash
jekyll new . --force
```

기본 테마로 **minima**가 적용되었습니다.

### 6. 설정 수정

`_config.yml`을 GitHub Pages에 맞게 수정했습니다:

```yaml
title: Ghost Blog
url: "https://g3941813-svg.github.io"
github_username: g3941813-svg
```

### 7. 사이트 빌드

로컬에서 사이트를 빌드했습니다:

```bash
bundle exec jekyll build
```

`_site` 폴더에 HTML 파일들이 생성되었습니다.

### 8. GitHub에 푸시

```bash
git add -A
git commit -m "Initial Jekyll site setup"
git push origin main
```

### 9. GitHub Pages 활성화

Repository Settings → Pages → Source: main branch / (root)

**자동 배포 완료!** 🎉

## 결과

사이트 주소: https://g3941813-svg.github.io/

기본 Jekyll minima 테마가 적용된 깔끔한 블로그가 생성되었습니다.

## 다음 계획

- 포스트 작성 방법
- 테마 커스터마이징
- 커스텀 도메인 연결
- SEO 최적화

---

Jekyll은 설정이 간단하고 GitHub Pages와 잘 통합되어서 만족스럽습니다. 
앞으로 development journeys를 이 블로그에 기록할 예정입니다!
