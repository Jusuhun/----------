# GitBook

## 설치

GitBook을 설치 하기 위해는 Node.js가 기본적으로 설치되어 있어야 합니다. 없는 경우에는 brew로 설치합니다.
``` 
brew install node
```

먼저 gitbook-cli를 설치한다.
```
npm install gitbook-cli -g
gitbook --version
```

전자책 포맷과 PDF를 생성하려면 ebook-convert 명령어가 필요합니다.
```
brew cask install calibre
```

---

## 사용방법

### 3.1 첫 GitBook 프로젝트 만들기
아래 명령어로 책의 boilerplate를 생성합니다. 기본적으로 README.md와 SUMMARY.md가 생성됩니다. 
```
gitbook init
```

로컬환경에서 gitbook 웹 서버를 띄워 브라우저에서 확인 할 수 있습니다. localhost:4000로 연결 해야 한다.
```
gitbook serve
```

생성된 기본적인 디렉토리 구조는 아래와 같다.
```
.
├── book.json            # 기본 GitBook구성 데이터(선택)
├── README.md            # 서적 소개(필수)
├── SUMMARY.md           # 목차 참조(선택)
├── GLOSSARY.md          # 용어 정리(선택 : 직접파일 성생필요) 
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

### 3.2 eBooks과 PDF 생성하기 

```
gitbook build
# gitbook build ./mybook --gitbook=2.0.1

gitbook pdf
# gitbook pdf . ./mybook.pdf

gitbook epub
# gitbook epub . ./mybook.epub

gitbook mobi
# gitbook mobi . ./mybook.mobi
```

[참고1](https://advenoh.tistory.com/1)

[참고2](https://pinedance.github.io/blog/2018/10/04/build-eBook-with-gitbook-cli)

[참고3](https://blog.chulgil.me/how-to-make-blog-using-github-5/)
