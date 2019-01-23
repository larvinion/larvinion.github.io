---
layout: post
title: "[부스트코스 - 웹 프로그래밍] 4일차"
excerpt: "Day 4 Boost Course Web Programming Review"
tags: [web, mooc, online course, boost course]
categories: [MOOC]
comments: true
---

# 2. HTML - FE

## 1. HTML Tags

##### HTML Tags
* 각각의 의미를 지님
* **Semantic** 한 태그
* **Semantic** 하다

##### HTML Tags의 종류
* div : Block 엘리먼트, 일반적인 영역 표현에 가장 많이 사용
* anchor, img, ul/li, heading, p 태그 등이 자주 사용

* HTML Tags List
> [w3schools HTML Tags List](https://www.w3schools.com/tags/default.asp)

{% highlight html %}
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>타이틀</title>
  </head>
  <body>
    <div>
      <h1>과일</h1>
      <ul>
        <li>사과</li>
        <li>바나나</li>
        <li>딸기</li>
      </ul>
    </div>
  </body>
</html>
{% endhighlight %}

## 2. HTML Layout 태그

##### Layout
* '배치'란 뜻, HTMl 각 태그 요소를 화면상에 어느 위치에 자리하여 구성하는 것을 결정
* header : 상단
* section
* nav : navigation
* footer : 하단
* aside

* 브라우저 버전에 따른 호환성 이슈
> 대부분의 PC **<div>의 class 이름으로 설정**, 모바일 **<header>, <footer>** 사용

![HTML Layout Tags](https://cphinf.pstatic.net/mooc/20171231_41/15146999078486r8Pv_JPEG/5086.HTML5PageLayout_2.jpg)[^1]
