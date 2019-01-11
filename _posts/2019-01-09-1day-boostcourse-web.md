---
layout: post
title: "[부스트코스 - 웹 프로그래밍] 1일차"
excerpt: "Day 1 Boost Course Web Programming Review"
tags: [web, mooc, online course, boost course]
categories: [MOOC]
comments: true
---

## 1. 웹 프로그래밍 기초

### 1) 웹 프로그래밍을 위한 프로그램 언어들
##### 저급 언어
* 기계 중심의 언어, 2진수(0과 1)로 이루어진 값 : **기계어(Machine Language)**
* 숫자로 된 문장 1:1 대응 기호 => 기호로 작성된 문장들을 원래의 숫자로 바꿔야 하는 과정 필요
* 이러한 과정에 사용되는 도구 : **어셈블러(Assembler)**
* 기호로 작성된 언어 : **어셈블리어(Assembly Language)**

##### 고급 언어
* 사람 중심의 언어, 사람이 좀 더 이해하기 쉬운 문법
* 작성된 소스코드를 번역하는 도구 : **컴파일러(Compiler)**

| 언어 | 특징 |
|:--------|:--------|
| FORTRAN | 최초의 고급 언어 중 하나, 주로 과학 계산용 |
| COBOL | 일반 업무 목적, 현재도 은행 등에서 사용 |
| PROLOG | 논리형 프로그래밍 언어, 논리식을 토대로 오브젝트와 오브젝트 간 관계에 관한 문제 해결 |
| C | 1972년 벨 연구소의 데니스 리치에 의해 개발, 시스템 프로그래밍에 가장 적합한 평가를 받음 |
| Erlang | 스웨덴의 에릭슨에서 개발한 함수형 병행성 프로그래밍 언어, 통신 인프라를 위한 언어 |
| Lisp | LISt Processor의 약자, 대료적인 함수형 언어 |
| Swift | 2014 WWDC에서 공개한 프로그래밍 언어, 현대 프로그래밍 언어의 발전을 대다수 계승한 모던 프로그래밍 언어 |
| Kotlin | JetBrains에서 2011년에 개발한 프로그래밍 언어, JVM기반으로 Java와 상호 운영 100% 지원 |
| Clojure |리치 히키가 만든 Lisp 프로그래밍 언어의 방언, 범용 함수형 언어 |
| Python | 데이터 과학에서 자주 사용되며 웹사이트 개발에서 많이 사용, 최근 ML(Machine learning)에서도 많이 사용 |
| Java | 1995년 썬 마이크로 시스템즈에서 개발한 객체지향 프로그래밍 언어, 세계에서 가장 많이 사용되는 언어 중 하나 |

#### 웹 관련 인기 언어
###### Python
> 프로그래밍 입문자에게 유용, 데이터 과학에서도 주로 사용되며 웹사이트 개발에서도 많이 사용

###### PHP
> 웹의 80% 이상이 PHP로 만들어졌다고 할 만큼 웹 개발에서 많이 사용

###### JavaScript
> 브라우저에서 동작하는 언어로 시작, 현재 서버에서도 작성하는 프로그램으로 점차 영역 확장

###### Java
> 엔터프라이즈 소프트웨어 환경에 잘 맞는 언어, 큰 규모의 소프트웨어 개발에 많이 사용

###### Ruby
> 빠른 개발에 널리 사용되며, 단순함과 세련된 웹 어플리케이션을 만들 수 있기에 인기 있는 언어 중 하나

* Github 인기 언어[^1]
* 티오베 언어 순위[^2]

[^1]: [Github 인기 언어](https://octoverse.github.com/projects#languages)
[^2]: [티오베](https://www.tiobe.com/tiobe-index)


### 2) 웹의 동작(HTTP 프로토콜 이해)
#### HTTP(HyperText Transfer Protocol)[^3]
* 서버와 클라이언트가 인터넷상에서 데이터를 주고받기 위한 프로토콜(Protocol)
* HTTP/2까지 등장한 상태, v1.1에 대해 학습
* 문서화된 최초의 HTTP버전은 v0.9(1991년)

#### HTTP 작동방식
* 클라이언트/서버 모델
* 장점
   * 불특정 다수 대상 서비스에 적합
   * 클라이언트/서버가 계속 연결된 형태X, 클라이언트/서버 간 최대 연결 수보다 많은 요청과 응답 처리 가능
* 단점
   * 연결을 끊기 때문에, 클라이언트의 이전 상태 알 수 없음(무상태, Stateless)
   * 정보 유지를 위해 Cookie와 같은 기술 등장

#### URL(Uniform Resource Locator)
* 인터넷 상 자원의 위치
* 특정 웹 서버의 특정 파일에 접근하기 위한 경로 혹은 주소
* 접근 프로토콜 :// 웹 서버명 / 경로 / 파일 이름

#### Request Message
* Request Method : GET, PUT, POST, OPTIONS 등
* URI(Uniform Resource Identifier) : 요청하는 자원의 위치 명시
* HTTP Protocol Version : 웹 브라우저가 사용하는 프로토콜 버전

#### Request Method 종류[^4]

| Method | 특징 |
|:--------|:--------|
| GET | 정보를 요청하기 위해 사용 (SELECT) |
| POST | 정보를 밀어넣기 위해 사용 (INSERT) |
| PUT | 정보를 업데이트하기 위해 사용 (UPDATE) |
| DELETE | 정보를 삭제하기 위해 사용(DELETE) |
| HEAD | (HTTP)헤더 정보만 요청, 해당 자원 존재유무, 서버 문제 확인을 위해 사용 |
| OPTIONS | 웹서버가 지원하는 메소드의 종류 요청 |
| TRACE | 클라이언트의 요청을 그대로 반환, ex) echo 서비스로 서버 상태 확인을 위한 목적으로 사용 |

#### Response Message
* HTTP Protocol Version : 웹 서버가 사용하는 프로토콜 버전
* Status Code : 요청의 성공여부 및 그 이유를 나타내는 상태 코드
* Status Message : Status Code에 대한 짧은 설명

#### Status Code 종류[^5]

| Status Code | 특징 |
|:--------|:--------|
| 1XX[^6] | Information responses, 요청 받았으며 작업 요청은 받았으나 클라이언트에 응답X(실험적인 상황 제외) |
| 2XX[^7] | Successful responses, 클라이언트가 요청한 동작 수신 후 성공적으로 처리 |
| 3XX[^8] | Redirection messages, 클라이언트는 요청을 마치기 위해 추가 동작 수행 필요 |
| 4XX[^9] | Client error responses, 클라이언트에 오류가 있음을 나타냄 |
| 5XX[^10] | Server error responses, 서버에 오류가 있음을 나타냄 |

[^3]: [An overview of HTTP](https://www.tiobe.com/tiobe-index)
[^4]: [HTTP Request Method](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
[^5]: [HTTP Status Code](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
[^6]: [Status Code 1XX](https://tools.ietf.org/html/rfc2616#section-10.1)
[^7]: [Status Code 2XX](https://tools.ietf.org/html/rfc2616#section-10.2)
[^8]: [Status Code 3XX](https://tools.ietf.org/html/rfc2616#section-10.3)
[^9]: [Status Code 4XX](https://tools.ietf.org/html/rfc2616#section-10.4)
[^10]: [Status Code 5XX](https://tools.ietf.org/html/rfc2616#section-10.5)
