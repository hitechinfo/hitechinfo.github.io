---
layout: post
title: React Template
tags: [Frontend, React, Template]
feature-img: "assets/img/pexels/react.jpg"
thumbnail: "assets/img/pexels/react.jpg"
image: "assets/img/pexels/react.jpg"
excerpt_separator: <!--more-->
---

## React Template
React Template을 활용하여 Cloud Native Application의 Frontend 서비스를 빠르게 구현해보세요.

<!--more-->

| 구분            | 설명            |링크   |
| :-------------: |:-------------:| :-----:|
| Full Version  | React-Redux, Babel, Webpack 기술을 이용한 Frontend 템플릿 | [바로가기](https://github.com/hitechinfo/template_frontend_react_001)|
| Skeleton Version      | Semantic UI를 활용한 Frontend 템플릿     |   [바로가기](https://github.com/hitechinfo/template_frontend_react_002)|

<br/>
<br/>

### 프로젝트 구조
---------------------------

**개발관련**  
* `node_modules` : npm install 시 설치되는 module이 저장되는 폴더  
* `public` : react app의 가장 root가 되는 element가 위치하는 index.html이 위치하는 폴더  
* `src` : application 관련 코드가 위치  
* `components` : 컴포넌트 형태의 component가 위치 (컴포넌트 형태는 주로 redux연결 없이 단순 view를 목적으로 하는 경우가 많다. presentational components라고도 함)  
* `containers` : 컨테이너 형태의 component가 위치 (components 폴더에 선언한 여러 컴포넌트들을 조합해서 완성된 형태를 보여주는 것을 컨테이너라고 한다. props관리를 위해 redux가 connect되는 레벨)  
* `lib` : 프로젝트 자체적으로 필요한 user-custom module이 위치하는 폴더 (날짜 formatter, session storage control 등)  
* `modules` : state상태 관리를 위한 reducer가 위치하는 폴더 (reducer + action 형태로 선언/관리 된다)  
* `routes` : url 이동정보 (인증 필요/불필요로 구분)  
* `style` : css파일이 위치한 폴더  
* `App.js` : application의 시작점 js  
* `index.js` : react의 root dom이 그려지는 js. 화면의 전체구조를 정의    
* `package.json` : 현재 프로젝트의 정보 파일  
* `webpack.config.dev.js` : 개발 진행 시 프로젝트 설정파일  
* `webpack.config.js` : 운영 배포 시 프로젝트 설정파일  
  
**설정관련**  
* `babelrc` : 바벨 설정파일
* `gitignore` : github commit시 제외할 항목을 설정하는 파일  
* `Dockerfile` : docker 설정파일  
* `Jenkinsfile` : Jenkins 설정파일  
* `nginx.conf` : nginx 설정파일   

<br/>

### 주요 사용 모듈
---------------------------

Front end 개발 시 주로 사용하는 모듈은 아래와 같으며, 추가적인 모듈이 필요한 경우 npm install 을 통해 설치하고 import하여 사용할 수 있습니다.
<br/>

* `react` : react view를 만들기 위한 라이브러리  
* `react-dom` : react를 브라우저에 rendering 할 때 사용되는 라이브러리  
* `redux` : redux 사용을 위한 라이브러리  
* `react-redux` : redux를 react컴포넌트에 연결하기 위해 사용되는 라이브러리  
* `react-router-dom` : 화면 이동을 위해 설정 및 사용하는 라이브러리  
* `redux-actions` : action 생성을 편리하도록 해주는 라이브러리  
* `immutable` : object의 생성 및 변경을 편리하게 할 수 있게 하는 라이브러리 (항상 new object를 return)  
* `lodash` : object의 형태 변형을 편리하게 할 수 있게 하는 라이브러리  
* `axios` : Rest 비동기 호출을 위해 사용하는 모듈  

<br/>

### 개발 시 유의점
---------------------------

**Axios** 

* GET, POST, PUT, DELETE 사용시 parameter 전달은 각각의 옵션에 맞게 전달합니다   
(ex POST 사용하는데 url에 parameter 전달 X)
* Headers에 `Pragma : 'no-cache'` 명령어는 ie 에서 오류를 방지하는 것 이므로 항상 포함시키도록 해야합니다
* 기본형태는 `then / catch` 형태로 사용. Finally는 꼭 필요 시에만 사용합니다
