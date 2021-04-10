# ReactJS

웹에 관해서, 그 중에서도 ReactJs에 대해서 공부하고 강의들을 수강한뒤, 최종 실습 파트 부분에서 만든 코드입니다.

https://kimsmartblog.tistory.com/

블로그 Web 파트 - ReactJS에 기능별로 정리되어있습니다.


## 강의 제목 및 출처
https://nomadcoders.co/react-fundamentals

Web front, backend Full stack Nomad 선생님

## 목차
![image](https://user-images.githubusercontent.com/44837403/114272363-dc5bd880-9a50-11eb-885d-2e1dde62edba.png)
![image](https://user-images.githubusercontent.com/44837403/114272370-e251b980-9a50-11eb-9fb0-4a7373bce72d.png)
![image](https://user-images.githubusercontent.com/44837403/114272333-be8e7380-9a50-11eb-9698-7756f004c0ac.png)


## 진행 기간
2020-07-16 ~ 2020-07-27

## 프로그램 기능

#### Components들을 만들고 동적으로 사용하기

jsx: JS와 HTML간의 상호 작용. React의 특징임. Component를 사용하는데 Component는 HTML을 JS에서 불러와 사용하기 위해 쓰여짐.
HTML을 반환하는 함수임.
React application은 하나의 component만을 rendering해야함.

#### API로 받아온 데이터를 저장하고 Component에서 Dynamic하게 사용하기

api에서 받아온 데이터를 Const 변수에 저장해서 사용한다고 가정한다. 이 데이터들을 동적으로 사용하는 것이 목표이다.
사용자 지정 함수로 어떤식으로 구성해서 웹에 표시할지를 정한다. App함수에서 map을 사용하는데 이 map 은 array형태의 object들에
설정한 함수을 부여한다. 함수의 내용엔 내부에서 사용될 데이터 인자들의 이름을 지정해서 사용하게 한다. map으로 주는 데이터는 object형태이다.

#### PropTypes 기능으로 데이터 속성 및 자료형 지정해 놓기

component에 있는 prop들을 보내줄때 제대로 보냈는지 확인할 것이다.
PropTypes 에 컴포넌트가 가지는 Props들을 check할 수 있다. 원하는 속성들을 잘 보내주었는지 확인시켜주는 기능이다.

#### Class Components and State 사용하기

React Class Component에서 받아와서 사용함.
render method를 사용할 수 있음.
React는 자동적으로 Class Component의 render method를 자동으로 실행함.
Class Component는 state를 가짐. state: object 데이터의 변하는 속성덕분에 state를 씀.
(state는 직접 변경하지 않고 setState(state와 연동되는 것임.)를 써야함. react가 state를 refresh하고 render를 같이 호출하게 하기 위해서이다.
) 

#### Component Life Cycle 이해하고 이에 맞춰 코드 작성하기

https://reactjs.org/docs/react-component.html
위 문서에 잘 설명되어 있다.

Mounting
-constructor
-render
-componentDidmount

Unmounting
componentDidUpdated (이벤트 실행 뒤에 발생함)
componentWillUnmount(페이지떠나거나 component가 끝날때 발생함)
![image](https://user-images.githubusercontent.com/44837403/114273216-2eeac400-9a54-11eb-8d22-7625e6387771.png)

위의 예제처럼 일종의 순서도를 가지고 있다.

#### 비동기 통신, async - await 구조로 데이터를 받아온 뒤 원하는 형태의 데이터로 맞춰 사용하기

Movie.js에 맞는 형태대로 movies.map을 통해서 데이터들을 화면에 출력하게 한다. 이 때 PropTypes도 지정을 하고 원하는 정보들을 선택해서 출력한다.
isLoading ? a : b 의 삼항연산자 형태로 Loading이 다 되었는지를 판단해서 원하는 기능이 실행되게끔 한다.
이때 Loading이 false인 경우 setState에서 온 movies 객체를 사용해서 map을 실행한다. 그러면 movies의 array안에 있는 객체들 마다 함수 movie가 실행이 되고 component를 실행하게 된다. 
이때 각 component는 key, id 등등이 설정이 된다. data가 올때에는 async, await구조를 이용하고 axios를 이용해 data를 fetch하였다.

#### Navigation 기능 만들기

 우선 파일들을 구조화 한다. Components에 Movie component파일들을 넣어준다. routes에는 메인 js와 About.js를 만들어서 넣어준다.
이제 App.js에서 react-router-dom을 이용한 Navigator 기능을 만들것이다.
 import경로를 달리해주었다. class 이름과 export 도 Home으로 해준다.
react-router의 HashRouter를 쓴 모습이다. 이 router를 이용하면 react에서 url을 가져와 path를 지정해서 사용할 수 있다.
이 때 exact함수를 사용했는데, 이는 react가 /를 가지는 여러개의 componet를 동시에 rendering하는것을 막아주기 위해서이다.

#### Route간의 데이터 공유해서 사용하기

 Link를 부여하고 이 Link를 누르면 router로 정보를 보내게 할 것임. 전송받은 데이터는 component로 받아서 새로운 페이지에 표시해 줄것임.


#### 출력 화면 

![image](https://user-images.githubusercontent.com/44837403/114273991-69099500-9a57-11eb-84fc-11ccfe403a94.png)



## 느낀점

 당시 방학기간이였는데 꽤나 힘들게 진행했던 기억이 있습니다. 생각보다 자바스크립트를 활용해서 웹을 구현하는 것이 복잡하고 다양했습니다.
 공부를 진행하지만 눈에 보이는 변화가 많이 보이지 않아 힘들었던 것 같습니다. 그래도 프로그래밍에 대해서 익히고, 웹 구성에 대해 이해하고
 언젠가 이 부분들이 활용될 수도 있을것이라 생각하면서 진행했습니다. 또 물론 강의를 들으며 진행했지만서도 웹으로 디자인을 구현해서
 출력이 될 때 나름 보람을 느꼈습니다.






