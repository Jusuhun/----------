# HomeBrew

[팁](https://tutorialpost.apptilus.com/posts/tools/homebrew-for-mac/)
명령어|설명|비고
-|-|-
brew install [패키지명] | 패키지 설치
brew uninstall [패키지명] |패키지 삭제
brew remove --force --ignore-dependencies $(brew list) | Homebrew로 설치한 모든 package 일괄 삭제 방법
brew upgrade [패키지명]|패키지 업그레이드 | 패키지명 미입력시, 전체 업데이트가 된다고 한다.
brew search [패키지명]|패키지 검색하기
brew list|설치된 패키지 목록 보기
brew update|HOMEBREW 업데이트|가끔씩 실행하자. 그렇지 않으면 예전 버전으로 설치가 될 수 있다.
