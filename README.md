# 외부 Jenkins 와 Openshift Cluster 연결 방법

- Jenkins 가 이미 설치되어 있다면 아래 스텝들을 진행한다.

## Step 1 : Jenkins 에 Openshift Client Plugin 설치

```
1. Manage Jenkins => Manage Plugins => Available Tab => Filter 로 "Openshift" 입력
2. 아래 플러그인 선택
     - Openshift Client
     - Openshift Login
     - Openshift Sync
3. Download now and install after restart 선택
4. Jenkins 재시작
5. 재시작후 설치된 플러그인에 위 플러그인들이 제대로 들어갔는지 확인
```



