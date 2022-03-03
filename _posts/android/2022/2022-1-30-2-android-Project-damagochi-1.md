---
title: Android-2-1) Personal Project-다마고치
layout: single
author_profile: true
read_time: true
comments: true 
share: true 
related: true 
popular: true
categories: android
tags: [android,androidStudio]

date: 2022-1-29T13:30:00-09:00 
last_modified_at: 2022-1-29T13:30:00-09:00 

# 목차 관련 설정
toc: true
toc_sticky: true
toc_label: 목차

# 구글 관련 설정
description: android
meta_keywords: android
---
<!-- {프로젝트 설명란} -->
개인적으로 진행한 Android 프로젝트-Damagochi에 대하여 서술합니다.  
코드는 맨 아래 태그되어있는 GIT Hub링크에 올라가 있으니 참고 바랍니다.  
{: .notice--primary }

## 1. 프로잭트 개요  
### ● Application 종류 선정  
Android Studio를 통하여 Project를 진행하였다.  
<br>
스마트폰의 App의 강점인 **실시간** 상호작용이 가능한 Project를 진행 하고 싶었고  
이에 가장 다양하고 상호작용 뿐만아니라 **실시간** 상호 작용이 진행되는 모바일 게임을 제작하기로 하였다.  

#### ● 게임 장르 선정  
개발을 진행할 게임 주제는 육성 시뮬레이션 게임으로 선정 하였다.  
<br>
필자가 육성 시뮬레이션 게임을 좋아하는 점도 강하게 작용하였지만 모바일 게임의 특성상  
시간을 잡아 먹지 않고 간단한 조작을 통해 꾸준히 진행 할 수 있는 게임을 생각하다보니  
육성 시뮬레이션 게임장르를 선택하게 되었다.

<h4>세부 게임 선정과 그 이유</h4>
<table style="border-style:hidden; display: table;">
  <colgroup>
    <col style="width:25%;">
    <col style="width:75%;">
  </colgroup>
  <tbody>
    <tr>
      <td>
  <div markdown="1" class="ImgBox">
  <br>
  ![다마고치 사진](/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/다마고치.png)
  *다마고치 사진*
  </div>
      </td>
      <td style="font-size: 1.2em; line-height: 1.5em">      
        밴치 마킹할 표적으로는 다마고치를 선정하였다.<br><br>
        다마고치는 1990년대부터 지금까지고 계속해서 아류작과 신작이 나오는<br>
        매니아 층이 두터운 게임이다.<br><br>
        <strong>간단한 조작성</strong>과 <strong>귀여운 캐릭터성</strong>으로 신규 유저의 진입뿐만 아니라<br>
        매니아층의 소비역시 기대할수 있는 상품이다.<br><br>
        또한 캐릭터별 객체화를 통하여 향후 캐릭터의 추가나 기능의 추가등<br>
        업데이트및 유지보수가 수월하기 때문에 Project 개발 표적으로 선정하였다.<br>
      </td>
    </tr>
  </tbody>
</table>  

## 2. 프로그램 구조

### ● 기능 목록 

<table style="display: table;">
  <colgroup>
    <col style="width:50%;">
    <col style="width:50%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.2em;">
        <h3 style="margin-top:0em;">구현</h3><hr>
        1. 랜덤 캐릭터 뽑기<br>
        2. 캐릭터 돌보기<br>
        3. 캐릭터 Save & Load<br> 
      </td>
      <td style="text-align:center; font-size: 1.2em;">
        <h3 style="margin-top:0em;">미 구현</h3><hr>
        1. 상태에 따른 진화체 변경<br>
        2. 상태에 따른 돌봄 요구<br>
        3. 상태에 따른 대화<br>
      </td>
    </tr>
  </tbody>
</table>  


### ● Algorithm & Save Data(DB Table 구성)  

