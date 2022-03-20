---
title: Coding Test) 완주하지 못한 선수 (Hash Lv-1)
layout: single
author_profile: true
read_time: true
comments: true 
share: true 
related: true 
popular: true
categories: CodingTest
tags: [Java, hash, coding test]

date: 2022-3-19T13:30:00-09:00 
last_modified_at: 2022-3-19T13:30:00-09:00 

# 목차 관련 설정
toc: true
toc_sticky: true
toc_label: 목차

# 구글 관련 설정
description: Coding Test
meta_keywords: Coding Test
---
<!-- {포스트 설명란} -->
프로그래머스 사이트 코딩테스트 고득점 Kit의 해시 부문 LV1문제의 풀이를 적어보았습니다.  
언어는 JAVA를 사용하였으며 파트에 걸맞는 Hash를 통하여 해결하였음을 참고 바랍니다.
{: .notice--primary }

## 문제

### 과제 내용  
마라톤대회가 열렸다!  
대회에선 1명의 참여자를 제외하고 모든 선수가 완주를 하였다.  
마라톤 참여자 명단과 완주자 명단이 배열로 재공되었을때  
완주하지 못한 참여자를 return 하도록 코드를 짜보자

### 제한 조건  
1. 선수의 수는 1명 이상 10,000명 이하 입니다.  
2. 완주자의 수는 참여자의 수보다 1명 적습니다.  
3. 참가자중에는 동명이인이 있을수 있습니다.  

### 입출력 예시

| 참여자 | 완주자 | 결과 |  
|:---|:---|:---:|  
| ["leo", "kiki", "eden"] | ["eden", "kiki"] | "leo" |  
| ["marina", "josipa", "nikola", "vinko", "filipa"] | ["josipa", "filipa", "marina", "nikola"] | "vinko" |  
| ["mislav", "stanko", "mislav", "ana"] | ["stanko", "ana", "mislav"] | "mislav" |

## 문제 해결 과정
### 요구 사항 파악  

이 문제에는 총 2가지의 요구사항이 있다고 판단된다.  

1. hash을 활용한 자료구조를 통하여 문제를 해결할것(제시항목은 아니나 주제가 hash임으로)
2. 목록에서 없어진 요소 1가지를 찾을것

### 자료구조 선정
이 문제를 해결하기 위해선 일단 hash가 무엇인지에 대하여 집고 가야할것 같다.  

<h5> 1. hash function</h5>
hash function줄여서 hash란 n의 길이를 갖는 데이터를 고정된 길이의 데이터로 매핑하는 함수를 말한다.(단방향 암호화)  
아무리 긴 단어를 입력해도, 아무리 짧은 단어를 입력해도 정해진 형식/길이의 데이터로 변환된다.  
이 기능을 활용한 자료구조에는 크게 3가지가 있다.  
1. hash table (hash map)
2. hash set
3. bloom filter

<details>
  <summary>hash를 활용한 자료구조</summary>
  <div markdown= 1>
<h6>● hash table(hash map)  </h6>
> hash table과 hash map은 둘다 map형식의 자료구조이다.  
> 사용방법도 거의 동일하지만 몇가지의 차이점이 있는 자료구조이다.  
> 
> <h5>1. 공통점 </h5>
> 둘다 Key, Value로 데이터를 저장하며 데이터를 빠르게 검색, 저장, 삭제할수 있다.
> 
> 내부적인 구조는 key값을 hash function 적용하여 버킷(배열)의 index를 생성하고  
> 이에 해당하는 value를 버킷의 index에 저장하여 Key, Value 를 1대1로 매칭하기 떄문에 검색, 저장, 삭제가 가능하다.
> {: .notice--info }
> 
> <h5>2. 차이점 </h5>
> 1. hash table은 동기화 기능과 스레드 세이프티를 지원해 멀티 스레드에서 사용하기 좋고  
>     map은 위 두 기능을 지원하진 않지만 보다 빠르기때문에 단일 스레드에서 사용하기 좋다.
> 2. hash table에는 key와 value 그 어디에도 null이 들어갈수 없지만  
>     map에는 1개의 null key와 여러개의 null value가 가능하다.  
> 3. hash table은 fail fast iterator 기능을  
>     (해당 자료를 이용하여 순환도중 자료가 변경되면 오류를 발생함)  
>     hash map은 fail safe iterator 기능을 사용함  
>     (순환시 자료의 복제본을 이용하기 때문에 자료가 변경되어도 오류가 발생하지 않음)


<h6>● hash set</h6>
> hash set은 데이터를 중복되지 않고(null 포함) 비순차적으로 저장하는 자료구조이다.  
> 비선형 구조이기때문에 인덱스가 존재하지 않고 빠른 검색과 중복된 값을 골라내야할떄 많이 사용됩니다.
> 
> 내부적 구조는 제공받은 데이터를 hash function을 적용하여 버킷(배열)의 index를 생성하고 이에 저장하는 구조이다.
> 위와 같은 구조임으로 저장하는 순서대로 저장되지 않고 중복된 값의 경우에는 저장이 불가하다.
> 

