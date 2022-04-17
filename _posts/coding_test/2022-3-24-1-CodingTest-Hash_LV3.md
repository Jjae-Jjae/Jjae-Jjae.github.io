---
title: Coding Test) 전화 번호 목록 (Hash Lv-2)
layout: single
author_profile: true
read_time: true
comments: true 
share: true 
related: true 
popular: true
categories: CodingTest
tags: [Java, hash, coding test]

date: 2022-3-22T13:30:00-09:00 
last_modified_at: 2022-3-22T13:30:00-09:00 

# 목차 관련 설정
toc: true
toc_sticky: true
toc_label: 목차

# 구글 관련 설정
description: Coding Test
meta_keywords: Coding Test
---
<!-- {포스트 설명란} -->
프로그래머스 사이트 코딩테스트 고득점 Kit의 해시 부문 LV2문제의 풀이를 적어보았습니다.  
언어는 JAVA를 사용하였으며 파트에 걸맞는 Hash를 통하여 해결하였음을 참고 바랍니다.
{: .notice--primary }

## 1. 문제

### ●과제 내용  
전화번호부가 있습니다.  
전화번호부에 적힌 전화번호중  
한 번호가 다른 번호의 접두어인경우 true를,  
한 번호가 다른 번호의 접두어가 아닌 경우에는 false를  
return 하는 프로그램을 짜보자!

### ●제한 조건  
1. 전화번호부의 길이는 1 이상 1,000,000 이하 입니다.
2. 각 번호의 길이는 1 이상 20 이하 입니다.
3. 같은번호는 중복되지 않습니다.

### ●입출력 예시

| 전화번호부 | 결과 |  
|:---|:---:|  
| ["119", "97674223", "1195524421"]	| false |  
| ["123","456","789"] | true |  
| ["12","123","1235","567","88"] | false |

## 2. 문제 해결 과정
### ●요구 사항 파악  

이 문제에는 총 2가지의 요구사항이 있다고 판단된다.  

1. hash을 활용한 자료구조를 통하여 문제를 해결할것(제시항목은 아니나 주제가 hash임으로)
2. 목록에 중복되는 번호가 앞에있는 번호가 있는지 여부를 판단하는것.

### ●자료구조 선정
이 문제를 해결하기 위해선 일단 hash가 무엇인지에 대하여 집고 가야할것 같다.  

<h5> 1. hash function</h5>
hash function줄여서 hash란 n의 길이를 갖는 데이터를 고정된 길이의 데이터로 매핑하는 함수를 말한다.(단방향 암호화)  
아무리 긴 단어를 입력해도, 아무리 짧은 단어를 입력해도 정해진 형식/길이의 데이터로 변환된다.  
이 기능을 활용한 자료구조에는 크게 3가지가 있다.  
1. hash table (hash map)
2. hash set
3. bloom filter

각각의 자료구조는 아래와같은 기능을 제공한다. 
1. hash table (hash map) - 특정 값에 해당하는 정보를 저장가능
2. hash set - 중복되지 않는 명단을 작성가능 (중복 여부 판단 가능)
3. bloom filter - 집합에 존재하지 않는값을 대략적으로 파악가능(단독사용이 힘듬)

bloom filter는 데이터가 많아질수록 확률적으로 false positive를 도출할수 있기 때문에 단독으로 사용이 힘들다.
{: .notice--info}
   
bloom filter의 경우에는 단독으로 사용이 불가하기에 해당 문제에 적합하지 않다.  
hash set의 경우에는 중복되는 동명이인이 있을경우가 판단이 안되기에 적합하지 않다.  
<br>
위와 같은 이유로 중복된 값의 존재 유무를 판단하기 쉬운  
hash set을 통하여 진행하기로 하였다.

### ●해결 방법 제시

이번 문제의 해결 포인트는 번호를 앞에서부터 같은 길이로 잘랐을때   
중복되는 번호가 되는지 찾으면 해결이 되는 문제이다.   

그러므로 각 번호를 저장해 중복 검사를 해줄 hash set한개   
번호들의 길이를 저장해줄 hash set한개씩 만들어    
(번호 길이의 중복을 피하기 위하여 hash set 사용)  

중복 검사를 해줄 hash set에 모든 번호를 넣어준뒤 각 번호를   
번호 길이만큼 잘라 중복검사를 돌리면 해결이 가능할거라 생각하고 코드화 해봤다.  

### ●해결 방법 코드화
      import java.util.*;

      class Solution {
          public static boolean solution(String[] phone_book) {

              // 각 번호 저장 hash set
              HashSet<String> number_set = new HashSet<String>();
              // 번호 길이 저장 hash set
              HashSet<Integer> length_set = new HashSet<Integer>();
              
              // 번호별 길이와 접두어 추출
              for( String number : phone_book){
              	number_set.add(number);
              	length_set.add(number.length());
              }

              // 번호 길이 배열화
              Integer[] len_arr;
              len_arr = length_set.toArray(new Integer[0]);

              // 각 번호별 접두어 존재 여부 판단
              for (int i = 0; i < len_arr.length - 1; i++ ){
              	for(String number : number_set){
              		if (number.length() > len_arr[i]){
              			if( number_set.contains(number.substring(0, len_arr[i]))){
              				return false;
              			}
              		}
              	}
              }
              return true;
          }
      }