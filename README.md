# Mohel - 온라인 역경매 플랫폼<h1>
## 🌟 Project Overview
인천일보아카데미 교육기관에서 진행한 팀 프로젝트로, <br>
'소비자가 필요한 생활 서비스를 일일이 비교하며 검색하지 않고, 편하게분야의 전문가를 찾을 수 있으면 좋겠다'라는 생각에서 만들어진프로젝트입니다. 소비자가 필요한 서비스를 등록하면 전문가들이 조건에 맞는 서비스로 응찰경쟁을 벌이고 소비자는 그중 하나를 선택하는 방식입니다. 소비자는 자신이 주도해서 매칭을 이끌어 나갈 수 있고 전문가는 각종'혜택'을 제공하면서 소비자를 유인할 수 있다는 장점이 있습니다. <br>
메세지 기능으로 소통이 가능하고, 리뷰를 통해 전문가에 대한 평가를 확인할 수 있습니다. 
 
 <br>
 
#### 사용기술
* HTML5
* CSS3
* SCSS(BEM 활용)
* JavaScript(ES6+)
* Java/JSP
* Spring
* DB(Oracle) 
#### 구현기능사항
scrollIntoView, 랜딩페이지 섹션이동 스크롤 버튼
* 회원가입/로그인/로그아웃
* 거래 상세 페이지
* 입찰하기
* 리뷰
* 마이 페이지, 프로필
* 메시지
<br>

---

<br>

### 🌟 scrollIntoView, 랜딩페이지 섹션이동 스크롤 버튼
![랜딩페이지](https://user-images.githubusercontent.com/74999421/115503645-bab0eb80-a2b1-11eb-9964-42e0926584f2.gif)

화살표 버튼에 getBoundingClientRect을 이용해 애니메이션을 주어 사용자 눈에 띌 수 있도록  구현하고, 사용자가 화살표 버튼을 클릭하면 scrollIntoView을 이용해 최상단으로 자동 스크롤 업을 할 수 있는 버튼을 구현하였습니다.
 
<br>
 
### 🌟 회원가입 / 로그인 / 로그아웃
![Authentication](https://user-images.githubusercontent.com/74999421/115509538-86412d80-a2b9-11eb-859b-1292e6bb5114.gif)
 
 <br>
 
### 🌟 거래 상세 페이지 / 입찰
![입찰](https://user-images.githubusercontent.com/74999421/115520473-29e40b00-a2c5-11eb-9919-c748ef77ab4b.gif)
 
역경매 요청글을 클릭하면 상세 페이지로 이동하고, 모달창(modal)을 이용해 입찰할 수 있도록 구현하였습니다.
모달창은 자바스크립트 이벤트리스너 추가를 하며 구현했습니다. 그리고 모달창의 닫기 버튼 말고도 모달창을 제외한 화면을 클릭해서 닫을 수 있도록 하여 사용자가 불편함 없이 사이트를 이용할 수 있습니다. 
```swift
window.addEventListener('click', (e) => {
    e.target === modal ? modal.classList.remove('show-modal') : false
});
```
window에 이벤트리스너를 추가하고 삼항연산자를 이용해 모달창 외부에서 클릭해도 닫을 수 있게 구현했습니다.

<br>
 
### 🌟 리뷰 (리뷰작성, 리뷰보기)
![리뷰](https://user-images.githubusercontent.com/74999421/115520545-3b2d1780-a2c5-11eb-8e1f-30abae1f2ae5.gif)
 
소비자 입장에서는 리뷰작성과 리뷰보기가 가능하고 전문가 입장에서는 리뷰보기가 가능합니다. 페이지에 깔끔하게 보이기 위해 리뷰작성과 리뷰보기 모두 모달창으로 구현했습니다. 
Nav bar에 드롭다운 애니메이션을 주어 편하게 페이지 이동을 할 수 있습니다.
  
<br>
 
### 🌟 메시지 (받은메시지함, 보낸메시지함, 메시지쓰기)
![메시지](https://user-images.githubusercontent.com/74999421/115526990-95c97200-a2cb-11eb-8fb7-c8686f67cada.gif)

아이디를 클릭하면 모달창으로 프로필을 확인할 수 있고, 제목을 클릭해 메시지 상세 페이지로 이동이 가능합니다. 
메시지쓰기와 답장하기 버튼을 통해 메시지 전송이 가능합니다.

<br>