<h6>● bloom filter</h6>
> 특정 값이 집합에 속해 있는지만을 검사하는 확률형 자료구조를 말한다.   
> 
> 확률형 자료구조인 이유는 가끔 틀린 사실을 도출할수도 있기 때문이다.    
> 하지만 false Negative(있는데 없다)는 발생하지 않고 false positive(없는데 있다)만이 발생한다.   
> 이 특성을 이용하여 큰 볼륨의 집합에서 특정 원소의 존재 여부를 검사할때 시간을 많이 단축할수 있다.  
> 
> 내부적인 구조는 집합에 원소를 저장할때 n개의 hash function을 통하여  
> 해당 원소의 n개의 해시를 만들고 해당하는 해시마다 마킹을 해준다.   
> 
> 원소를 검색할때는 저장할때와 같이 원소의 n개의 해시를 만들고 마킹되어있는지 확인한다.  
> 마킹이 안되어 있다면 해당 원소는 집합에 해당하지 않는다는 점을 도출해 낼수 있다. 
> 
  </div>
</details><br>

각각의 자료구조는 아래와같은 기능을 제공한다. 
1. hash table (hash map) - 특정 값에 해당하는 정보를 저장가능
2. hash set - 중복되지 않는 명단을 작성가능
3. bloom filter - 집합에 존재하지 않는값을 대략적으로 파악가능(단독사용이 힘듬)

bloom filter는 데이터가 많아질수록 확률적으로 false positive를 도출할수 있기 때문에 단독으로 사용이 힘들다.
{: .notice--info}
   
bloom filter의 경우에는 단독으로 사용이 불가하기에 해당 문제에 적합하지 않다.  
hash set의 경우에는 중복되는 동명이인이 있을경우가 판단이 안되기에 적합하지 않다.  
<br>
위와 같은 이유로 hash table (hash map)로 선정 하였고  
궂이 멀티 스레드를 사용할 이유가 없기에 싱글 스레드에서 좀더 빠른 hash map으로 자료형을 선택하게 되었다.  

### 해결 방법 제시
해당문제의 다행인 점은 참여자의 식별을 오로지 이름만을 통하여 한다는 점이다.  
만약 **jjae**란 사람이 두명이 있다고 가정해보자  
*(각* **jjae-A jjae-B** *라 칭하겠다.)*  
이중 **jjae-A**는 완주를 하였지만 **jjae-B**는 완주를 하지 못하였어도 **jjae**란 이름만을 도출하면 된다.  
고로 각 이름에을 가진 참여자가 몇명이고 이중 몇명이 완주하였는지만을 파악하면 해결된다.  
해당 사람의 순번(저장된 순서 or 앞뒤 사람)에 상관 없기때문에 이문제는 hash 자료구조를 통하여 해결할수 있는 문제이다.  

hash map을 만들어 참여자의 목록(배열)을 반복문을 통하여  
각 이름에(key) 해당하는 사람이 몇명 참여하였는지 카운팅(value) 해주고  
<br>
완주자의 목록(배열)을 똑같이 각 이름에(key) 해당하는 사람이 몇명 완주하였는지  
디스 카운팅(value) 해주면 미완주자만 표시해줄수 있을것이다.

### 해결 방법 코드화
      import java.util.HashMap;
      import java.util.Map.Entry;

      class Solution {
          public String solution(String[] participant, String[] completion) {
              HashMap<String, Integer> hm_list = new HashMap<>();          
          		String answer = "";
              // 변수 선언
      		
              for (String name_list : participant){      
                  hm_list.put(name_list, hm_list.getOrDefault(name_list, 0) + 1);
              }
              // 참여자 수 hash map에 가산
              
              for (String name_finish : completion){
              	hm_list.put(name_finish, hm_list.get(name_finish) - 1);
              }
              // 완주자 수 hash map에 감산
              
              for (Entry<String, Integer> entry : hm_list.entrySet()) {
              	if(hm_list.get(entry.getKey()) > 0){
              		answer = entry.getKey();
                  break;
              	}
              }
              // 미 완주자 검색

              /* Entry 사용 이유 : hash map의 순회하위해선  keySet(), entrySet() 를 사용해주면 되는데. 
                 keySet()의 경우에는 key의 목록만 필요할때, entrySet()의 경우에는 key, value 모두 필요할때 사용한다. 
                 이번 문제 같은경우는 key와 value둘다 필요하기 때문에 entrySet()을 사용해두는것이 보다 효율적이다. 
                 keySet()을 사용시 value값을 불러올때 매번 get()을 통하여 serch를 하여 리소스를 더 많이 잡아 먹는다. */

              return answer;
          }
      }