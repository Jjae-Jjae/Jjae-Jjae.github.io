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
### ● Apach Tiles 구조
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_2.jpg)
![Framework_arki](/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Site_arki_3.jpg)
### ● MyBatis3 구조와 흐름도
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
  회원 화면은 회원와 관련된 기능들을 모아놓은 페이지이다.  
  크게 3가지 종류의 페이지로 구현되어있고 세부적인 기능은 아래와 같다.  
  > 1. 회원 가입 페이지
  > 2. 일반 회원 마이 페이지
  > 3. 관리자 계정 관리 페이지
  
  1. 회원 가입 페이지  
  > * 회원가입 유효성 체크
  > * 중복 회원 판별
  > * Post Code API (Daum API 사용)

  2. 일반 회원 마이 페이지
  > * 회원 정보 수정 기능
  > * 회원 비밀번호 수정 기능
  > * 회원 탈퇴 기능

  3. 관리자 계정 관리 페이지
  > * 일반 유저 관리 기능
  > * 일반 유저 정보 기능
  > * 유저 등급 설정 기능
  
<details>
  <summary>회원화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_2.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_3.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_4.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_5.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_6.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_7.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Member_8.jpg" >
</details>


### ● 상품
상품 화면은 상품을 회원에게 보여주고 소개하는 페이지이다.   
계정별 기능이 조금 제한되어 있다. 관리자 계정일시에만 상품 등록이 들어나게 되어있다.  
* 주요 기능
  > 1. 관리자 계정 식별 기능  
  > 2. 새 상품 등록 기능
  > 3. 전체 상품 조회 기능
  > 4. 카테고리별 조회 기능
<details>
  <summary>상품화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Product_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Product_2.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Product_3.jpg" >
</details>

### ● 예약
  예약 화면은 상품 페이지에 있는 상품들중 원하는 제품을 선택하여 예약등록 하는 페이지 이다.  
  로그인여부를 확인하여 로그인 되어있을때만 기동하며 예약에 관련된 기능들을 전반적으로 관리할수 있다.
  > 1. 로그인 확인 기능
  > 2. 예약 조회 기능
  > 3. 예약 취소 기능
  > 4. 예약 상품 검색 기능
  > 5. 예약 상품 관련 페이지 접근 기능
  
<details>
  <summary>예약화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Book_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Book_2.jpg" >
</details>

### ● 리뷰
  리뷰 화면은 작성된 리뷰들을 보여주고 예약된상품에 리뷰를 작성하는 페이지이다.
  기본적인 레이아웃은 포토 리뷰이며 별점, 사진, 내용등으로 구성되어있다.
  > 1. 리뷰 작성 기능
  > 2. 리뷰 수정, 삭제 기능
  > 3. 리뷰 작성 여부 확인 기능
  > 4. 상품별 리뷰 모아보기 기능

<details>
  <summary>리뷰화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Review_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Review_2.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Review_3.jpg" >
</details>

### ● 공지
  공지 화면은 사이트의 중요사항들을 담은 내용을 기제하는 페이지이다.  
  기본적인 게시판의 형태를 띄우고 있으며 관리자만이 작성 가능하다.  
  > 1. 관리자 계정 식별 기능  
  > 2. 공지사항 검색 기능
  > 3. 분류별 공지사항 검색 기능
<details>
  <summary>공지화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Notice_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Notice_2.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/Notice_3.jpg" >
</details>

### ● FAQ
  FAQ 화면은 사이트에서 자주 올라오는 QnA를 모아둔 게시판이다.  
  공지 화면돠 마찬가지의 형태를 띄우고 있으며 관리자만이 작성 가능하다.  
  > 1. 관리자 계정 식별 기능  
  > 2. FAQ 검색 기능
  > 3. 분류별 공지사항 검색 기능
  > 4. 테마별 공지사항 표시 기능
<details>
  <summary>FAQ화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/FAQ_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/FAQ_2.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/FAQ_4.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/FAQ_5.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/FAQ_6.jpg" >
