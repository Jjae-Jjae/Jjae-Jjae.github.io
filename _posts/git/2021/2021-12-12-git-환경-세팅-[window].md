---
title: Git 환경 세팅-[Window]
layout: single
author_profile: true
read_time: true
comments: true 
share: true 
related: true 
popular: true
categories: Git
tags: [Git,깃]

date: 2021-12-12T13:30:00-09:00 
last_modified_at: 2021-12-12T13:30:00-09:00 

# 목차 관련 설정
toc: true
toc_sticky: true
toc_label: 목차

# 구글 관련 설정
description: Git을 사용하기 위한 셋팅을 진행하는법을 알아본다
meta_keywords: Git, Git Hub, Git 세팅, Git 환경 세팅, Git 설치, Git Hub 설치
---
이번 글에선 Window OS에서의 Git의 환경 세팅에 대하여 서술 할려 한다.<br>
OS 별로 설치 방법이 달라 각각 나누어 설명하니<br>
다른 OS라면 해당하는 설치법을 참고하도록 하자.


 º Git<br>
 º Git Hub<br>
 º Git이 지원되는 IDE(통합 개발 환경)<br>    { ex - eclipse, Visual Studio, VS Code, Android Studio 등)<br>
{: .notice--info}

위 박스에 서술되어 있는 3가지를 세팅을 할 예정이다.

## step 1 - Git 설치하기

자 일단 가장 먼저 지금부터 사용할 Git을 설치해볼 것이다.<br>
Git을 설치할때는 운영체제 마다 설치 방법이 다르다.

### 1. Git의 파일을 다운 받기

<hr>
[![텍스트](https://git-scm.com/images/logo@2x.png){: width="50%" height="50%"}](https://git-scm.com/){: target="_blank"}
[다운로드 링크](https://git-scm.com/){:target="_blank"}
<hr>
 
위 링크로 접속하면 아래와 같은 화면이 나오는데<br>여기서 **빨간색 박스**를 클릭하면 자동 다운로드가 진행된다.
 
![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_down_%20(1).png){: .align-center width="50%" height="50%"}
 
<details>
  <summary>만약 자동 다운이 진행되지 않는다면</summary>
  <div markdown = "1">
  <br>

  ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_down_%20(2).png){: .align-center width="50%" height="50%"}

  위 이미지의 빨간 네모를 클릭하면 수동으로 다운 받을 수 도 있다.
  </div>
</details>
<br>

### 2. 설치 진행하기
<br>
다운로드가 완료된 파일을 더블 클릭하여 설치를 진행한다.<br>

<hr>

**옵션 셋팅**
> 1. Next를 눌러 진행한다 <br>
> (필자는 재설치중이기에 아래에 Only Show 뉴 옵션이란 창이 떠있지만 무시 바란다.)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(1).png){: .align-center width="50%" height="50%"}
>  <br><br><br>
> 
> 2. 자신이 원하는 설치경로를 지정해준다.<br>
> (당연히 기본 설치경로를 추천한다.)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(2).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 3. 이곳에선 자신이 원하는 부분만 선택하여 셋팅 해주면 된다.<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(3).png){: .align-center width="50%" height="50%"}
> <br><br>
> ```
>       1.Additional icons
>           > On the Desktop : 바탕화면에 아이콘 생성
> 
>       2.Windows Exporer integration
>           > Git Bash Here : Git Bash를 폴더에서 우클릭을 통해 바로 해당 폴더경로로 실행하는 기능
>           > Git GUI Here : Git GUI를 폴더에서 우클릭을 통해 바로 해당 폴더경로로 실행하는 기능
> 
>       3.Git LFS (Large File Support) : 용량이 큰 파일 지원
>
>       4.Associate .git configuration files with ~ : git 구성파일을 기본 텍스트 편집기와 연결
>
>       5.Associate .sh files to be run with Bash : 확장자.sh 파일을 Bash와 연결
>
>       6.Check daily for Git for Windows updates : Git 업데이트를 여부를 매일 확인
>
>       7.(NEW!) Add a Git Bash Profile to Window Terminal : Window 터미널에 Git Bash Profile을  
>```
> 4. 시작메뉴에서 어떤 폴더에 Git을 넣어둘지를 선택하는 옵션.<br>
> (Don't create a Start Menu folder 를 선택하면 시작메뉴에 추가하지 않습니다.)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(4).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 5. Git을 사용할 기본 에디터를 선택하는 옵션<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(5).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 6. 기본 브렌치 이름을 어떤것을 사용할지에대한 옵션<br>
> (Let Git decide 추천)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(6).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 7. Git 명령어를 어디서 사용할지 선택하는 옵션.<br>
> (Git from the command line and also from 3rd-party software 추천)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(7).png){: .align-center width="50%" height="50%"}
> <br><br><br>
>
> 8. 어떤 SSH를 사용할지에 대한 선택 옵션<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(8).png){: .align-center width="50%" height="50%"}
> <br><br><br>
>
> 9. https 전송시 어떤 인증서를 사용할지에 대한 옵션<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(9).png){: .align-center width="50%" height="50%"}
> <br><br><br>
>
> 10. Git 저장소에 Checkout 할때 줄 바꿈 을 어떤 명령어로 할지에 대한 옵션<br>
> (unix : "&#8361;n", Window :  "&#8361;n")<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(10).png){: .align-center width="50%" height="50%"}
> <br><br><br>
>
> 11. 터미널 에뮬레이터를 선택하는 옵션<br>
> (Use MinTTY : Git Bash, Use Windows : CMD)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(11).png){: .align-center width="50%" height="50%"}
> <br><br><br>
>
> 12. Git Pull 할떄의 deFault 전략 설정<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(12).png){: .align-center width="50%" height="50%"}
> <br><br><br>
>
> 13. Credential Helper의 사용여부를 묻는다<br><br>
> Credential Helper란 <br>(HTTP 프로토콜 사용 시 매번 입력하여야하는 인증정보를 자동으로 입력해주는 시스템이다.)<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(13).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 14.  부가적인 옵션을 선택하는 부분이다<br><br>
> Enable file system  : 성능향상을 위해 파일 시스템 데이터를 메모리에 캐시
> Enable symbolic links : symbolic links 활성화<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(14).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 15. 실험옵션 선택란이다 넘기자<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(15).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 16. 설치 셋팅을 끝냈으면 자동으로 설치가 진행된다.<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(16).png){: .align-center width="50%" height="50%"}
> <br><br><br>
> 
> 17. 설치 완료<br>
> Finish 버튼을 눌러 이 지겨운 창을 닫아주자<br><br>
> ![Git Down](/image/post/git/2021/2021-12-12-git-사용법/git_setup_%20(17).png){: .align-center width="50%" height="50%"}
> <hr>


<br>

 ### asdas
 
