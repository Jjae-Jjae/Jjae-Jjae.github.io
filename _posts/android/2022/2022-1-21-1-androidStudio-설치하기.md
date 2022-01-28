---
title: 1] androidStudio 설치하기
layout: single
author_profile: true
read_time: true
comments: true 
share: true 
related: true 
popular: true
categories: android
tags: [android,androidStudio]

date: 2022-1-20T13:30:00-09:00 
last_modified_at: 2022-1-20T13:30:00-09:00 

# 목차 관련 설정
toc: true
toc_sticky: true
toc_label: 목차

# 구글 관련 설정
description: android Studio 설치하기
meta_keywords: androidStudio, androidStudio 설치, 안드로이드 스튜디오 설치, 안드로이드 스튜디오
---
안드로이 스튜다오를 설치하는 법을 기술합니다.  
차분히 따라하면 누구나 설치가능하도록 작성합니다.  
오류 발견시 업데이트 하도록 하겠습니다.  
감사합니다.
{: .notice--primary }


# Android Studio 란?

<table style="border-style:hidden; display: table;">
  <colgroup>
    <col style="width:30%;">
    <col style="width:70%;">
  </colgroup>
  <tbody>
    <tr>
      <td>
  <div markdown="1" class="ImgBox">
  <br><br>
  ![나뭇가지 아이콘](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/studio_logo.png)
  <br><br>
  </div>
      </td>
      <td style="font-size:1.4em">
        Android 개발을 위해 Google 제공하는 IDE(통합개발환경)이다.<br>
        <br>
        프리웨어 이며 기존 Eclipse를 밀어내고 Android 공식 IDE가 되었다.<br>  
        <br>
        Android 공식 프로그래밍 언어인 Kotlin을 사용 가능하다.<br>
        또한 Gradle지원과 IntelliJ IDEA기반으로 많은 편의성을 제공하여 많은 Android 개발자가 사용중이다.
      </td>
    </tr>
  </tbody>
</table>

# Android Studio 설치하기
<div markdown="1" class="ContentBox">

<h3> 만약 특정 JDK 버전을 사용해야 할경우 </h3>

안드로이드 스튜디오에선 ADK(Android Develop Kit)을 통하여 Open JDK를 제공해준다.  
따라서 별도의 JDK를 설치할 필요는 없지만 만약 **특정버전의 JDK**를 사용해야한다면
아래 링크를 따라 들어가 설치하고 오자.

[JDK 설치하기](https://jjae-jjae.github.io//java/1-JDK-설치하기/)
<!-- [JDK 설치하기](http://localhost:4000/java/1-JDK-설치하기/) -->

</div>


[안드로이드 스튜디오 설치](https://developer.android.com/studio/install?hl=ko)  
해당 링크로 들어가면 안드로이드 스튜디오에서 제공하는 설치 설명을 볼수 있다.  
필자도 이를 토대로 설명을 진행할 예정이다.
{: .notice--info}

<div class="ContentBox" >
  <table style="border-style:hidden; display: table;">
    <colgroup>
      <col style="width:40%;">
      <col style="width:60%;">
    </colgroup>
    <tbody>
      <tr>
        <td>
          <div class="ImgBox">
            <a hrfe="https://developer.android.com/studio?hl=ko" style=" text-align:center;">
              <img src="/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_logo.png" style="margin-bottom:10px;">
              * 다운로드 링크 *
            </a>
          </div>
        </td>
        <td style="font-size:1.4em">
        옆에있는 링크로 들어간뒤 해당 글의 순서를 따라 설치를 진행할 예정이다.
        </td>
      </tr>
    </tbody>
  </table>
</div>

* <h5>파일 다운받기.</h5>  
  위 링크로 접속 하였다면 아래이미지와 같은 창이 나올 것이다.  
  아래 창에서 빨간 칸을 누르면 자신의 os에 맞는 버전이 다운될것이다.  
  (만약 그렇지 않다면 파란 칸을 눌러 버전을 선택해주자.)

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_1.png){: .align-center width="70%" height="50%"}
<br>
<br>
![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_3.png){: .align-center width="70%" height="50%"}
<hr>
* <h5>exe파일 실행하기.</h5>   
  파일 다운로드가 다완료되었다면 파일을 더블클릭해 실행하여주자.

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_4.png){: .align-center width="70%" height="50%"}
<hr>
* <h5>설치 진행하기</h5>   
  파일이 준비가 다 되었다면 아래와 같이 설치 마법사가 실행되었을 것이다.  
  안내에 따라 계속 NEXT 버튼을 눌러주면 끝이다.

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_6.png){: .align-center width="70%" height="50%"}  

