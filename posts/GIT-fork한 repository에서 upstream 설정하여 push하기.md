### repository fork 후 push 하기

참고 : [Git Forks and Upstreams: How-to and a cool tip](https://www.atlassian.com/git/tutorials/git-forks-and-upstreams)


**위의 사이트를 참고하여 그~대로 했다😎**


1. remote에 upstream 추가
```
git remote add upstream https://github.com/Study-Java-Together/study-http.git
```

2. git remote upstream 정상 추가 되었는지 확인
```
git remote -v
```

3. upstream repository fetch
```
git fetch upstream
```

4. push 하기
```
git push upstream study/kimdahyeee
```

> `git push`하는 경우에 `refusing to merge unrelated histories` 에러가 떨어지는 경우가 있다.
> 나는 보통 readME.md 파일 때문에 나는 경우가 많았다.
> 당황하지 말고, `git pull origin 브런치명 --allow-unrelated-histories` 해당 옵션을 통해 `pull` 받고, `merge`한 뒤 `push`해 주자.
