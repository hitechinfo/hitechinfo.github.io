---
layout: post
title: Getting Started
summary: 행복성장플랫폼 가이드는 처음 시작하실 때 참고하시면 좋을 만한 내용을 소개하고 있습니다.
featured-img: skhappycampus
---

## 행복성장플랫폼 가이드
행복성장플랫폼 가이드는 처음 시작하실 때 참고하시면 좋을 만한 내용을 소개하고 있습니다.


### 1. Cloud Native 란?
행복성장플랫폼은 Cloud Native를 지향하고 있습니다. 일반적인 의미에서 “클라우드 네이티브”는 클라우드 컴퓨팅 제공 모델의 이점을 활용하는 애플리케이션 구축 및 실행 접근 방법입니다. 클라우드 네이티브 앱 개발에는 일반적으로 데브옵스, 애자일 방법론, 마이크로서비스, 클라우드 플랫폼, 쿠버네티스 및 도커와 같은 컨테이너, 그리고 CI/CD 개념이 포함됩니다.

[현대적인 소프트웨어 개발 방법 ‘클라우드 네이티브’의 정의와 특징](http://www.itworld.co.kr/news/109679)
  
### 2. 행복성장플랫폼 구조
행복성장플랫폼은 Github-ZCP-CloudZ로 연결되는 CloudZ기반 오픈소스 플랫폼입니다.
![플랫폼구조](/assets/img/posts/platform.png)
  
### 3. 참고 기술요소
#### - Git
깃(Git /ɡɪt)은 프로그램 등의 소스 코드 관리를 위한 분산 버전 관리 시스템입니다. 분산 버전 관리 시스템을 쉽게 말하면, 여러명의 개발자(분산)가 특정 프로젝트를 자신의 컴퓨터로 협업하여 개발하면서 버전을 관리할 수 있는 시스템입니다. 

[Git이란 무엇인가?](https://medium.com/@psychet_learn/git-%EC%82%AC%EC%9A%A9%EB%B2%95-1%EA%B0%95-git%EC%9D%B4%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80-340438d9a69f)

#### - Github
git을 호스팅해주는 웹 서비스이며,  git 저장소 서버를 대신 유지 및 관리해주는 서비스입니다. 다른 유저들과 함께 온라인으로 하나의 프로그램을 제작하는 것도 가능하여, 많은 오픈소스 프로그램들이 github을 통해서 전세계 유저들에 의해 제작되고 있습니다. 

[github란? - github 소개 및 설치](https://m.blog.naver.com/PostView.nhn?blogId=ufo7142&logNo=220628116787&proxyReferer=https%3A%2F%2Fwww.google.com%2F)

#### - JWT
행복성장플랫폼의 템플릿은 JWT를 이용하여 토큰 기반 인증을 하고 있습니다. JSON Web Token은 웹표준(RFC 7519)으로서 두 개체에서 JSON 객체를 사용하여 가볍고 자가수용적인(self-contained) 방식으로 정보를 안전성 있게 전달해줍니다.

[토큰 기반 인증 간단 정리 Token based Authentication](https://blog.msalt.net/251)

[JSON Web Token 소개 및 구조](https://velopert.com/2389)

#### - Redis
행복성장플랫폼은 유효한 토큰을 White List로 관리하고 있으며, 이때 토큰 저장을 위해 Redis 사용하고 있습니다. Redis는 REmote DIctionary Server의 약자로, 디스크가 아닌 메모리 기반의 데이터 저장소입니다.

[Redis 개념과 특징](https://goodgid.github.io/Redis/)
  
  
  
## Template 사용하시기 전에 읽어보세요!
행복성장플랫폼 템플릿을 활용하면 Cloud Native Application을 쉽게 구현하실 수 있습니다. 

  
### 1.React Frontend 템플릿
React-Redux, Babel, Webpack 기술을 이용한 Frontend 템플릿

#### - Prerequisite
1) Javascript 문법에 대한 기본 지식

2) React/Redux에 대한 이해


#### - Reference

[생활코딩-자바스크립트 기본](https://opentutorials.org/course/743/6582)

[누구든지 하는 리액트: 초심자를 위한 리액트 핵심 강좌](https://velopert.com/3613)

[리덕스(Redux)를 왜 쓸까? 그리고 리덕스를 편하게 사용하기 위한 발악 (ii)](https://velopert.com/3533)

  
### 2.Node.js Backend 템플릿
Node.js, Express, Sequelize 기술을 이용한 Backend 템플릿

#### - Prerequisite
1) Javascript 문법에 대한 기본 지식

2) 동기/비동기 처리에 대한 이해 (Promise)

3) REST 동작원리

4) Redis(NoSQL) 사용법

5) MariaDB 사용법

#### - Reference

[생활코딩-자바스크립트 기본](https://opentutorials.org/course/743/6582)

[동기(Sync) 와 비동기(Async)](http://leechoong.com/posts/2017/nodejs_syncasync/)

[Promise 강의](https://programmingsummaries.tistory.com/325)

[REST란?](https://nachwon.github.io/rest-1/)

[node.js에서 Redis 사용하기](https://bcho.tistory.com/1098)

[MySQL – 자주 사용하는 명령어, 문법](https://bugwhale.com/mysql-commands-frequently-used/)

  
### 3.SpringBoot Backend 템플릿
Springboot, Spring Security, JPA 기반 템플릿

#### - Prerequisite
1) JAVA/Spring에 대한 이해

2) Spring Security

2) JPA 사용법

3) REST 동작원리

4) Redis(NoSQL) 사용법

5) MariaDB 사용법

#### - Reference

[MVC패턴이란](https://m.blog.naver.com/jhc9639/220967034588)

[spring security 파헤치기](https://sjh836.tistory.com/165)

[Spring Boot 기반 Spring Security 회원가입 / 로그인 구현하기](https://xmfpes.github.io/spring/spring-security/)

[Spring Boot JPA 사용해보기](https://velog.io/@junwoo4690/Spring-Boot-JPA-%EC%82%AC%EC%9A%A9%ED%95%B4%EB%B3%B4%EA%B8%B0-erjpw41nl7)