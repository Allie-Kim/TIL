# Electron: 웹 개발자들을 위한 Desktop Application 제작
Speaker: 김성훈 [스튜디오씨드코리아](https://www.protopie.io/) CTO  
[Electron Korea](http://www.meetup.com/electron-kr)

### 1.Electron 101

* 검색팁: github electron XXX (electron이 과학용어라)

### 2.
* why electron? 초기는 Cloud(SaaS)로 개발 -> 지역적 packet loss, 보안 

### 3.Design Pattern
* Electron 소스 보기가 쉬움 -> 소스를 보호하기 위해 많은 로직을 Backend로 보냄
* [github에 소스](https://github.com/ScottyKim/NaverDeview2016-Electron-Demo)

#### Command Pattern
* undo/redo: command를 큐에 담아 꺼내 쓴다

#### Front-End Framework
* not React, AngularJS but 직접
* ES6/7, typescript

###
Chrome Debugger, Devtron

### 5.Build & Deploy
* 소스 보호: 유료 EncloseJS 사용 - 노드 바이너리화
* dev vs prod 나눠서 빌드와 테스트
* 빌드: electron-builder 사용
* 배포: 강제(auto) 업데이트 -> 지역별 다운로드 속도 다름 -> CDN 구축

### 6.Summary
* Web개발자 Desktop APP 쉽게
* 소스 보호 대비 필요

### 7.Q&A
* 브라우저에서는 지원되는데 electron에서는 지원 안되는거?(like HTML5 notification)  
대체할 수 있는 api가 개발되고 있다더라.. 그냥 기다려라

* UI가 어떤 웹 엔진을 사용하는지?  
일렉트론에 chronium 베이스라서 크롬 설치하지 않아도 된다.