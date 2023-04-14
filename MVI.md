## MVI Pattern

MVI Pattern?

: Model + View + Intent



### Model

- 모델은 앱의 유일한 상태와 데이터를 갖고 있는 불변 객체

### View

- 뷰는 Model로 받은 데이터가 우리에게 보여지는 화면을 뜻함

### Intent

- MVI에서 Intent는 우리가 알고있는 안드로이드의 android.content.Intent가 아님
- MVI에서의 Intent는 앱의 상태를 바꾸라는 요청을 뜻함
- 따라서 Intent()가 실행되면 새로운 상태를 가진 모델을 받게 됨

![img](https://miro.medium.com/max/875/1*yJNyvM0ATFZqs3m0NJLrmQ.png)

Intent를 실행함으로써, Intent의 결과가 새로운 model을 만들어내고,

이와 동시에 다른 구성요소의 부수효과를 실행시키게 됨



### Redux

- MVI에서 모델 업데이트는 Redux라는 새로운 개념에 의해 진행
- 자바스크립트에서 앱의 상태 관리를 위한 오픈 소스 라이브러리
- 3가지의 컴포넌트를 가짐

  - State : 앱으이 상태를 갖고 있는 홀더
  - Action : State를 바꾸기 위한 명령
  - Reducer : 이전의 State와 Action을 받아 새로운 State를 만들어주는 순수 함수



### Reducer

- Reducer을 실행시켜 새로운 모델을 만들어냄.
