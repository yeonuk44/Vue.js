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

### 코드 분할
코드 분할(Code Splitting)은 싱글 페이지 애플리케이션의 성능을 향상시키는 방법입니다. 싱글 페이지 애플리케이션(Single Page Application)은 초기 실행시에 필요한 웹 자원을 모두 다운 받는 특징이 있습니다. 코드 분할을 활용하게 되면 초기 로딩시에 모든 웹 자원을 다운받지 않고 필요한 시점에 다운 받아 성능 상의 이점이 생깁니다. 
#### 라우터의 코드 분할 문법
```
{
	path: 'url 이름',
	component: () => import('컴포넌트 이름')
}
```
위와 같은 방법을 지연된 로딩(Lazy Loading)이라고 합니다. 이는 애플리케이션 규모가 커져 싱글 페이지 애플리케이션의 초기 화면 로딩 시간을 줄일 때 사용하는 방법입니다. 왜냐면 화면이 10개인 웹 앱이 있는데 애플리케이션을 처음 시작했을 때 쓰지도 않을 나머지 화면 9개를 다 불러오는 것 보다는 특정 화면으로 이동할 때마다 해당 화면의 내용을 추가적으로 불러오는 것이 애플리케이션 로딩 속도 면에서 더 효율적이기 때문입니다.

### 초기 진입 페이지 설정
리다이렉트 뷰(Redirect) 뷰 이름에 "redirect:" 접두어를 붙이면, 지정한 페이지로 리다리렉트 된다. 리다이렉트 URL은 다음과 같이 두 가지 방식으로 입력할 수 있다.
```
redirect:/bbs/list: 현재 서블릿 컨텍스트에 대한 상대적인 경로로 리다이렉트
redirect:http://host/bbs/list: 지정한 절대 URL로 리다이렉트
```

### Back-End
axios 웹 또는 앱을 개발하다 보면 거의 대부분이 서버가 필요하게 된다. 서버에 내용을 저장하고 웹이나 앱에서 서버의 저장된 내용을 불러다가 사용자에게 보여주게 된다. 이때 javascript에는 axios라는 아주 훌륭한 플러그인이 있다. axios는 javascript용 플러그인으로 많이 사용하지만 Vue.js에서도 매우 요긴하게 사용된다. axios는 Promise 기반의 자바스크립트 비동기 처리방식을 사용합니다. 그래서 요청후 .then()으로 결과값을 받아서 처리를 하는 형식으로 구성되어 있다.
설치하는 법
```
npm install --save axios
```

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

## 2020-09-15 공부 

const instance = axios.create({
baseURL : 'http://~})

-axios의 create 인스턴스를 변수로 할당가능

.env 파일 (생성) 위치 : 루트
-VUE_APP_변수명으로 env에 할당하면 다른곳에서 쓸수있음

## 2020-09-23 공부 

실제 앱 제작에서는 기능보다 에러를 잘 구현하는 것이 수준 높은 앱

에러가 났을 때는 무조건 화면에 표시해줘야 함

this.$router.push(); -->()안에 있는 주소가 더해진 URL로 이동

1) loginform - login page - app - appheader (컴포넌트 통신 방식)

2) loginfrom - appheader (이벤트버스)

3) 뷰엑스 (스토어 방식) - 스트링 값을 store라는 통에 담아 놓고 app-header로 이동

dependencies - npm run build 결과물 포함
devdependencies - 미포함

store 의 state는 여러 컴포넌트에서 공유되는 데이터


this.$store.commit('setuername')

상태변경된 값을 가져오는  getters -->return 값 가져옴 마치 computed
html은 최대한 간단하게
script단에있는걸 연결하는 방식
