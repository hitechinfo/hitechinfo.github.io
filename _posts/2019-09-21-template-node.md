---
layout: post
title: Node.js Template
tags: [Backend, Node.js, Template]
feature-img: "assets/img/pexels/node.jpg"
thumbnail: "assets/img/pexels/node.jpg"
image: "assets/img/pexels/node.jpg"
excerpt_separator: <!--more-->
---

## [Node.js Template]

Node.js Template을 활용하여 Cloud Native Application의 Backend 서비스를 빠르게 구현해보세요.

<!--more-->

| 구분            | 설명            |링크   |
| :-------------: |:-------------:| :-----:|
| Full Version  | Node.js, Express, Sequelize 기술을 이용한 Backend 템플릿 | [바로가기](https://github.com/hitechinfo/template_backend_node_001)|
| Skeleton Version      | 기본적인 REST 기능만 구현된 Backend 템플릿     |   [바로가기](https://github.com/hitechinfo/template_backend_node_002)|

<br/>

### 프로젝트 구조
---------------------------

* `api` - Api 통신을 위한 data model과 data를 만들기 위한 controller가 정의합니다. 
* `bin` - 서버와 DB의 연결을 제어합니다.  
* `config` - 공통 메세지 및 각종 설정파일이 정의합니다.  
* `docs` - git의 프로젝트 소개 파일이 정의합니다.  
* `k8s` - k8s 설정관련 파일이 정의합니다.
* `node_modules` - 프로젝트에 사용되는 package들이 설치되어 있습니다.  
* `server` - backend 서버의 시작점이자 db 연결의 시작점입니다.  
* `.dockerignore` - docker에 변경정보를 반영 할 때 무시할 파일을 정의합니다.
* `.env` - db, redis 정보 등 민감한 정보들을 정의합니다.
* `.gitignore` - git에 변경정보를 반영 할 때 무시할 파일을 정의합니다.   
* `app.js` - api호출이 들어왔을때 path를 구분하여 각 api index를 호출합니다.  
* `Dockerfile` - docker 설정관련 정보를 정의합니다.  
* `Jenkinsfile` - jenkins 설정관련 정보를 정의합니다.
* `package.json` - 프로젝트 설정관련 정보를 정의합니다. 
 <br/>
 <br/> 

### 프로젝트 설정
---------------------------

server
---------------------------------
1. Package.json에 `npm start`(서버실행명령어)를 실행하게 되면 위의 `server.js`가 실행된다.(Package.json에 세팅)  
2. `server.js` 코드를 보면 `app.js` 파일에서 node 서버를 구동하고 이후 `syncDatabase()`를 통해 db와 연결한다.
<br/>
<br/>

environments
---------------------------------
1. 로컬 환경과 운영환경의 구분을 위하여 config 폴더내에 `environments.js` 파일을 정의하여 사용한다.  
2. `.env`파일에 서버 정보 등을 정의해놓고 `environments.js`파일에서 사용하여 local환경가 운영환경에서의 정보를 분리시킨다.
<br/>
<br/>
 
 env
---------------------------------
 1. `.env` 파일내에 maria ,redis , jwt 관련 정보등을 정의하여 사용한다. Node_env 속성을 통하여 위에서 설명한 `environmemts.js` 파일내에서 로컬과 운영환경을 구분 할 수 있다.
<br/>
<br/>

systemMessage
---------------------------------
 1. 공통으로 사용되는 메시지는 config 폴더안에 `systemMessage.js` 파일 내에 정의하여 사용한다.
<br/>
<br/>

models
--------------------------------- 
 1. Node에서는 maria db와 통신하기 위해 편리한 기능을 제공하는데, 이때 사용되는것이 `Sequelize`이다. `Sequelize`를 사용하기 위해서는 객체를 만들고 db정보를 통해 연결을 해야한다. 매번 객체를 만들어 db와 연결되는 model을 정의 할 수 없으니 `models.js`를 따로 만들어 db와 연결하고 필요시 import해서 사용한다.
<br/>
<br/>

sync-database
---------------------------------
 1. `Sync-database.js` 파일은 db와 연결하는 부분이다. `Sequelize`와 연결을 위해 생성한 model을 가져와 sync 함수를 통해 db연결을 실행한다. 이때 force:false 옵션을 주면 테이블이 존재할 경우 테이블을 지우지 않는다.
