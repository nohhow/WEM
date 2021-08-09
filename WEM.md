# WEM
## The world is ready for WEM
* 기술 < 경험  
* IT 직원 -> 비즈니스 관련 역할 수행
* 전통적 개발보다 10배 빠름
* javascript + html로 웬만한 custom 가능
* 모바일 서비스로 업무도구 전환 추세
* Enterprise-grade solution
* visual development : drag&drop으로 개발 수행
* 협업 가능

## What is WEM
* cloud-based 어플리케이션 개발 플랫폼
* 빠름
* 웹, 모바일 동시 개발 가능

## Introduction to WEM
* .NET
* AJAX
* Javascript
* HTML/CSS
* 등

## Concepts and Tutorials

### Ontology
* Concept Set
	- Concept 

### remote data sources  
- Odata - 엑셀과 연동
### real-time messages  
- vote program : 투표 결과 즉각 보여주는 등 (프로그램 간 통신)

### Widget 
- 부분적 화면 구성 (HTML + Js)
- <img width="1904" alt="스크린샷 2021-08-10 오전 12 39 58" src="https://user-images.githubusercontent.com/61059893/128733774-6727c50c-5eef-40ce-9be8-9cd36af85120.png">

### Basic Layout
* Header
* menu bar
* main

### Flowcharts

action flowchart : user-interaction 이 없이 흘러가는 흐름
regular flowchart : user interaction 포함

* user-interaction
* end
* enter-sub-flowchart : 서브 플로우차트에서 반드시 메인 플로우 차트로 복귀한느 것이 원칙이다. (마지막은 end 노드로 끝내야함.), 복잡도를 낮추기 위해서는 여러 개의 서브 플로우 차트를 사용하는 것이 좋다.
* Decision : if문
* List Action : 데이터 조작 노드, 데이터 삭제 생성 모두
* Loop : 데이터 조작 노드, 데이터 패치(꺼내올 때) 할 때 사용
* Save-DB : 트렌젝션 (시작과 끝 점을 가지는 가운데 그 흐름을 포함하는 단위)은 실행되거나 무시되거나 그 중간은 없다.
* HTTP request node : REST 지원, get post, rest call node
* excute process : send email, sleep 등 기능 지원
* Comet message : real-time message (send listening)

> 세션 : 클라이언트와 서버 간에 연결  


### Exits
노드를 마치며(벗어나면서) 시작될 동작 정의 (Default Exit, Error), 모든 노드는 EXIT를 가진다.


### Data Model 
* transient list : 가변성 테이블 (어플 종료시에 함꼐 제거)
* database list : 데이터베이스에 저장

	Field
	- text 
	- rich text : html 문서라고 보면 된다.


reference variable : 레퍼런스 변수, 테이블 간에 연결을 위해 사용(중복 방지) N:N 관계에서 사용

* Concept : 상속과 비슷한 개념, TabBar 만들 때 사용가능, (with Ontology)
-> 예를 들어 상위 구조에 변수 타입을 지정하면 하위에도 적용된다. Javascript의 Prototype?