</details>

### ● Q&A
  QnA 화면은 회원들의 문의사항을 접수하는 화면이다.
  게시판에는 답글 기능이 있고 이를 통하여 관리자만이 답변을 달 수 있다.
  > 1. 관리자 계정 식별 기능  
  > 2. QnA 검색 기능
  > 3. 답글 쓰기 기능  

<details>
  <summary>QnA화면 구조 보기</summary>
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_1.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_2.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_3.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_4.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_6.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_7.jpg" >
<img src="/image/post/java_Spring/2022/2022-2-20-1-JavaSpring-Project-Travel-Site-1/QnA_8.jpg" >
</details>

## 5. 프로젝투 후일담
  이번 프로젝트는 한달전 Spring을 배우기 전에 Java와 Servlet을 이용하여 만든 사이트를  
  Java Spring으로 이식하며 업데이트와 보완을 진행한 프로젝트 였다.   
  <br>
  Java 프로젝트를 진행했을적엔 다들 처음으로 팀 프로젝트를 진행하다보니  
  여러사람들이 규칙이나 룰등을 정하였음에도 이를 무시하고 자기 맘대로 진행하여  
  최종 Merge가 정말 힘들었던 프로젝트였다  
  (실제 프로젝트 진행후 2명이나 학원에서 퇴소 하였다 ^^;)   
  <br>
  하지만 이번 프로젝트에선 전작의 실책을 파악하여 사전에 프레임워크 제작하고   
  (사용 기술 선정, 템플릿 제작, 폴더구조 설정등)  
  사용방법들을 사전에 교육하여 원하는 방향으로 프로젝트를 진행해 나가기 위한 노력도 같이 진행하였다.  
  이를 진행하며 프로젝트진행시 코딩과 기능만의 문제가 아닌  
  서로간의 소통과 약속이 정말 중요한 점이란 것을 다시한번 체감할수 있었다.  

## 6. 동작 시연

### ● Youtube 동영상

<style>
  .embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; }
  .embed-container iframe, 
  .embed-container object, 
  .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
</style>

<style>
  .embed-container-half { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 50%; }
  .embed-container-half iframe, 
  .embed-container-half object, 
  .embed-container-half embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
</style>
<table style="border-style:hidden; display: table;">
  <colgroup>
    <col style="width:50%;">
    <col style="width:50%;">
  </colgroup>
  <tbody>
    <tr>
      <td>
        <div class='embed-container'>
          <iframe src='https://www.youtube.com/embed//m-_tUUlx4-o' frameborder='0' allowfullscreen></iframe>
        </div>
      </td>
      <td>
        <div class='embed-container'>
          <iframe src='https://www.youtube.com/embed//fgojjW_dt5I' frameborder='0' allowfullscreen></iframe>
        </div>
      </td>
    </tr>
    <tr>
      <td>
        <div class='embed-container'>
          <iframe src='https://www.youtube.com/embed//lDtWDL-aOBY' frameborder='0' allowfullscreen></iframe>
        </div>
      </td>
      <td>
        <div class='embed-container'>
          <iframe src='https://www.youtube.com/embed//kE6J7yGfDTo' frameborder='0' allowfullscreen></iframe>
        </div>
      </td>
    </tr>
    <tr>
      <td colspan="2" style="text-align:center">
        <div style="display:inline-block; width:50%">
          <div class='embed-container'>
            <iframe src='https://www.youtube.com/embed//XXmlTHWp5fk' frameborder='0' allowfullscreen></iframe>
          </div>
        </div>
      </td>
    </tr>
  </tbody>
</table>  

### ● Git Hub Repository 링크

<div markdown="1" class="ImgBox" >
  [![](/image/post/git/2021/2021-12-20-git-Hub-가입하기/Git-Hub-Logo.png)](https://github.com/Jjae-Jjae/JavaSpring_Project-TheTravel){: text-align:center;}
    * Git Hub Repository *
</div>

