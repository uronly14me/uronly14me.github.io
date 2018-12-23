---
layout: post
title: 깃허브 https로 사용하기
modified:
categories: common
description:
tags: []
image:
  feature:
  credit:
  creditlink:
comments:
share:
date: 2018-12-23T08:56:49-05:00
---

깃허브를 https로 클론하여 사용할 경우가 있다
```
git clone https://github.com/username/repo.git
```

이런 경우에 푸시를 하면 아래와 같은 에러가 난다.
```
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

이것은 https로 github에 접근할때 아이디와 비밀번호가 없어서 나는 에러다. 아래와 같이 해주면 해결된다. 아이디와 비밀번호를 넣어준다.
```
git remote set-url origin https://username:password@github.com/username/repo.git
```

이 경우 개인 컴퓨터에서만 하기를 추천하며 어지간하면 ssh를 통해 접근하는 것이 좋겠다.

참고자료
[github에서 username과 password를 요구할 경우](https://stackoverflow.com/questions/6565357/git-push-requires-username-and-password)