<table style="border-style:hidden; display: table;">
  <colgroup>
    <col style="width:50%;">
    <col style="width:50%;">
  </colgroup>
  <thead>
    <tr>
      <td style="padding:1em 1em 1em 1em; text-align:center; text-size:2em">
        <strong>Flow Chart</strong>
      </td>
      <td style="padding:1em 1em 1em 1em; text-align:center; text-size:2em">
        <strong>DB Table</strong>
      </td>
    </tr>
  </thead>  
  <tbody>
    <tr>
      <td style="padding:1em 1em 1em 1em; text-align:center">
        <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/flow_chart.png" >
      </td>
      <td style="padding:1em 1em 1em 1em; text-align:center">
        <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Table.png" >
      </td>
    </tr>
  </tbody>
</table>  

<details>
  <summary>Algorithm Flow Chart 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/flow_chart.png" style="width:100%">
  </div>
</details>

<details>
  <summary>Save Data(DB Table 구성) 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Table.png" style="width:100%">
  </div>
</details>

### ● 페이지 구성
<div markdown="1" class="ImgBox">
  <br>
  ![Page Structure](/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Page_Structure.png)
  *Page Structure*
  </div>
  
<details>
  <summary>Start Page 구성 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Start_Page.png" style="width:100%">
  </div>
</details>


<details>
  <summary>Choice_Page 구성 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Choice_Page.png" style="width:100%">
  </div>
</details>

<details>
  <summary>Choice_Dialog 구성 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Choice_Dialog.png" style="width:100%">
  </div>
</details>


<details>
  <summary>Hatchery_Page 구성 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Hatchery_Page.png" style="width:100%">
  </div>
</details>

<details>
  <summary>Game_Main_Page 구성 크게 보기</summary>
    <div>
      <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Game_Main_Page.png" style="width:100%">
  </div>
</details>

## 3. 기능 설명

### ● Start Page 기능 설명

<table style="display: table;">
  <colgroup>
    <col style="width:40%;">
    <col style="width:60%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.2em;">
        <div class="ImgBox"> 
          <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Function_StartPage.svg" style="width:100%">
        </div>
      </td>
      <td style="padding-right:5px ; font-size: 1.2em;">
        상단은 게임의 <strong>화면부</strong>, 하단은 게임의 <strong>조작부</strong>이다.<br>
        게임에 전채적으로 역동적인 느낌을 주기 위하여<br>
        캐릭터와 배경에 google에서 개발한 Glide 라이브러리를 통하여<br> 
        GIF파일로 움직이는 이미지를 삽입해주었다.<br>

        <h4>* 조작부 버튼별 역할</h4>
        -<strong>새로 시작하기</strong> : Go To Choice Page<br>
        -<strong>게임 이어하기</strong> : Game Main Page (With Save Data)<br>
        -<strong>게임 종료 하기</strong> : Close This App<br>       
      </td>
    </tr>
  </tbody>
</table>  

### ● Choice Page 기능 설명

<table style="display: table;">
  <colgroup>
    <col style="width:40%;">
    <col style="width:60%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.2em;">
        <div class="ImgBox"> 
          <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Function_ChoicePage.svg" style="width:100%">
        </div>
      </td>
      <td style="padding-right:5px ; font-size: 1.2em;">
        Choice Page는 <strong>뽑기 창</strong>과 <strong>이동 버튼</strong> 으로 구성 되어있다.<br>
        원하는 위치의 알을 선택시 Flip 애니 매이션과 함께<br>
        선택한 알의 모습을 Dialog로 띄워준다.<br><br>
        
        <strong>이동 버튼</strong> 같은 경우에는 알을 선택 후 활성화 되며<br>
        해당 버튼을 터치시 알을 부화시키는 Hatchery Page로 이동된다.<br>


        <h4>* 화면별 역할</h4>
        -<strong>빨간 영역</strong> : Egg Choice Area<br>
        -<strong>버튼 영역</strong> : Go To Hatchery Page (After Select Egg)<br>
      </td>
    </tr>
    <tr>
      <td colspan="2">
        <details style="text-align: center;">
          <summary>ChoiceDialog 보기</summary>
          <div class="ImgBox" style="display: inline-block; margin-right: 0%;">
            <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Function_ChoiceDialog.gif" style="width:80%">
          </div>
        </details>
      </td>
    </tr>
  </tbody>
</table>  



### ● Hatchery Page 기능 설명

