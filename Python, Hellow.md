# Python, Hellow

## 파이썬의 종류와 가능성

### 2.x vs 3.x

### PEP?

Python Enhancement Proposal

## 작업 환경 구축 하기

### 홈브류 설치

ruby -e "$ (curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)”

버전 확인 $ brew -v

업데이트 $ brew update

### pip 설치

$ sudo easy_install pip

설치 확인

$ pip

### 파이썬 3.x

### 라이브러리 설치 방법

Python 2.x
pip install 
ex) pip install numpy

Python 3.x
pip3 install 
ex) pip3 install numpy

#### 설치 관련 오류..

matplotlib 1.3.1 requires nose, which is not installed.
-> matplotlib를 설치해야 한다.

could not install packages due to an environmenterror errno 13
-> 폴더에 접근 할 권한이 없다..

could not install packages due to an environmenterror errno 1
-> --user를 붙여 주어야 한다.
  ex) sudo pip install <LibName> ——user

### 주요 기본 Lib

(대소문자 구분 안함)

numpy

pandas

opencv

openpyxl

matplotlib

PyQt5

### 라이브러리 목록 확인 하기

[pip list를 수행 해주면 된다.](https://zetawiki.com/wiki/Python_%EC%84%A4%EC%B9%98%EB%90%9C_%EB%AA%A8%EB%93%88_%EB%AA%A9%EB%A1%9D)

## VS Code로 파이썬 시작하기

### 설치 하기

인터넷에서 다운 받음

### 초기설정하기

파이썬 팩 설치
작업 환경 설정
테스트 시작하기

## python 기초 문법 (심화 내용 x)

### 기본 문법

### 자료형

컬렉션 리터럴
[ ... ]로 감싸져 있으면 list자료형
( ... )로 감싸져 있으면 tuple자료형
{ 키:값, ... }로 감싸져 있으면 dictionary자료형
{ ... }로 감싸져 있으면 set자료형

### 분기

### 반복

### 권장 코딩 스타일

Python Enhancement Proposal 8 (PEP 8)은 파이썬 코딩 스타일에 대한 가이드를 제시하고 있다. PEP 8은 2001년 귀도 반 로썸에 의해 처음 제안되었
으며, [python.org 의 PEP 링크](https://www.python.org/dev/peps/pep-0008/)에 자세히 소개되어 있다. 파이썬 프로그래머들은 일반적으로 이러한 PEP 8 코딩 스타일에 따라 프로그래밍을 하고 있는데,
이러한 일관된 코딩 스타일을 적용하는 것은 자신의 코드를 명료하게 할 뿐만 아니라 특히 다른 개발자 혹은 커뮤니티간 코딩을 공유할 때 매우 효율적이다. 
아래는 PEP 8 의 중요한 부분에 대한 요약이다.

## 업무 자동화 프로젝트, with telegram

### Git 주소

https://github.com/Jusuhun/PytionTest.git

### 사용 라이브러리

python-telegram-bot

pandas

### 텔레그램 환경 구축하기

라이브러리 설치

### Bot 작동 구성.

### 기본 이벤트 설명

### 커맨드 추가 및 관리

### 커멘드 UI 추가.

### 참고

[30분 만에 텔레그램 봇 만들기](https://steemit.com/kr-dev/@maanya/30)

[텔레그램 로봇, 공식 API로 만들기 (파이썬, 구글 앱 엔진)](https://bakyeono.net/post/2015-08-24-using-telegram-bot-api.html)

[Code snippets](http://velopert.com/)

[Telegram Bot API 정리](https://trifleidea.blogspot.com/2018/04/ifttt-telegram-bot-api.html)

## 가계부, with telegram and SQLite.

### 참고

[파이썬으로 데이터베이스 처리하기](https://code.tutsplus.com/ko/tutorials/database-handling-in-python--cms-25645)

[파이썬으로 배우는 알고리즘 트레이닝](https://wikidocs.net/5332)

[pandas data flame 변형](http://nittaku.tistory.com/124)

## 추가 자료

### python 활용

[파이썬으로 도전하는 업무 자동화.](https://www.youtube.com/watch?v=w7Q_eKN5r-I&t=2s)

[파이썬을 배우는 최고의 방법](https://nolboo.kim/blog/2014/08/10/the-best-way-to-learn-python/)
