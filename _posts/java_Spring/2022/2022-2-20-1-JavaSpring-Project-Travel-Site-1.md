---
title: JavaSpring-1) Team Project-여행사 차리기(TheTravel)
layout: single
author_profile: true
read_time: true
comments: true 
share: true 
related: true 
popular: true
categories: JavaSpring
tags: [JavaSpring,JDK,Java]

date: 2022-2-20T13:30:00-09:00 
last_modified_at: 2022-2-20T13:30:00-09:00 

# 목차 관련 설정
toc: true
toc_sticky: true
toc_label: 목차

# 구글 관련 설정
description: JAVA Spring
meta_keywords: JAVA Spring
---
<!-- {프로젝트 설명란} -->
팀 프로젝트로 진행된 여행사 사이트에 관하여 서술합니다. 
게시판들과 맴버 관리로 이루어집니다. 코드는 맨 아래 첨부된 GIT HUB링크를 참고하시기 바랍니다.
{: .notice--primary }

## 1. 프로젝트 개요

### ● 사이트 설명

<table style="display: table;">
  <colgroup>
    <col style="width:40%;">
    <col style="width:60%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        사이트명 : 
      </td>
      <td style="font-size: 1.2em;">
        더조은 여행 (The Travel Spring)
      </td>
    </tr>
    
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        주요 기능 : 
      </td>
      <td style="font-size: 1.2em;">
        1. 회원 가입 및 로그인을 처리한다.<br>
        2. 사이트 관리자를 지정한다.<br>
        3. 국내/해외 지역별 여행 상품을 소개한다.<br>
        4. 여행 상품을 예약하고 여행 후기를 작성한다.<br>
        5. 여행 상품/예약 관련 공지사항 및 FAQ를 제공한다.<br>
        6. 고객의 질의/응답 요청을 처리한다.<br>
      </td>
    </tr>

    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        담당 업무 : 
      </td>
      <td style="font-size: 1.2em;">
        ● 김남우 : QNA, FAQ<br>
        ● 김동현 : 상품관리<br>
        ● <Strong style="text-decoration:underline;">이재원 : 레이아웃/CSS, 회원관리, 여행후기</Strong> <br>
        ● 전희선 : 상품예약, 공지사항<br>

      </td>
    </tr>
  </tbody>
</table>  

### ● 적용 기술
  
<table style="display: table;">
  <colgroup>
    <col style="width:35%;">
    <col style="width:65%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        Apache Maven
      </td>
      <td style="font-size: 1.2em;">
        <strong>● 프로젝트 관리를 도와주는 Build Tool</strong><br>
        프로젝트 관리도구로 프로젝트의 의존성, 라이브러리, 라이프사이클 등을<br>
        POM이라는 개념을 바탕으로 관리하기 편하게 도와주는 관리도구이다.
      </td>
    </tr>
    
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        MVC Pattern<br>(Model-View-Controller)
      </td>
      <td style="font-size: 1.2em;">
        프로젝트를 구현할때 구성요소를 3가지 분할<br>
        역할별로(Model, View, Controller) 구현하는 패턴<br>
        - Model : 데이터들과 비즈니스 로직을 관리하는 파트<br>
        - View : 레이아웃과 화면을 관리하는 파트<br>
        - Controller : 이벤트들을 처리하고 모델이나 화면에 전달하는 역할 <br>
      </td>
    </tr>

    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        Apache Tiles
      </td>
      <td style="font-size: 1.2em;">
        <strong>● 페이지 레이아웃 구성</strong><br>
        반복적으로 사용되는 요소들을 이용하여 레이아웃템플릿을 정의<br>
        이를 통하여 페이지를 일관되고 확장성이 좋게 구성할수 있다.
      </td>
    </tr>

    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        Mybatis3
      </td>
      <td style="font-size: 1.2em;">
        <strong>● 자동 맵핑기능을 지원하는 프레임 워크 ORM(Object relational Mapping)</strong><br>
        JDBC를 통하여 데이터 베이스에 엑세스 하는 작업을 캡슐화하고 <br>
        SQL, 저장 프로시저, 고급 매핑을 지원하며 중복작업들을 제거하여<br>
        관계형 데이터 베이스를 보다 쉽게 구현할수 있도록 도와주는 프레임 워크이다.
      </td>
    </tr>
  </tbody>
</table>  

### ● 개발환경

<table style="display: table;">
  <colgroup>
    <col style="width:35%;">
    <col style="width:65%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        운영 체제
      </td>
      <td style="font-size: 1.2em;">
        ● Windows 10
      </td>
    </tr>
    
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        개발 Tool
      </td>
      <td style="font-size: 1.2em;">
        ● STS (Spring Tool Suite)
      </td>
    </tr>

    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        빌드 Tool
      </td>
      <td style="font-size: 1.2em;">
        ● Apache Maven
      </td>
    </tr>

    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        WAS
      </td>
      <td style="font-size: 1.2em;">
        ● Apache Tomcat v8.0
      </td>
    </tr>

    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        프레임 워크
      </td>
      <td style="font-size: 1.2em;">
        ● MVC : Spring Framework 3.1.1 (Tiles)
        ● ORM : MyBatis 3.2.8
      </td>
    </tr>
    
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        개발 언어
      </td>
      <td style="font-size: 1.2em;">
        ● Java, Servlet, JSP, HTML/CSS, JavaScript, jQuery, Ajax, EL/JSTL
      </td>
    </tr>
    
    <tr>
      <td style="text-align:center; font-size: 1.5em; font-weight:bold;">
        Database
      </td>
      <td style="font-size: 1.2em;">
        ● MySQL 5.5
      </td>
    </tr>
  </tbody>
</table>  


## 2. 사용된 프레임 워크의 구조

### ● Spring MVC 구조
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_1.jpg)
### ● MyBatis3 구조와 흐름도
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_2.jpg)
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_3.jpg)
### ● Apach Tiles 구조
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_4.jpg)
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_5.jpg)

## 3. 프로젝트 구성
### ● 사이트 맵
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_1.jpg)
### ● Tiles 레이아웃 구조
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_2.jpg)
### ● 프로젝트 폴더의 구조
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_3.jpg)
### ● DB 자료구조
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_4.jpg)
### ● DB 테이블 구성
<details>
  <summary>Member Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_5.jpg" >
</details>
<details>
  <summary>Product Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_6.jpg" >
</details>
<details>
  <summary>Product_order Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_7.jpg" >
</details>
<details>
  <summary>Review Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_8.jpg" >
</details>
<details>
  <summary>Review_image Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_9.jpg" >
</details>
<details>
  <summary>Notice Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_10.jpg" >
</details>
<details>
  <summary>QnA Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_11.jpg" >
</details>
<details>
  <summary>FAQ Table 구성 보기</summary>
  <img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_12.jpg" >
</details>
## 4. 화면별 설명
### ● 회원
### ● 상품
### ● 예약
### ● 리뷰
### ● 공지
### ● FAQ
### ● Q&A

## 5. 프로젝투 후일담



## 6. 프로젝트 시연

