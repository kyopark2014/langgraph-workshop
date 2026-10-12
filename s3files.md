# Amazon S3 Files

langgraph-workshop은 Amazon S3 Files를 사용하지 않습니다.

- AgentCore Runtime 세션 저장은 managed `sessionStorage`(`/mnt/workspace`, `networkMode: PUBLIC`)입니다.
- ECS task definition은 S3 Files 볼륨을 마운트하지 않습니다. 태스크 DB는 컨테이너 디스크의 `application/data/tasks.db`입니다.
- `installer.py`는 S3 Files 파일 시스템·access point·mount target을 만들지 않습니다.
- 이전에 배포된 S3 Files 리소스가 있으면 `uninstaller.py`가 삭제합니다.
