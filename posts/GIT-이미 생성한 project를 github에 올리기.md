### 이미 생성한 project를 gitHub에 올리기

---

1. `cd {project 위치}`

2. `git init`

3. `git add .`

4. `git commit -m "init"`

5. `git remote add origin "깃 주소"`

6. `git push origin master`

#### 5 ~ 6 과정에서 문제 발생!

remote 에 readME.md 파일을 생성해서 push가 안되는 문제가 생겼다.

에러 문구는 `pull`을 받으라는 ~

`pull`을 시도했지만, 실패 😅
아래는 `pull`을 시도 했을 때 만난 에러 문구

```
fatal: refusing to merge unrelated histories
```

구글링을 해보니 '공통된 커밋 포인트'가 없어서 나는 에러라고 한다.

나는 pull을 강제로 받는 방식을 사용해 해결하였다. 😉

```
git pull origin master --allow-unrelated-histories
```
