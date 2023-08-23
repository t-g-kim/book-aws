# Introduction

gitbook instal
```bash
$ gitbook serve
```

gitbook init
```bash
# 해당 디렉토리에서
$ gitbook init
```

local server start
```bash
$ gitbook serve

# ...
# Starting server ...
# Serving book on http://localhost:4000
```

목차 생성 파일
Summary

SUMMARY.md 예시
```text
* [Introduction](README.md)  
  
* [Part I](part1/README.md)  
	* [Writing is nice](part1/writing.md)  
	* [GitBook is nice](part1/gitbook.md)  
* [Part II](part2/README.md)  
	* [We love feedback](part2/feedback_please.md)  
	* [Better tools for authors](part2/better_tools.md)  
```

Gitbook 디렉터리 구조
```bash
├── book.json            # 기본 GitBook구성 데이터(선택)  
├── README.md            # 책 소개(필수)  
├── SUMMARY.md           # 목차 참조(선택)  
├── GLOSSARY.md          # 용어 정리(선택 : 직접파일 성생필요)   
├── part-1/  
|   ├── README.md  
|   └── something.md  
└── part-2/  
    ├── README.md  
    └── something.md  

# book.json에서는 플러그인을 세팅 할 수 있다.
```

# 배포
1. repository를 생성
2. gh-pages 브랜치를 생성
3.  _books/ 디렉터리를 반영하면 t-g-kim.github.io/repo-name 으로 gitbook이 반영
```bash
# ../book-algorithm/ 에서 파일생성 및 gitbook serve 했다고 가정   
$ cp -R ../book.aws/_book/* . #*  
$ git clean -fx node_modules  
$ git clean -fx _book  
```
배포 요약
- 해당 디렉토리 이동  
cp -R ../book.aws/_book/* .  
git clean -fx node_modules   
git clean -fx _book  

git add .  
git commit -m"message"  
git push origin gh-pages  