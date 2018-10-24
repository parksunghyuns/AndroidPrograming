# AndroidPrograming

기본적인 사용법

아래 명령어에서 [ ]는 선택적인 매개변수를 의미한다.

새로운 파일을 추가하거나 존재하는 파일 스테이징하고 커밋하기
h1-기본적인 사용법
git add <파일>

git commit -m “<메시지>”

파일의 일부를 스테이징하기
git add -p [<파일> [<파일> [기타 파일들…]]]

add 명령에서 Git 대화 모드를 사용하여 파일 추가하기
git add -i

수정되고 추적되는 파일의 변경 사항 스테이징하기
git add -u [<경로> [<경로>]]

수정되고 추적되는 모든 파일의 변경 사항 커밋하기
git commit -m “<메시지>” -a

작업 트리의 변경 사항 돌려놓기
git checkout HEAD <파일> [<파일>]

커밋되지 않고 스테이징된 변경 사항 재설정하기
git reset HEAD <파일> [<파일>]

마지막 커밋 고치기
git commit -m “<메시지>” - -amend

이전 커밋을 수정하고 커밋 메시지를 재사용하기
git commit -C HEAD - -amend


-----------------브랜치 문서입니다.
브랜치

지역 브랜치 목록 보기
git branch

원격 브랜치 목록 보기
git branch -r

지역과 원격을 포함한 모든 브랜치 목록 보기
git branch -a

현재 브랜치에서 새로운 브랜치 생성하기
git branch <새로운 브랜치>

다른 브랜치 체크아웃하기
git checkout <브랜치>

현재 브랜치에서 새로운 브랜치 생성하고 체크아웃하기
git checkout -b <새로운 브랜치>

다른 시작 지점에서 브랜치 생성하기
git branch <새로운 브랜치> <브랜치를 생성할 위치>

기존의 브랜치를 새로운 브랜치로 덮어쓰기
git branch -f <기존 브랜치> [<브랜치를 생성할 위치>]

브랜치를 옮기거나 브랜치명 변경하기
git checkout -m <기존 브랜치> <새로운 브랜치>

<새로운 브랜치>가 존재하지 않을 경우
git checkout -M <기존 브랜치> <새로운 브랜치>

무조건 덮어쓰기
다른 브랜치를 현재 브랜치로 합치기
git merge <브랜치>

커밋하지 않고 합치기
git merge - -no-commit <브랜치>

선택하여 합치기
git cherry-pick <커밋명>

커밋하지 않고 선택하여 합치기
git cherry-pick -n <커밋명>

브랜치의 이력을 다른 브랜치에 합치기
git merge - -squash <브랜치>

브랜치 삭제하기
git branch -d <삭제할 브랜치>

삭제할 브랜치가 현재 브랜치에 합쳐졌을 경우에만
git branch -D <삭제할 브랜치>

삭제할 브랜치가 현재 브랜치에 합쳐지지 않았어도

#git 이력 문서입니다.
Git 이력
모든 이력 보기
git log

변경 사항을 보여주는 패치와 함께 로그 표시하기
git log -p

1개의 항목만 보이도록 로그 개수 제한하기
git log -1

20개의 항목과 패치만 보이도록 로그 제한하기
git log -20 -p

6개월 동안의 커밋 로그 보기
git log - -since=”6 hours”

이틀 전까지의 커밋 로그 보기
git log - -before=”2 days”

HEAD보다 세 개 이전의 커밋 로그 보기
git log -1 HEAD-3

git log -1 HEAD^^^

git log -1 HEAD~1^^

두 지점 사이의 커밋 로그 보기
git log <시작 지점>…<끝 지점>

시작 지점이나 끝 지점은 커밋명, 브랜치명, 혹은 태그명이 될 수 있고 조합하여 사용 가능하다.
각 항목의 로그 이력 한 줄씩 보기
git log - -pretty=oneline

각 항목마다 영향 받은 줄의 통계 보기
git log - -stat

커밋할 시점의 파일 상태 보기
git log - -name-status

현재 작업 트리와 인덱스의 차이점 보기
git diff

인덱스와 저장소의 차이점 보기
git diff - -cached

작업 트리와 저장소의 차이점 보기
git diff HEAD

작업 트리와 특정 위치 간의 차이점 보기
git diff <시작 지점>

시작 지점은 커밋명 or 브랜치명 or 태그명이다.
저장소의 두 지점 사이의 차이점 보기
git diff <시작 지점> <끝 지점>

차이점의 통계 보기
git diff - -stat <시작 지점> [<끝 지점>]

파일의 커밋 정보 줄 단위로 보기
git blame <파일>

파일의 줄 단위의 복사, 붙여 넣기, 이동 정보 보기
git blame -M <파일>

파일의 줄 단위의 이동과 원본 파일 정보 보기
git blame -C -C <파일>

로그에서 복사와 붙여 넣은 정보 보기
git log -C -C -p -1 <특정 지점>


##마크다운 문법입니다.

  마크다운 문법이란?
마크다운 문법은 존 그루버(John Gruber)와 아론 스워츠(Aaron Swartz)가 메일의 글쓰기 형식에서 영감을 받아 만들었으며 자신의 블로그에 마크다운 문법 소개와 함께 python으로 만든 html 변환기(마크다운 문서->html)를 올림으로써 알려지게 되었습니다. 위에서 보는 것 같은 여러 장점들로 인해 문법은 빠르게 확산되었고 지원 툴들도 여럿 만들어 졌지만 안타깝게도 존 그루버가 약 10년전 문법을 제시한 이후 별다른 새 표준을 제시하지 않아서 마크다운 표준 자체는 정체되어 있는 상태입니다. 현재는 각 커뮤니티 등에서 이를 조금씩 발전시켜서 새로운 문법을 만들고 있지만 때문에 권위있는 표준없이 새 표준이 난립하는 파편화가 진행되고 있는 문제 역시 안고 있습니다. 마크다운 문서는 대체로 .md나 .markdown과 같은 확장자를 사용하지만 근본이 txt인지라 메모장에서도 잘 열립니다.

마크다운 문법의 장단점은 다음과 같습니다.

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


마크다운 문법 Syntax
기본 마크다운 문법 (존 그루버)

사진첨부가 안돼서 이메일로 보냅니다.





