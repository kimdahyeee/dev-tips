
### 이미 리모트에 push 된 commit 변경하기

---

CASE1. `commit`하지 않아야할 파일인데, 커밋 하고 `push` 까지 해버린 경우

CASE2. `commit` 내용을 잘못 입력한 경우


#### `rebase` 하여 `commit` 조작


##### 🙅‍♀ 싫어요 !

```
rebase -i
```

시도했지만 출력에 커밋 로그가 보여지지 않음

👉 `noop`이라는 단어만 보여짐

👉 해당 명령어 호출 때, `commit` range를 지정하지 않으면 `noop` 출력이 된다고 함


##### 🙆‍♀ 좋아요 !

```
rebase -i HEAD~1
```

👉 범위 지정하여 `rebase` 후 강제 push

##### 주의할 사항

> 다른 사람과 공유 중인 브랜치는 절대!! `rebase` 하지 말 것