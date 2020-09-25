# 외부 Jenkins 와 Openshift Cluster 연결 방법

- Jenkins 가 이미 설치되어 있다면 아래 스텝들을 진행한다.

## Step 1 : Jenkins 에 Openshift Client Plugin 설치
 
Manage Jenkins => Manage Plugins => Available Tab => Filter 로 "Openshift" 입력후 아래 설정을 진행

1. 플러그인 선택
     - Openshift Client
     - Openshift Login
     - Openshift Sync
2. Download now and install after restart 선택
3. Jenkins 재시작
4. 재시작후 설치된 플러그인에 위 플러그인들이 제대로 들어갔는지 확인

## Step 2 : Global Tool Configuration 설정

Manage Jenkins => Global Tool Configuration 으로 이동해 아래 설정을 진행

1. Openshift Client Tools 
    - Name : oc
    - Install automatically : 체크
    - Add Openshift Client Tools 클릭 후 "Extract *.zip/*.tar.gz" 선택
    - Openshift About 페이지에서 Openshift 버전 확인 후 https://mirror.openshift.com/pub 에서 알맞은 Client 의 URL 을 복사
    - Download URL for binary archive : https://mirror.openshift.com/pub/openshift-v3/clients/3.11.0-0.32.0/linux/oc.tar.gz
    - Apply 버튼 클릭  
2. JDK Installations (Openshift 플러그인 테스트용)

```console
 $ sudo apt-get update
 $ sudo apt-get install openjdk-8-jdk
 $ sudo vi /etc/environment
 JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64"
 $ source /etc/environment
 $ echo $JAVA_HOME
```
