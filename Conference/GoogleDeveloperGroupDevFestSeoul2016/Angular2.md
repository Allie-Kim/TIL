# Angular2 어디까지 왔을까
[한장현](http://han41858.tistory.com)  
삼성SDS4년 -> 프리랜서, 번역(Angular2), 개인프로젝트

현재 2.2.0
Angular2부터 SemVer사용, but 제대로 안 지킴  
[Major].[Minor].[Path] = [호환되지 않는 API].[호환되면서 기능 변경,추가].[버그수정]

### 장애물1
* 버전 업데이트 너무 빠름, Minor와 Patch 병행 업데이트

### 장애물2: 사용하는 언어
* **Typescript**, Javascript, Dart 지원
* Typescript, Dart를 써야 하느냐? 
Angular2에서 Typescript 선호  
Javascript을 사용하면 구현하기 복잡하고 코드가 길어짐  
-> Typescript를 쓰는게 좋겠음

### 장애물3: 새로운 툴, 개발 방식의 변화
* [Angular CLI](https://github.com/angular/angular-cli) 베타. 아직 불안정

### 작은 장애물: 문법 변화
* 디렉티브 많이 변화함
* data binding 달라짐(one way binding이 기본)
* @ngModule 새로 생김. 중요.

### 장점1: 속도
빠르다고 했던 Angular Directive with react 보다 Angular2가 좀 더 빠르다(고 Angular에서 발표)

### 장점2: 체계적인 개발 방법
* Mobile oriented
* Modern browsers only
* Dynamic loading, server-side loading 등..

### 결론: Angular2 써야 할까?
* 아직 애매하긴 하지만 생산성(체계적인 프로젝트 관리+최신기술도입)을 위해서 쓸만함.
* 발표자는 아직 안 쓰겠다고..ㅎㅎ