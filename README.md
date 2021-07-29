# MQTT-Project-Dashboard
<MQTT 기반 메시지 서버의 성능 모니터링 시스템>의 웹 서비스 파트입니다.

전체 프로젝트 배경과 설명은 첨부파일-최종 보고서에서 확인 가능합니다.


## 1. 프로젝트 전체 구조
<img src = "https://user-images.githubusercontent.com/38847724/127315703-15176e0d-dbb7-4b4c-a5c6-508073f110a0.png" width="90%" height="90%">


## 2. 그 중 ③Dashboard Web System 파트
<img src = "https://user-images.githubusercontent.com/38847724/127315778-428ebada-3d32-43bf-8d11-196989210cbd.png" width="90%" height="90%">


## 3. 실시간 성능 데이터 출력 웹 서비스(node-server)
 본 프로젝트의 모니터링 시스템은 주기적으로 웹 페이지에 실시간으로 성능 정보를 출력합니다.
 
 이를 위해 서버 측에서는 MySQL DB에 저장된 데이터를 주기적으로 읽어와 mosquitto MQTT broker를 통해 웹 브라우저의 Javascript 코드와 연계하여 웹 페이지에 출력합니다.
 
- DB에서 가져온 JSON 형태의 레코드(ex. performance table)
<img src = "https://user-images.githubusercontent.com/38847724/127317714-b5f9a206-b1ee-48b7-a241-c7c41addebf8.png" width="70%" height="70%">
 
- JSON 형태의 레코드를 리액트의 차트에 따라 String 형식으로 가공한 예시
<img src = "https://user-images.githubusercontent.com/38847724/127317782-f5d38760-dc05-433d-8fb5-098bed93ae06.png" width="60%" height="60%">


## 4. 대시보드 웹 시스템(react-client)
 서버로부터 받은 성능 정보를 다양한 차트 형식으로 운영자에게 출력하는 서비스입니다.

- 대시보드 UI 1 - 타겟 메시지 서버 성능 정보
![image](https://user-images.githubusercontent.com/38847724/127319346-975d3ca6-62bb-4dda-a790-8041eb8048df.png)

- 대시보드 UI 2 - 메시지 트래픽 정보
![image](https://user-images.githubusercontent.com/38847724/127319576-7c3ba2ec-40e5-4e6a-b289-fde94d71f2a5.png)

- 대시보드 UI 3 - 토픽 트리
![image](https://user-images.githubusercontent.com/38847724/127319630-7cf72b14-78b2-4b44-8b10-59e9e19377b9.png)
