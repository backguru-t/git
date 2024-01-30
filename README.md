# git
git management

## 다수의 원격 저장소 연결

```bash
git remote -v
origin git@xxxx (fetch)
origin git@xxx (push)
```

연동하고자 하는 원격 repository를 **git remote add [단축이름] [저장소주소]** 형식으로 입력하여 추가한 후 **git remote -v** 로 추가 여부를 확인한다.
아래의 예시는 github라는 단축이름으로 github 저장소를 추가하는 모습이다.

```bash
git remote add github  https://github.com/backguru-t/openai.git
git remote -v
github  https://github.com/backguru-t/openai.git (fetch)
github  https://github.com/backguru-t/openai.git (push)
origin  git@xxx (fetch)
origin  git@xxx (push)
```

이제 다음과 같이 두 개 이상의 저장소에 push할 수 있다.
```bash
git push origin master
git push github master
```

## 원격 저장소 삭제
아래의 방식으로 원격 저장소를 삭제할 수 있다. **github** 원격 저장소를 삭제해 보자.

```bash
git remote remove github
```

**Reference**: https://git-scm.com/book/en/v2


