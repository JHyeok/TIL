# Git 원격 저장소의 파일명 대소문자 변경

같은 이름의 파일명을 대소문자만 변경하려고 할 경우, 대소문자를 로컬에서 변경하고 원격 브랜치에 Push 하더라도 변경된 내용이 원격 브랜지에 반영되지 않는다.

그런 경우 로컬 디렉토리에서 파일의 위치에 직접 가서 아래 명령어로 변경해야 한다.

```
# gRPC.md의 파일명을 grpc.md로 변경
git mv --force gRPC.md grpc.md

# 파일명 변경이후 변경 내용에 대한 처리
git commit

git push
```

원격 브랜치에 대소문자가 변경된 것을 확인할 수 있다.

