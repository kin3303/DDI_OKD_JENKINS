# 외부 Jenkins 와 Openshift Cluster 연결 방법

- Jenkins 가 이미 설치되어 있다면 아래 스텝들을 진행한다.

## Step 1 : Jenkins 에 Openshift Client Plugin 설치
 
1. Manage Jenkins => Manage Plugins => Available Tab => Filter 로 "Openshift" 입력
2. 아래 플러그인 선택
     - Openshift Client
     - Openshift Login
     - Openshift Sync
3. Download now and install after restart 선택
4. Jenkins 재시작
5. 재시작후 설치된 플러그인에 위 플러그인들이 제대로 들어갔는지 확인

## Step 2 : Global Tool Configuration 설정

1. Manage Jenkins => Global Tool Configuration
   1. Openshift Client Tools 항목을 찾아 아래 내용을 반영
     - Name : oc
     - Install automatically : 체크
     - Add Openshift Client Tools 클릭 후 "Extract *.zip/*.tar.gz" 선택
     - Openshift About 페이지에서 Openshift 버전 확인 후 https://mirror.openshift.com/pub 에서 알맞은 Client 의 URL 을 복사
     - Download URL for binary archive : https://mirror.openshift.com/pub/openshift-v3/clients/3.11.0-0.32.0/linux/oc.tar.gz
     - Apply 버튼 클릭  
