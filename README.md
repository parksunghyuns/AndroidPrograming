# git명령어와 markdown명령어 정리과제
### 학번 : 2014261111
### 성명 : 박성현
### 과목명 : 안드로이드프로그래밍
### 시간 : (수요일)15:00~17:50
### 담당교수님 : 진용화교수님
---
---
##git 명령어##

git명령어|기능
---|---
git add|<파일>
git commit -m|“<메시지>”
git add -p |[<파일> [<파일> [기타 파일들…]]]
git add -i|수정되고 추적되는 파일의 변경 사항 스테이징하기
git add -u |[<경로> [<경로>]]수정되고 추적되는 모든 파일의 변경 사항 커밋하기
git commit -m “<메시지>” -a| 작업 트리의 변경 사항 돌려놓기
git checkout HEAD <파일> [<파일>]|커밋되지 않고 스테이징된 변경 사항 재설정하기
git reset HEAD <파일> [<파일>]|마지막 커밋 고치기
git commit -m “<메시지>” - -amend|이전 커밋을 수정하고 커밋 메시지를 재사용하기

---
---

###마크다운 문법입니다.

•큰제목: 문서 제목 This is an H1 ============= This is an H1 
•작은제목: 문서 부제목 This is an H2 ------------- This is an H2
•글머리: 1~6까지만 지원
# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6
####### This is a 7.





####마크다운 문법의 장단점은 다음과 같습니다.
장점
문법이 단순해서 배우기 쉽고 쓰기도 쉽습니다.
html 문서로 변환하지 않아도 그 자체로 충분히 읽을 수 있습니다.
다양한 도구들을 이용해 손쉽게 html 문서로 변환될 수 있습니다.
inline HTML을 지원하기 때문에 html의 풍부한 기능을 그대로 사용할 수 있습니다.
단순한 텍스트이기 때문에 어떤 운영체제나 편집기에서도 작성할 수 있습니다.
단순한 텍스트이기 때문에 용량이 매우 작고 검색속도가 빠릅니다.
html로 변환되기 때문에 문서 호환성이 좋습니다.

단점
문법이 너무 간단하고 오래되어서 테이블 등 새로운 서식에 대한 요구사항을 반영하지 못하고 있습니다.
새 표준이 나오지 않아 PHP Markdown Extra, Multimarkdown, Github Flavored Markdown(GFM) 등으로 파편화가 진행되고 있습니다.
그림파일을 삽입/관리하기가 어렵습니다.



### 마크다운 
마크다운 문법 Syntax
기본 마크다운 문법 (존 그루버) ![사진](C:\Users\user\Desktop\캡처.PNG)


