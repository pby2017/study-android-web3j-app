# android app과 geth 연동 (계정 주소 목록, 송금 기능)

Web3j 라이브러리와 Android 앱을 연동하는 학습 내용

## 시작하기

### 준비사항

1. [Android Studio 3.0](https://developer.android.com/studio)
2. [geth & tools 1.7.3](https://geth.ethereum.org/downloads/)

## 테스트 (방법)

1. Geth (dev mode & rpcport except 8545) 실행
```
geth --datadir testNode1 --networkid 9865 --rpcapi "personal,db,eth,net,web3,miner" --rpc --rpcaddr "0.0.0.0" --rpcport 8544 --rpccorsdomain "*" --nodiscover --maxpeers 0 --dev console
```
2. Android Studio에서 앱 빌드 후 기기에 설치
3. IP 주소 입력 (아래 예시 참고)
```
http://{geth 실행 기기 IP}:{geth --rpc port 번호}
ex) http://192.168.0.5:8544
```
4. 지갑주소 목록 확인 및 송금
```
트랜잭션이 생성되면 이더/비밀번호 입력 칸이 공백으로 설정됨
```

## UI
```
※ 편의상 첫 번째 계정은 비밀번호를 공백으로 생성했기 때문에 이더 전송 트랜잭션 생성시 비밀번호 입력란을 공백으로 두었음.
※ 송금 이후 이더 결과 확인은 화면을 누른 상태로 아래로 내렸다가 손을  새로고침하여 확인할 수 있음.
※ 트랜잭션 생성은 송금 이더 입력 칸과 비밀번호 입력칸이 공백으로 변경되는 것으로 확인할 수 있음.
```
<img src="https://github.com/pby2017/study-android-web3j-app/blob/master/image/sample.gif" width="288" height="512">
