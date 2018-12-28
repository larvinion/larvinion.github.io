---
layout: post
title: "Little Endian & Big Endian"
excerpt: "Description little endian and big endian"
tags: [os, operating system, little endian, big endian]
categories: [operating system]
comments: true
---

## Little Endian & Big Endian

### 바이트 배열 방법, Byte Ordering[^1]
* Little Endian : 인텔 포맷, (작은 단위 Byte)낮은 주소 -> 높은 순으로 바이트 배열, 가산기
* Big Endian : 네트워크 포맷, (큰 단위 Byte)높은 주소 -> 낮은 주소 순으로 바이트 배열

#### Example

| 32 Bit Integer | Little Endian | Big Endian |
|:--------|:-------:|--------:|
| 0x12345678  | 0x78563412  | 0x12345678  |
| 0x0A0B0C0D  | 0x0D0C0B0A  | 0x0A0B0C0D  |


[^1]: [엔디언](https://ko.wikipedia.org/wiki/%EC%97%94%EB%94%94%EC%96%B8)
