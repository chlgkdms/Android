## HTTP

### HTTP

: Hyper Text Transfer Protocol

#### HyperText

: 문서와 문서가 링크로 연결되도록 하는 태그로 구성된 언어

#### Transfer

: 사전적으로는 "전송하다", 웹사이트를 다른 사람들과 공유하기 위해

다른 컴퓨터에 전송

#### Protocol

: 협약, 통신 규약 이라는 의미를 가짐

컴퓨터들끼리 HTML 파일을 주고받을 수 있도록 하는 소통방식 또는 약속



### HTTP의 두가지 특징

#### 1. Request(요청) / Response(응답)

보내는 주체는 받는 주체에게 요청을 보내고, 받는 주체는 요청을 보낸 주체에게 응답을 보낸다.

즉, 사람끼리의 소통을 컴퓨터에게 적용하여 '요청'과 '응답'을 하게끔 한것



#### 2. Stateless = State (상태) + less (없음)

각각의 HTTP 통신은 독립적 이기 때문에 과거의 통신에 대한 내용을 전혀 알지 못함

:arrow_forward: 매 통신마다 필요한 모든 정보를 담아서 요청을 보내야함

**연속된 데이터 처리가 필요한 경우**를 위해

로그인 토큰 or 브라우저의 쿠키, 세션, 로컬스토리지 같은 기술이 만들어짐



## HTTP Method

### HTTP Method 를 쓰는 이유

: 같은 경로 (api/users)로 request가 들어온다고 해도, method에 따라 다른 행동을 하기 위해 씀.

ex ) /api/users로 request가 들어와도,

- GET 이면 user를 read 하도록
- POST 면 user를 create 하도록
- ...

#### 자주 쓰이는 method

- GET : 특정 리소스의 표시를 요청. 데이터의 수정 없이 데이터를 받기만 함
- HEAD : GET과 동일한 응답이지만, 응답에 body 가 포함되지 않음
- POST : 특정 리소스를 제출할 때 쓰임
- PUT : 목적 리소스의 모든 현재 표시를 요청하는 값으로 바꿈
- DELETE : 특정 리소스를 삭제
- PATCH : 리소스의 부분만을 수정

##### 그 외

- CONNECT : 목적 리소스로 식별되는 서버로의 터널을 맺음
- OPTIONS : 목적 리소스의 통신을 설정

- TRACE : 목적 리소스의 경로를 따라 메세지 loop-back 테스트를 함



#### CRUD 관점에서 보면..

- GET = Read
- POST = Create
- PUT = Update (total replace : 원래 것을 덮어 씌움)
- PATCH = Update (part correct : 원래 것의 일부를 수정)
- DELETE = Delete



## HTTP 상태코드

- 상태코드는 3자리 숫자로 첫번째 자리 1~5까지 제공

- ##### 1xx (정보) : 요청을 받았으며 프로세스를 계속 진행합니다.

- ##### 2xx (성공) : 요청을 성공적을 받았으며 인식했고 수용하였습니다.

- ##### 3xx (리다이렉션) : 요청 완료를 위해 추가 작업 조치가 필요합니다.

- ##### 4xx (클라이언트 오류) : 요청의 문법이 잘못되었거나 요청을 처리할 수 없습니다.

- ##### 5xx (서버 오류) : 서버가 명백히 유효한 요청에 대해 충족을 실패했습니다.



### 더 자세한 HTTP 상태코드

### 1xx (Information responses)

- 100 Continue (진행 상태에 문제 X)
- 101 Switching Protocol (클라이언트가 보낸 Upgrade 요청)
- 102 Processing WebDeV (서버가 요청 수신 but, 아직 제대로 된 응답 X)



### 2xx (Successful responses)

- 200 OK (요청 성공적)
- 201 Created (요청 성공적 :arrow_forward: 새로운 리소스 생성)
- 202 Accepted (요청 수신 but, 그에 응하여 행동X)
- 204 No Content (요청에 대해서 보내줄 수 있는 콘텐츠X, 헤더는 의미 있을 수 있음)



### 3XX (Redirection messages)

- 301 Moved Permanently (요청한 리소스의 URI가 변경)

- 302 Found (요청한 리소스의 URI가 일시적으로 변경)

- 303 See Other 

  (클라이언트가 요청한 리소스를 다른 URI에서 GET 요청을 통해 얻어야 할 때, 서버가 클라이언트로 직접 보내는 응답)

- 304 Not Modified (캐시를 목적으로 사용, 클라이언트에게 응답이 수정되지 않았음을 알려줌)

- 307 Temporary Redirect

- 308 Permanent Redirect



### 4XX (Client error responses)

- 400 Bad Request (잘못된 문법으로 인하여 서버가 요청 이해X)
- 401 Unauthorized (비인증)
- 403 Forbidden (클라이언트가 콘텐츠에 접근 권리X)
- 404 Not Found (서버가 요청받은 리소스를 찾을 수 없음 브라우저에서 알려지지 않은 URL)



### 5XX (Server error responses)

- 500 Internal Server Error (웹 사이트 서버에 문제가 있음)
- 503 Service Unavailable (서비스 이용 불가)


