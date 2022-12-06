---
title: local에 연결된 git remote 백업, 변경하기
feed: show
date : 2022-04-01
tags : [ git, 📝️/🌲️ ]
comments: true
---

1. 기존 remote repository 기준 pull하고 전체 push
``` shell
git pull
git add .
git commit -m "the last push for cleansing repository"
git push
```

2. 기존 remote repository 제거
``` shell
git remote remove origin
```

3. 새 remote repository 추가
``` shell
git remote add origin https://github.com/깃헙계정명/리포지토리이름
```

4. 새 remote repository가 등록되었는지 확인
``` shell
git remote -v
```
- origin으로 새로운 remote 주소가 등록되어 있다면 성공!

_끝_