**여기서 잠깐!**  
Android virtual Device 항목은 안드로이드 앱을 테스트 해볼 스마트폰 VM을 설치할지를 묻는 항목이다.  
불편하게 항상 안드로이드 폰을 연결하여 테스트 해줄게 아니면 꼭 체크하자.
{: .notice--info}

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_7.png){: .align-center width="70%" height="50%"}

NEXT 버튼을 클릭한다.  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_8.png){: .align-center width="70%" height="50%"}

NEXT 버튼을 클릭한다.  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_9.png){: .align-center width="70%" height="50%"}

로딩을 기다렸다가 NEXT 버튼을 클릭한다.  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_10.png){: .align-center width="70%" height="50%"}

NEXT 버튼을 클릭한다.  
여기까지가 딱 설치만 하는 과정의 끝이다.  


![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_11.png){: .align-center width="70%" height="50%"}
<hr>


# Android Studio 설정

## 설정파일 적용하기.
해당 항목은 안드로이드 설정파일을 적용하는 항목이다.  
첫 설치라면 없을태니 아래쪽 do not import 항목을 체크해주자.  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_12.png){: .align-center width="70%" height="50%"}

ok 버튼을 누르고 나면 이쁜 여우가 나올것이다.  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_13.png){: .align-center width="70%" height="50%"}

로딩이 끝난뒤 IDE 사용에대한 내용을 Google과 공유 할 것인지 물어본다.  
사용자가 원하는대로 체크한뒤 넘어가자.

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_14.png){: .align-center width="70%" height="50%"}

* <h5>설치중 환경 설정하기.</h5>
  
기본적으로  Standard를 선택해주면 된다.  
하지만 만약 JDK위치를 설정해주어야 하거나, 사용하지 않을 컴퍼넌트들을 설정할 정도의 고수라면  
Custom을 선택하면 된다! (물론 그런고수면 이글을 안보겠지만 말이다...)  


![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_24.png){: .align-center width="70%" height="50%"}

자 Next를 눌러 설치를 진행하자.  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_15.png){: .align-center width="70%" height="50%"}

<details>
  <summary>Custom 세팅 보기</summary>
  <div markdown= 1>
    
  JDK 경로 설정  
![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_16.png){: .align-center width="70%" height="50%"}  
  UI 모드 설정하기  
![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_17.png){: .align-center width="70%" height="50%"}
  SDK 컴포넌트 선택
![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_20.png){: .align-center width="70%" height="50%"}
  </div>
</details>

세팅값을 보여준다.  
![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_21.png){: .align-center width="70%" height="50%"}

(원래대로라면 맨 아래에 실패가 뜨지 않는다! 참고하자!)  

![android Down](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/android_22.png){: .align-center width="70%" height="50%"}

## Android Studio SDK 설정하기.

인제 IDE는 설치를 다 해주었으니 안드로이드 SDK를 설치해줄 차례이다!  
SDK는 Software Develop Kit의 약자로 소프트웨어를 개발하기 위한 도구들의 모음집이다!  

AndroidStudio를 실행하였다면 아래와 같은 화면이 뜰것이다.  
해당 창에서 More Action을 눌러 SDK Manager을 눌러 설정창을 띄워주자.  

![android SDK-2](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_2.png){: .align-center width="70%" height="50%"}  

아래와 같이 창이 열렸다면 다운 받을 SDK Platform을 선택해주면 된다.  
(여기서 선택된 Platform 버전으로 안드로이드는 앱을 빌드하게된다.)

![android SDK-3](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_3.png){: .align-center width="70%" height="50%"}  

다 선택하였다면 Apply 버튼을 눌러 SDK Platform 다운로드를 진행하자!  
OK ->

![android SDK-4](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_4.png){: .align-center width="70%" height="50%"}

NEXT 버튼을 눌러주면 다운로드가 자동으로 진행된다.  

![android SDK-5](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_5.png){: .align-center width="70%" height="50%"}  

SDK Tools 탭으로 이동하여준다.  
해당탭에선 SDK Tool들을 선택할수 있는데 여기선.