<table style="display: table;">
  <colgroup>
    <col style="width:40%;">
    <col style="width:60%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.2em;">
        <div class="ImgBox"> 
          <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Function_HatcheryPage.svg" style="width:100%">
        </div>
      </td>
      <td style="padding-right:5px ; font-size: 1.2em;">
        Hatchery 페이지는 선택한 알을 개봉하는 페이지로<br>
        Start Page와 마찬가지로 <strong>화면부</strong>와 <strong>조작부</strong>로 나누어져있다.<br><br>

        조작부에있는 [알 흔들기]버튼을 터치시 횟수가 카운트 되며<br>
        카운트가 횟수에 도달하면 알이 깨지는 애니메이션과 함께<br>
        베이비 몬스터가 부화하여 나온다.<br>

        <h4>* 화면별 역할</h4>
        -<strong>빨간 영역</strong> : Show Egg Status at Character Image<br>
        -<strong>버튼 영역</strong> : Add to Counter Of Hatching (일정 카운트가 쌓이면 부화한다.)<br>
        -<strong>파란 영역</strong> : Show Egg Status at Text<br>
      </td>
    </tr>
  </tbody>
</table>  

### ● Game Main Page 기능 설명

<table style="display: table;">
  <colgroup>
    <col style="width:40%;">
    <col style="width:60%;">
  </colgroup>
  <tbody>
    <tr>
      <td style="text-align:center; font-size: 1.2em;">
        <div class="ImgBox"> 
          <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Function_GameMainDialog.png" style="width:100%">
        </div>
      </td>
      <td style="padding-right:5px ; font-size: 1.2em;">
        해당 페이지로 만약 Hatchery Page를 통하여 왔다면<br>
        일단 캐릭터의 이름을 만들어주어야한다.<br>
        오른쪽에 있는 이미지처럼 Dialog가 뜨며<br>
        해당 Dialog에 원하는 이름을 입력해주면 된다.
      </td>
    </tr>
    <tr>
      <td style="text-align:center; font-size: 1.2em;">
        <div class="ImgBox"> 
          <img src="/image/post/android/2022/2022-1-30-2-android-Project-damagochi-1/Function_GameMainPage.svg" style="width:100%">
        </div>
      </td>
      <td style="padding-right:5px ; font-size: 1.2em;">
        Game Main Page는 게임을 플래이하는 메인 페이지 이다.<br>
        게임의 주 목적인 캐릭터를 성장시키는 기능이 해당 페이지에 존재한다.<br>
        또한 게임의 진행사항을 저장하는 저장 버튼 역시 해당페이지에 있다.<br><br>

        Activate Buttton버튼을 누르면 캐릭터의 스테이터스가<br>
        증가/하락 하고 경험치가 증가한다.<br>
        이를통하여 캐릭터를 성장시키며 게임을 진행하게 된다.<br>

        

        <h4>* 화면별 역할</h4>
        -<strong>파란 영역</strong> : 스테이터스를 보여주며 필요한 활동이 무엇인지 알려준다.<br>
        -<strong>디스크 모양 버튼</strong> : 게임의 진행 상황을 기기의 DB에 객체화 하여 저장한다.<br>
        -<strong>빨간 영역</strong> : 캐릭터의 성장 상태를 Image를 통하여 보여준다.<br>
        -<strong>버튼 영역</strong> : Activate Buttton(해당 버튼들을 이용하여 게임을 진행한다.)<br>
      </td>
    </tr>
  </tbody>
</table>  

## 동작 시연

### ● Youtube 동영상

<style>
  .embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; }
  .embed-container iframe, 
  .embed-container object, 
  .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
</style>
<div class='embed-container'>
  <iframe src='https://www.youtube.com/embed//WeyNIx5hOoU' frameborder='0' allowfullscreen></iframe>
</div>

### ● Git Hub Repository 링크


<div markdown="1" class="ImgBox" >
  [![](/image/post/git/2021/2021-12-20-git-Hub-가입하기/Git-Hub-Logo.png)](https://github.com/Jjae-Jjae/AndroidProject_Damagochi){: text-align:center;}
    * Git Hub Repository *
</div>

