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