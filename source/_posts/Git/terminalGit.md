---
title: 
date: 2020-01-26 15:18:10
categories:
    - Git
---

<pre>

일단 기본적으로 terminal 에서 git을 사용하는 것에 익숙해지기로 했다.

내가 사용한 방법은 로컬에 프로젝트를 만들고,
remote repo를 만든후 두개를 연결해서
master 브랜치에다만 push를 한 것이다.
다른 방법이나 사용법들은 추가적으로 사용할 때마다 업로드 하도록 하겠다.

1. 로컬에 프로젝트를 만든다.
2.  git init : 해당 프로젝트 디렉터리에서 이닛을 한다.
3.  git config (--global) user.name "내이름"
    git config (--global) user.email "내 이메일"
// 글로벌은 전역이고 안하면 그냥 개별임.
4.  git remote add origin remoteRepo의 주소(" 쌍따옴표는 넣지 않는다.)
5.  git push -u origin master : 처음 푸시할 경우 -u 라는 옵션을 넣어주어야 하는 듯 하다.

6. git add . (. 이라는 옵션은 전체다 스테이징 하겠다는 뜻인 듯)
7. git commit -m "커밋 메세지 넣기"
8. git push origin master : 리모트에 푸시하기.

이다.

이후에는 6~8 단계 위주로 사용했는데,
점점 더 늘려야 겠다.

</pre>

## Reference

