# **MADCAMP_1주차**
### 개발기간 : (1주일) 2022. 06. 30 ~ 2022. 07. 06

### **Team**
- 장지원 (부산대학교 정보컴퓨터공학 19) 
- 김찬우 (카이스트 전산학부 20)


### **Enviorment**
- **Language**: Kotlin
- **program** : Android Studio VERSION 11 
- **API** : 33

### **Overview**
- Fragment, Adapter, Permission(전화, 갤러리, 지도), Event Listener, 
- Contact, Gallery, Map 기능을 가진 3개의 탭으로 구성된 안드로이드 어플리케이션이다.   
- 각각의 탭은 Fragment로 구현하였으며, tablayout을 이용하여 탭 간 전환을 구현하였다.

### **TAB 1: Contact**
- 처음에는 Asset 폴더에 json file을 만들어서 불러오는 방식이었지만 나중에 연락처 연동 방식으로 수정했다.
- 휴대전화의 연락처와 연동하여 이름과 전화번호를 보여주는 탭이다.
- listview를 기반으로 adapter를 통해 customize하였다.
- 상단의 검색바는 이름을 기준으로 해당하는 연락처를 필터링해준다.
- 검색바는 searchview를 통해 구현하였다.

![20220705144938-7c011ad592 gif-2-mp4 com](https://user-images.githubusercontent.com/83392219/177321506-c55ae5db-56a1-4e8e-bfca-0e3e89a9ac55.gif)


### **TAB 2: Gallery**
- 휴대전화의 갤러리와 연동하여 원하는 사진을 선택하여 가져오는 탭이다.
- 선택하는 사진의 개수에 상관없이 원하는 만큼 화면에 추가할 수 있다.
- recycleview의 grid layout을 사용하여 커스터마이징하였다.
- 화면에 추가된 사진을 누르면 해당 사진만 확대하여 보여주는 팝업 기능을 추가하였다.
- 새로고침 버튼을 누르면 선택한 사진을 화면에서 지울 수 있다.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83392219/177326246-14d4d2af-9b66-45ba-bd60-0f8d8b8fc619.jpg" width="20%" height="20%">
  <img src="https://user-images.githubusercontent.com/83392219/177326303-0b201b23-9e58-450c-8a34-b87a5cf72c15.jpg" width="20%" height="20%">
</p>




### **TAB 3: Map**
- Naver Map API를 연동하여 지도를 보여준다.
- 경도와 위도 좌표 값으로 현재 위치를 지도 상에 나타내고 마커로 표시하였다.
- 지도에서 새로운 위치를 클릭할 때마다 바뀌는 주소 값을 구하였고 이것을 마커와 토스트 메시지로 표시하였다.

<p align="center">
  <img src="https://user-images.githubusercontent.com/83392219/177326420-a48e0175-703e-40a4-818c-84b24136d7f7.jpg" width="20%" height="20%">
  <img src="https://user-images.githubusercontent.com/83392219/177326452-f0892040-1adb-453b-9e43-75a1991e3782.jpg" width="20%" height="20%">
</p>


### **UI** ###
- 애플리케이션 아이콘 변경
- 탭 레이아웃의 각 탭을 아이콘으로 변경



### **Error Handling** ###
- 처음에는 Activity에서 3개의 Tab을 intent로 연결하여 구현했으나 Activity의 동작이 무거워서 애뮬레이터가 갑자기 중단되는 상황이 발생하였다. 그래서 각 탭을 Fragment로 바꿨다.
 
