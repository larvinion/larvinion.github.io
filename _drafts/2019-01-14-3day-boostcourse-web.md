---
layout: post
title: "[부스트코스 - 웹 프로그래밍] 3일차"
excerpt: "Day 3 Boost Course Web Programming Review"
tags: [web, mooc, online course, boost course]
author: larvinion
comments: true
---

## 5. Browser에서의 웹 개발

### 1) Browser
##### HTML 문서구조
* html 시작, /html 종료
* HTML 계층 구조
* HTML은 tag <>를 사용하여 표현
* head : HTML의 추가적인 정보
* body : HTML의 내용

##### 특징
* Browser 해석순서 : 1 Line 씩 순차적 해석
* JavaScript와 CSS의 위치는 HTML안의 여러 곳
* CSS의 위치 : head 안에 위치하여 렌더링 처리 시 브라우저가 더 빨리 참고할 수 있도록 함
* JavaScript의 위치 : body 다음에 위치하여 HTML 렌더링을 방해하지 않도록 함
* **defer/async** 속성을 사용하여 선언부와 스크립트 실행 시점을 분리 할 수 있음[^1]

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, intial-scale=1">
    <title>타이틀</title>
    <link rel="stylesheet" href="css/style.css">
    <sript src="js/start.js"></script>
  </head>
  <body>
    <h1>헤더</h1>
    <div>연습 코드입니다.</div>
  </body>
  <script src="js/library.js"></script>
  <script src="js/main.js"></script>
</html>
{% endhighlight %}

##### 추가질문
* Where to place JavaScript in an HTML file?
> [https://stackoverflow.com/questions/196702/where-to-place-javascript-in-an-html-file](https://stackoverflow.com/questions/196702/where-to-place-javascript-in-an-html-file)

* Best Practices for Speeding Up Your Web Site - Yahoo Developer
> [https://developer.yahoo.com/performance/rules.html#css_top](https://developer.yahoo.com/performance/rules.html#css_top)

**<CSS : head 태그 안, JavaScript : </body> 태그 이전 위치>가 웹 페이지 로딩을 빠르게 함**

## 6. Web Server

### 1) Web Server Software
##### Web Server란?
* 보통 **Web Server Software** 를 뜻하지만, 이를 동작하고 있는 컴퓨터를 뜻함
* 클라이언트(Client)가 요청하는 HTML문서, 각종 리소스(Resource)를 전달
* Web Browser 또는 Web Crawler가 요청하는 리소스는 Web Server에 저장되어 있는 정적(Static) 데이터 또는 동적인 결과임
* **정적(Static) 데이터 : 이미지, HTML, CSS, JavaScript 등의 File**
* **동적 결과 : Web Server에 의해 실행된 프로그램을 통해 만들어진 결과**

##### Web Browser & Web Server
<div markdown="0" style="width:100%; text-align:center"><div class="btn btn-info">Web Browser(Client)</div></div>
<div markdown="0" style="text-align:center"><div class="arrow arrow-down" style="display:inline-block">(1)Request Message</div><div class="arrow arrow-up" style="display:inline-block">(2)Response Message</div></div>
<div markdown="0" style="width:100%; text-align:center"><div class="btn btn-info">Web Server(Server)</div></div>

##### Web Server Software 종류
* 가장 많이 사용하는 Web Server는 Apache, Nginx, Microsoft, Google 등
* Apache Web Server : 가장 많이 사용, Apache Software Foundation에서 개발한 오픈소스 소프트웨어
* Nginx : 차세대 Web Server, 더 적은 자원으로 더 빠르게 데이터를 서비스하는 목적으로 개발, 오픈소스 소프트웨어

##### Netcraft 전세계 웹 서버 시장 점유율
![December 2018 Web Server Survey]({{ site.url }}/img/dec-2018-web-server-survey.jpg)[^2]

## 7. WAS

### 1) Web Application Server
##### WAS(Web Application Server)란?
* Client/Server 구조
![Client Server Model]({{ site.url }}/img/client-server-model.jpg)[^3]
* DBMS(DataBase Management System)
   * DBMS의 등장으로 Client에서 직접 접속하여 동작하는 프로그램들이 개발(Fat Client)
![Database Management System]({{ site.url }}/img/dabase-manegement-system.jpg)[^4]
* 미들웨어(MiddleWare)
   * 위와 같은 문제점을 해결하기 위해 등장
   * 클라이언트에 많은 비즈니스 로직 -> 클라이언트 관리(배포 등)에 많은 비용 소모
   * 비즈니스 로직을 클라이언트와 DBMS 사이의 미들웨어 서버에서 동작하도록 함 -> 클라이언트(입/출력만) 담당
![MiddleWare]({{ site.url }}/img/middleware.jpg)[^5]
* WAS(Web Application Server)
   * 일종의 미들웨어, 클라이언트의 요청 중 동적인 데이터를 제공하기 위한 웹 애플리케이션을 동작하도록 지원
   * 프로그램 실행 환경과 데이터베이스 접속 기능 제공
   * 트랜잭션 관리
   * 비즈니스 로직 수행

##### Web Server vs WAS
* Web Server : 보통 정적 데이터를 웹 브라우저에 전송
* WAS : 프로그램의 동적인 결과를 웹 브라우저에 전송
* 현재 WAS가 제공하는 내장 Web Sever의 정적 데이터 처리 기능으로도 성능상 큰 차이 X
* But, 간단한 구조의 Web Server와 3-Tier구조로 장애 극복 기능(FailOver)에 유리 -> 무중단 운영에 중요
![Web Server and WAS]({{ site.url }}/img/web-server-vs-web-application-server)[^6]

[^1]: [defer/async](https://developer.mozilla.org/ko/docs/Web/HTML/Element/script)
[^2]: [그림 출처:netcraft](https://news.netcraft.com/archives/2018/12/17/december-2018-web-server-survey.html)
[^3]: [그림 출처:Edwith](https://www.edwith.org/boostcourse-web/lecture/16666/)
[^4]: [그림 출처:Edwith](https://www.edwith.org/boostcourse-web/lecture/16666/)
[^5]: [그림 출처:Edwith](https://www.edwith.org/boostcourse-web/lecture/16666/)
[^6]: [그림 출처:Edwith](https://www.edwith.org/boostcourse-web/lecture/16666/)
