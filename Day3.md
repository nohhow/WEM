# 3일

## Tab Bar
1. Ontology 생성
2. Concept Set 생성
3. 하위 Concept 생성
4. TabBar Drag&Drop
5. Conditional과 함께 사용 시 시너지 UP

여러 개의 Interaction을 사용해야할 것을 단 한 페이지에 TabBar와 함께 정리 가능
<img width="1904" alt="스크린샷 2021-08-10 오전 12 57 53" src="https://user-images.githubusercontent.com/61059893/128740082-3b359d63-6fca-47fb-a8ae-d55d9b5967af.png">


### Tab Bar 사용 시, 장점과 단점

**Tab Bar 사용 시 장점**
- 한 페이지에 모두 정리 가능 (여러 개의 interaction 사용 필요 없음)
- 탭 간 이동에도 페이지가 전환되지 않아서 정보 유지에 유리함
  
> Tab Bar 사용 FlowChart  

<img width="777" alt="스크린샷 2021-08-10 오전 1 03 27" src="https://user-images.githubusercontent.com/61059893/128740102-5aaddfef-5fc6-42bd-8730-8b734b608df5.png">


**Tab Bar 사용 시 단점**
* 탭 바 사용 시에는 Validation Rule이 제대로 적용되지 않을 수 있음 (현재 보고 있는 탭에서만 동작 할 수도 있음(Conditional 사용시)
* 필수입력 form 입력에 대한 validation도 불가할 수 있음.(Conditional 사용 시) 주의해야함.
* Flowchart에서 한 눈에 진행 흐름을 살펴보기 어려울 수도 있다.
   
> Tab Bar 미사용 FlowChart  

<img width="1054" alt="스크린샷 2021-08-10 오전 1 04 50" src="https://user-images.githubusercontent.com/61059893/128740119-567a60e7-6d92-4d81-bee1-be8969fca26c.png">


## Fragment
* 6번째 탭에서 Template fragments 생성가능
* Widget이라고 이해하면 됨. HTML과 JS가 작성되어 하나의 기능을 수행하는 요소
* 자체적으로 로직 수행이 가능해야함.(응집도 높아야함)

<img width="288" alt="스크린샷 2021-08-10 오전 1 06 39" src="https://user-images.githubusercontent.com/61059893/128740132-1e8dfffa-e498-42de-83c8-5e4f30014323.png">



## User Enrollment
* 유저 등록 테이블 구성
* 하위에 추가적인 LIST 생성 및 활용 전략
* 새로운 LIST를 사용하여 input 할 예정이 있다면 반드시 추가적인 ADD ROW가 필요하다. (상위 LIST만 ADD ROW하면 안 된다는 말이다.)

<img width="281" alt="스크린샷 2021-08-10 오전 1 08 54" src="https://user-images.githubusercontent.com/61059893/128740189-f11eb508-f1e6-4223-b9aa-42ab7acbfb22.png">


### Password 생성 및 보안 전략
Password Hash + Salt + Pepper 전략

* Password는 관리자도 절대 알아서는 안된다.
* 사용자만 Password를 알 수 있어야 한다.

그렇다면 어떻게 해야할까?

`hash(사용자 Password + Salt + Pepper) -> 강력한 암호화된 Password 생성`

** salt : 함수를 통해서 생성된 32자리의 랜덤한 문자열을 저장
** Pepper : 관리자가 임의로 작성한 예측할 수 없는 문자열을 저장
** hash () : 해시 함수, 인자로 받은 문자열을 숨겨주는 역할을 수행.

사용자 Password는 암호화는 있지만 복호화 방법이 없다.
따라서 암호화 : 암호화가 일치하는지를 확인해야한다.

사용자는 Password를 정하고, 프로그래머는 임의로 생성된 32자리 수의 문자열을 더하고, 예측하기 어려운 문자열을 덧붙인다. 

이렇게 완성된 긴~~ 문자열을 hash함수를 통해서 숨겨줄 수 있다. 즉 암호화할 수 있다.
이렇게 암호화 된 문자열은 사용자가 로그인 할 때에, 사용자 password를 입력받아, 일전에 hash함수까지 적용하는 과정들을 다시 한 번 적용하여 기존의 passwrod Hash와 일치하는지 확인하는 방법을 통해서 사용자 로그인을 구현할 수 있다.

> 참고로 WEM에서는 hash함수를 PBKDF2(사용자 Password, Salt(추가할 문자열들))를 사용한다.  




#현장실습
