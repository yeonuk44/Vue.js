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

### Vue CLI 설치 
[Reference](https://cli.vuejs.org/guide/installation.html)

### Vue 프로젝트 설치 옵션
- Manually select features
- Babel, Linter, Unit
- Prettier
- Lint on Save
- Jest
- In dedicated config files
- n

### CLI 설치 이후 ESLint 에러가 콘솔창에만 뜨고 앱에는 표시되지 않게 하는 방법
vue.config.js 를 프로젝트 단위 폴더에 생성한 뒤 
```
module.exports = {
    devServer: {
        overlay: false
    }
};
```
입력한 뒤 저장한다.

### 코드 작성 규칙
현 프로젝트는 prettier 를 사용하여 코드를 작성하여 정리한다.
[Prettier 링크](https://prettier.io/)

### ESLint 플러그인 설치 이후..
vscode 설정에서 "format on save" 입력 이후 체크박스에서 체크 해제를 누른다.

### VSCode를 활용한 파일의 절대 경로 찾기
프로젝트 단위 폴더에 jsconfig.json 파일을 생성한 뒤 
```
{
    "compilerOptions": {
      "baseUrl": ".",
      "paths": {
        "~/*": [
          "./*"
        ],
        "@/*": [
          "./src/*" 
        ],
      }
    },
    "exclude": [
      "node_modules",
      "dist"
    ]
  }
```
를 입력한다. 이후 파일의 경로를 탐색 시 @를 기입하면 바로 src 로 이동한다.

## kwanmin08

eslint - 자바스크립트 문법 보조 도구

설정파일 변경 하면 ---> 서버 재실행 해야함

eslint의 rules와 prettier가 충돌하기 때문에 eslint가 우선시 되어야 한다

Prettier - 팀으로 개발할 때, 개행이라든지 코드를 표현하는 방법을 통일하기 위함(빨간줄로 표시를 해줌)

ctrl + , -->설정 화면

개발툴의 영향을 받지 않기 위해! 

eslintrc에서 extends 는 node_modules에 있는 prettier 정보들을 가져온당

절대경로 필요한 이유 -- 파일이 깊어질수록 경로가 넘 복잡해짐(상대경로)

### 라우터 & 컴포넌트 

Vue.use --> 플러그인 초기화 및 실행을 위한 코드

export 로 파일을 밖으로 내보낼 수 있음

code splitting - 싱글 페이지 에플리케이션 성능 향상 ( 초기에 로딩 x 필요할 때 로딩)

redirect - 초기진입페이지 설정 하기

mode : 'history' 추가하면 url의 #의 사라짐

url에 #이 있는건 서버는 상관하지 않아 

git checkout 2_router -f (브랜치 변환)

## 2020-09-14 공부 

-서버실행 npm run dev

vim - component 불러오기

페이지 컴포넌트는 가급적 dry하게

vda - 데이터 속성 빠르게 설정하기

input들을 다 작성한 다음
login 버튼을 누르면
form에서 submitForm 이 수행이 된다
.prevent를 쓰면 form의 기본동작인 제출, 새로고침을 막는다


vue -typescript로 만든 개발툴

submitform 을 비동기 처리를 해줘야 해(가입이 완료되었습니다 등의 부가적 기능을 위하여)

input 정보 초기화
initFrom(){
this.~~~ =' ';
}
