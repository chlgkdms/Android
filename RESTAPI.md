# RestApi

: REST 아키텍처의 제약 조건을 준수하는 API를 뜻합니다

![post-thumbnail](https://velog.velcdn.com/images/somday/post/2a7df2da-2a3c-44af-b059-ee03efc125ef/restapi-image.png)

- 자원을 이름 (자원의 표현) 으로 구분하여 해당 자원의 상태 (정보)를 주고 받는 모든 것
- 월드 와이드 웹 (WWW) 과 같은 분산 하이퍼미디어 시스템을 위한 소프트웨어 개발 아키텍처의 한 형식
- REST는 기본적으로 웹의 기존 기술과 HTTP 프로토콜을 그대로 활용하기 때문에 웹의 장점을 최대한 활용할 수 있는 아키텍처 스타일

### API

: Application Programming Interface

사용자 또는 클라이언트, 그리고 사용자와 클라이언트가 얻으려 하는 리소스 사이의 조정자

API는 개발자가 새로운 애플리케이션 구성 요소를 기존 [아키텍처](https://www.redhat.com/ko/topics/cloud-native-apps/what-is-an-application-architecture)에 통합하는 방식을 간소화

![](https://www.redhat.com/cms/managed-files/styles/wysiwyg_full_width/s3/API-page-graphic.png?itok=5zMemph9)

- API는 리소스에 대한 액세스 범위를 넓히는 동시에

  보안과 제어를 유지할 수 있도록 함.



### Rest 구성

- 자원 (RESOURCE) - URI
- 행위 (Verb) - HTTP Method
- 표현 (Representations)

### Rest 의 특징

#### **1) Uniform (유니폼 인터페이스)**

: URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일

#### **2) Stateless (무상태성) **

: 작업을 위한 상태정보를 따로 저장, 관리 X

  키 정보를 별도로 저장, 관리 X 

:arrow_forward: API 서버는 들어오는 요청만을 단순히 처리하면 됨

#### **3) Cacheable (캐시 가능) **

: HTTP라는 기존 웹표준을 그대로 사용

> 웹에서 사용하는 기존 인프라를 그대로 활용 가능

따라서 HTTP가 가진 캐싱 기능이 적용 가능

#### **4) Self-descriptiveness (자체 표현 구조) **

: REST API 메세지만 보고도 이를 쉽게 이해 할 수 있는 자체 표현 구조

#### **5) Client - Server 구조 **

: 서버는 API 제공, 클라이언트는 사용자 인증이나 컨텍스트(세션, 로그인 정보)등을 직접 관리하는 구조로 각각의 역할이 확실히 구분

#### **6) 계층형 구조 **

: REST 서버는 다중 계층으로 구성 O

> 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있음
>
> > PROXY, 게이트웨이 같은 네트워크 기반의 중간매체를 사용

