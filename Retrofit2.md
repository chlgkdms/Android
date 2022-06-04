## Retrofit2

- REST API 통신을 통해 구현

- 동일 Squareup사의 OkHttp 라이브러리의 상위 구현체

  : Retrofit은 OkHttp를 네트워크 계층으로 활용하고 그 위에 구축됨

#### 장점

- 빠른 성능

  > Okhttp는 AsyncTask를 사용 (AsyncTask의 3~10배의 성능차이)

- 간단한 구현 - 반복된 작업을 라이브러리 넘겨서 처리

- 가독성

  > Annotation 사용으로 코드의 가독성이 뛰어남, 직관적인 설계가 가능

- 동기/비동기 쉬운 구현

  > 동기 Synchronous - 동시에 일어난다는 의미로, 요청(응답이 하나의 트랜잭션에서 발생) 후 									응답까지 대기한다는 의미

  > 비동기 Asynchronous - 동시에 일어나지 않는다는 뜻으로
  >
  > ​									요청(응답은 별개의 트랜잭션) 후 응답이 도착하면 Callback으로 받아서 처리

### 3가지 구성요소

- DTO (POJO) - 'Data Transfer Object', 'Plain Old Java Object' 형태의 모델 / JSON 타입변환에 사용
- Interface - 사용할 HTTP CRUD 동작 (메소드) 들을 정의해놓은 인터페이스
- Retrofit.Builder 클래스 - Interface를 사용할 인스턴스, baseUrl(URL) / Converter(변환기) 설정
