---
layout: post
title: "[부스트코스 - 웹 프로그래밍] 2일차"
excerpt: "Day 2 Boost Course Web Programming Review"
tags: [web, mooc, online course, boost course]
author: larvinion
comments: true
---

## 3. Web Front-End & Back-End

### 1) Front End
##### Web Front End란?
* 사용자에게 웹을 통해 다양한 콘텐츠(문서, 동영상, 사진 등)을 제공
* 사용자의 요청(요구사항)에 반응해서 동작
* Client Side

##### Web Front End의 역할
* **HTML** : 웹 콘텐츠를 잘 보여주기 위한 구조
* **CSS** : 적절한 배치와 일관된 디자인 등을 제공
* **JavaScript** : 사용자의 요청을 잘 반영

### 2) Back End
##### Web Back End란?
* 정보처리 및 저장, 요청에 따라 정보를 내려주는 역할
* Server Side

##### Back End 개발
* 프로그래밍 언어(**Java**, PHP, Python, JavaScript 등)
* 웹의 동작 원리
* 알고리즘, 자료구조 등 프로그래밍 지식
* 운영체제, 네트워크 등에 대한 이해
* 프레임워크에 대한 이해(**Spring**, Django 등)
* DBMS에 대한 이해와 사용방법(MySQL, Oracle 등)

## 4. Web Browser의 동작[^1]
##### Browser란?[^2]
* 데이터를 해석해주는 파서 + 데이터를 화면에 표시해주는 렌더링엔진을 포함한 소프트웨어

##### Browser의 기본 구조

| 구성 요소 | 특징 |
|:--------|:-------:|
| User Interface | 주소표시줄, 이전/다음 버튼, 북마크 메뉴, 브라우저에서 보이는 모든 요소(요청 페이지 창을 제외) |
| Browswer Engine | UI와 렌더링 엔진 사이의 작업을 정렬 |
| Rendering Engine | 요청된 콘텐츠를 보여주는 역할, ex) 요청된 HTML을 렌더링 엔진이 HTML과 CSS를 파싱하여 화면에 파싱된 콘텐츠를 보여줌 |
| Networking | 플랫폼 독립 인터페이스로, HTTP 요청과 같은 네트워크 호출에 사용 |
| JavaScript Interpreter | 자바스크립트 코드를 파싱하고 처리함 |
| UI Backend | 콤보 박스와 창 같은 기본적인 위젯을 그리는데 사용, 플랫폼에 종속되지 않은 일반 인터페이스|
| Data Storage | 영구적인 층으로, 브라우저는 쿠키와 같은 모든 종류의 데이터를 로컬로 저장 가능해야 함 |

##### Main Flow(Webkit)
![Webkitflow Image]({{ site.url }}/img/webkit-flow.jpg)[^3]

##### Parsing General
* Lexical Analysis
* Syntax Analysis
* Semantic Analysis
* 자세한 부분은 컴파일러 관련으로 Pass

##### HTML Parser
* HTML 태그를 통해 DOM Tree 구성

##### CSS Parser
* Brace로 작성, Selector, Declaration로 Tree 구조 구성

[^1]: [How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)
[^2]: [브라우저는 어떻게 동작하는가?](https://d2.naver.com/helloworld/59361)
[^3]: [그림 출처](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/#The_browser_main_functionality)
