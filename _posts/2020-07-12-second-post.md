---
title: "git 블로그 설정"
date: 2020-07-12 23:09:28 -0400
categories: fastlane dev study
---
1. gitHub가입
[git-join] -> 'https://github.com/'

2. git Repositories 생성 'Repositories > New'
- Repository name 입력 'hui0222.github.io'
- Description (설명) 입력
- Public or Private (공유 및 비공개 선택)
- Initialize this repository with a README (기본파일 생성 체크)
- Create repository (생성하기)

3. Jekyll 테마 찾기. 
- GitHub에는 이미 수백 개의 Jekyll 테마가 공개되어 있습니다. 
- jekyll-theme이라는 topic을 갖고 있는 repository는 모두 공개된 jekyll 테마인데요. 
- 이 중 어떤 테마든 내 블로그에 적용하고 싶은 테마를 선택해 보세요
[git-theme]'https://github.com/topics/jekyll-theme'

4. 테마를 찾고 _config.yml 파일 가져오기 및 수정하기.
- 원하는 테마의 _config.yml 파일에서 raw(소스)를 가져옴
- 내 github에 _config.yml 생성후 raw를 넣기.
- 소스에 아래 추가(or 주석제거).
(이는 remote_theme을 지정하는 설정이며 GitHub의 OWNER/REPOSITORY 의 형식으로 이루어집니다. 아래는 mmistakes라는 owner의 so-simple-theme라는 저장소의 Jekyll 테마를 가져오겠다는 뜻입니다.)
'
remote_theme : mmistakes/so-simple-theme (주석제거) --추가
url          : "https://hui0222.github.io" # 위에서 생성했던 나의 hui0222.github.io 넣어주기.
baseurl      : "" #빈값으로 두기
'

5.index.html 파일 생성하기.
- 아래와 같이 index.html파일을 생성 후 입력해 줍니다.
```html
---
layout: home
author_profile: true
---
```

6. _posts에 글쓰기.
- 새파일 생성시 'YYYY-MM-DD-name-of-post.md' 형식으로 파일 생성
(ex)_posts/2020-07-12-first-post.md
- 생성내용
```html
---
title: "제목"
date: 2020-07-12 23:26:28 -0400 #날짜
categories: fastlane dev study #카테고리
---
내용 [git-join][git-join]
[git-join] : https://github.com
[git-theme]: https://github.com/topics/jekyll-theme
```

[git-join] : https://github.com
[git-theme]: https://github.com/topics/jekyll-theme
