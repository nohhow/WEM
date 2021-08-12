# 4일
##  built-in function 정리
자주 사용하는 것들 위주로 정리

### Text
* AsText - Rich Text를 Text로 반환 (모든 HTML 태그 포함)
* Contains(text, subtext) - text가 subtext의 내용되는 것이 포함되는지 Boolean값으로 반환
* ToString - value to String
* Length, IndexOf, Concat 등 

### Math
* ABS - 절대값
* Ceiling - 올림
* Cos - 코사인
* Distance - 좌표값(x,y)  두 개씩을 인자로 받고 두 포인트 간 거리를 반환
* Exp - 거듭제곱
* Floor - 내림
* ToNumber - value to Number

### Date
* Date(year, month, day) - 주어진 인자에 대해서 Date를 생성
* DateDiff(date, date2, date_unit)  - date_unit에 맞게 Date간의 차이 반환
* Now() - 현재 시간 (날짜 + 시간) 반환
* Today() - 현재 날짜 반환

### Ontology
* ConceptId - Concept의 ID반환
* Description - Concept의 Description 반환
* LocalName - Concept의 LocalName으로 변환 (WebService간 통신 시 사용)
* FindConcepts (text, conceptset, include synonyms) - conceptset의 synonyms에서 text가 포함된 Concept을 찾아서 반환
> 사용 예시 : First(FindConcepts(“Male”, GetChildren([Gender]), true ))  
> 이런 식으로 작성하면 됨. WebService 통신에서 사용  
  
* GetChildren - Concept의 모든 자식 Concept 반환

### List
* RowId(list) - 리스트의 current row에 대한 RowId반환

  
## custom widget 사용 - chart
User Interaction 화면 그리기 상에서, Custom을 Drag&Drop 하여 사용
<img width="357" alt="스크린샷 2021-08-12 오전 9 33 25" src="https://user-images.githubusercontent.com/61059893/129121262-8464bb7a-4c3a-4abe-bb4d-5b2f83ca0e3d.png">


프로젝트 상에서 가진 위젯이 없다면,  Add more widgets here클릭 후
원하는 widget 다운로드 가능

Chart 생성 후 Chart로 보여질 List 선택
<img width="986" alt="스크린샷 2021-08-12 오전 9 35 42" src="https://user-images.githubusercontent.com/61059893/129121270-cf3234b4-c1e8-46fa-9060-4f9f39e86239.png">


**실제 웹 화면**
<img width="1158" alt="스크린샷 2021-08-12 오전 9 36 33" src="https://user-images.githubusercontent.com/61059893/129121288-10d7e85f-7bd2-4b89-acbe-140ee41faff6.png">
(null 은 Garbage값)


##  filter 이해
FILTER 
- DB 에 적용 - 공용
- Grid 에 적용 - 화면에서만 적용



#현장실습#
