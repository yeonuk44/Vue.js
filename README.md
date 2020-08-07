# Vue.js
Vue.js practice environment (with. yeonuk44, kwanmin08)


## yeonuk44
게시판을 기능을 구현하기 위해 개린이르라나 님의 유튜브를 참고하였습니다.
[Reference](https://www.youtube.com/channel/UC5ChZXCogqV99ju-M0TNNfw)

### Build Setup
- Install Dependencies : npm install
- Install Vue | Version Up Vue : npm install vue
- Create Project(Install Webpack, Yarn, Jest etc) : vue init webpack Project Name
- Serve with Hot Reload at localhost:8080 : npm run dev
- Build for Production with Minification : npm run build
- Build for Production and View the Bundle Analyzer Report : npm run build --report
- Run Unit Tests : npm run unit
- Run All Tests : npm test

### Vue.js 특징
- MVVC 패턴 : 뷰는 UI 화면 개발 방법 중 하나인 MVVM 패턴의 뷰 모델에 해당하는 화면단 라이브러리입니다.
화면의 요소들을 제어하는 코드와 데이터 제어 로직을 분리하여 코드를 더 직관적으로 이해할 수 있게 도와주며 추후 유지 보수가 편해집니다.
- 컴포넌트 기반 프레임워크 : 컴포넌트 트리 구조를 갖게 되는 것입니다. 이러한 컴포넌트 기반의 프레임워크를 사용함으로써 코드의 재사용성이 향상되며 직관적인 화면 구조를 갖게 됩니다.
- 리액트, 앵귤러의 각 장점을 갖고 있는 프레임워크 : 뷰는 앵귤러의 양방향 데이터 바인딩과 리액트의 단방향 데이터 플로우의 장점을 모두 결합한 프레임워크입니다. 양방향 데이터 바인딩이란 화면에 표시되는 값과 프레임워크의 모델 데이터 값이 동기화되어 한 쪽이 변경되면 다른 한쪽도 자동으로 값이 변경되는 것을 의미하며, 단방향 데이터 플로우는 컴포넌트 간 데이터 전달 시 항상 상위 컴포넌트에서 하위 컴포넌트로 한 방향으로만 전달되게끔 프레임워크가 구조화되어 있는 것을 말합니다. 
- 빠른 랜더링 : 리액트 가상 돔 랜더링 방식을 적용해 사용자 인터랙션이 많은 현대의 웹 화면에 적합한 동작 구조를 갖고있습니다. 가상 돔을 활용하게되면 특정 돔 요소를 추가하거나 삭제하는 변경이 일어날 때 화면 전체를 다시 그리지 않고 프레임워크에서 정의한 방식에 따라 화면을 갱신하여 브라우저 측면에서 성능 부하가 줄어들어 웹의 퍼포먼스 향상에 기여할 수 있게합니다.

### Vue로 네이티브 모바일 앱 만드는 방법
NativeScript로 만들 예정입니다.
[Reference](https://vuejs-kr.github.io/vue/nativescript/2017/08/11/introduce-vue-nativescript-01/)
## kwanmin08
