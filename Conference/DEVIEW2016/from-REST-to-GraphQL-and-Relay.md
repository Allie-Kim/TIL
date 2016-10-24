# REST에서 GraphQL과 Relay로 갈아타기
speaker: 이정우 [에디켓](https://ediket.com/) CTO  
Q&A는 22살 (full stack) 개발자가 진행했는데 내공이 엄청남..

### 1. REST API

#### REST API 한계
* [필드제한(sparse fieldset)](http://jsonapi.org/format/#fetching-sparse-fieldsets) 깔끔하게 어려움
* 필드타입이 없음
* side effect: 동기화 문제
* Query Hell
* 라이브러리 부족

### 2. GraphQL
GraphQL(2015) by facebook

#### REST와 GraphQL 비교하기 

* 공식문서 아주 잘 되어있으니 참조
* 쿼리 언어다
* Different Request

#### GraphQL 구현 예제

* 클라이언트에서 lokka 라이브러리 사용
* GraphiQL: 자동문서화와 Type Inspection이 가능한 강력한 툴

### 3. Relay
Realy (2015) from facebook
GraphQL의 확장..

* React와 함께 엄청난 시너지 효과

#### Relay 소개
* Node
* Connection: 다수의 Node를 가져올 때 사용. pagination에 특화돼있음
컴포넌트마다 필요한 data가 다른데 

#### React Relay

#### Mutation in Relay

#### REST에서 GraphQL Relay로 갈아타기


Q&A
* Redux랑도 연동이 잘 되는지?

* 어느 서버 프레임웍 쓰나? 장점/단점?
어썸 시리즈 어썸 GraphQL
리씽크디비?

* 클라이언트에서 React가 아닌 타 프레임웍(Angular)해도 잘 연동이 되는지?
충분히 가능할 것 같다.

* GraphQL을 앱에도 적용 괜찮은지?
http에 국한 된 것이 아니라 ** 프로토콜임.

* sql에서 어떻게 최적화
GraphQL에서 서버 구현체가 페잇

* GraphQL에서 null이나 generic object 지원을 안 하는데 어떻게 하셨는지?
두가지 방법 있는데
다 스키마에 추가해서 사용했음.