> * Android SDK Build-Tool
> * Android SDK Platform-Tool
> * Android SDK Tool
> * Android Emulator + [자신의 CPU에 맞는 Emulator]  
  
추가적으로

> * Google USB Driver
> * Google WEB Driver
> * Google Play Service  
  
이렇게 체크해주고 넘어가자

(해당 탭을 보면 맨 아래 Hide Obsolete Packages란 체크박스가 있는데 체크 해제를 하여야 모든 기능이 보인다.)

![android SDK-6](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_6.png){: .align-center width="70%" height="50%"}  

Platform 을 설치해줄 때와 마찬가지로 Apply 버튼을 눌러 다운을 진행해주면 아래와 같이 나온다.  
OK 버튼을 통해 다운을 진행하자.

![android SDK-7](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_7.png){: .align-center width="70%" height="50%"}  

NEXT버튼을 누르면 다운로드가 진행되는데  
[자신의 CPU에 맞는 Emulator] 때문에 ok버튼을 눌러야하는 창이 뜬다. OK 버튼을 눌러 진행해주자  

간혹 [자신의 CPU에 맞는 Emulator] 설치 진행중 Error가 나서 진행이 안되는 경우가 있는데  
그럴경우 BIOS에 들어사 CPU virtual기능을 켜주면 해결된다.
{: .notice--info}

![android SDK-8](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/Android_SDK_8.png){: .align-center width="70%" height="50%"}


## Android Studio AVD 설정하기.

AVD는 Android virtual Device 의 약어로 Android Studio에서 개발하는 앱을  
별도의 장치 없이 자체적으로 테스트 해볼수 있는 가상 머신이다.

SDK Manager에 들어갈때와 마찬가지로 More Action을 눌러 AVD Manager을 눌러 설정창을 띄워주자.  

![android AVD-1](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_1.png){: .align-center width="70%" height="50%"}

만든 Device가 없다면 아래와 같이 Create virtual Device 버튼이 있다.   
이 버튼을 눌러 Device 설정창을 켜 새로운 Device 를 만들어 주자.  

![android AVD-2](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_2.png){: .align-center width="70%" height="50%"}  

이 창에선 자기가 개발할 기기의 종류를 선택할수 있다.  
자신이 개발할 하드웨어에 최적화 되어있는 장치를 선택하여 진행하자.  

![android AVD-4](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_4.png){: .align-center width="70%" height="50%"}

기기를 선택하였다면 OS 버전을 선택할 차례이다.  
원하는 OS 를 선택하여 설치하고 NEXT를 눌러 진행하자.  
(만약 이미 OS중 Download 받은게 있다면 OS 버전 아래에 Download 버튼이 없을것이다.)

![android AVD-7](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_7.png){: .align-center width="70%" height="50%"}

기기의 설정을 진행하는 창이다.  
여러 항목이 있으니 자신이 원하는데로 선택해주면 된다.  
(Show Advanced Setting 버튼을 누르면 상세 설정이 나온다.)

![android AVD-9](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_9.png){: .align-center width="70%" height="50%"}

(상세 설정창)  

![android AVD-8](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_8.png){: .align-center width="70%" height="50%"}

아래와 같이 생성이 완료 되었으면 오른쪽에 있는 실행 버튼을 눌러 AVD를 실행하자.  

![android AVD-11](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_11.png){: .align-center width="70%" height="50%"}

제대로 설정 되었다면 아래와같이 virtual Device창이 켜질것이다.  
(오른쪽 메뉴바에 있는 전원 버튼을 눌러야 Device의 전원이 켜진다.)


<table style="border-style:hidden; display: table;">
  <colgroup>
    <col style="width:50%;">
    <col style="width:50%;">
  </colgroup>
  <tbody>
    <tr>
      <td>
  <div markdown="1" class="ImgBox">
  <br><br>
  *전원 꺼진 모습*
  ![android AVD-12](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_12.jpg){: .align-center width="70%" height="50%"}
  <br><br>
  </div>
      </td>
      <td>
  <div markdown="1" class="ImgBox">
  <br><br>
  *전원 켜진 모습*
  ![android AVD-13](/image/post/android/2022/2022-1-21-1-androidStudio-설치하기/AVD_Setup_13.png){: .align-center width="70%" height="50%"}
  <br><br>
  </div>
      </td>
    </tr>
  </tbody>
</table>