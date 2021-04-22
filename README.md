# Mohel - 온라인 역경매 플랫폼
## 🌟 Project Overview
인천일보아카데미 교육기관에서 진행한 팀 프로젝트로, <br>
'소비자가 필요한 생활 서비스를 일일이 비교하며 검색하지 않고, 편하게 전문가를 찾을 수 있으면 좋겠다'라는 생각에서 만들어진 프로젝트입니다. 소비자가 필요한 서비스를 등록하면 전문가들이 조건에 맞는 서비스로 응찰경쟁을 벌이고 소비자가 전문가를 선택하는 방식입니다. 소비자는 자신이 주도해서 매칭을 이끌어 나갈 수 있고 전문가는 각종'혜택'을 제공하면서 소비자를 유인할 수 있다는 장점이 있습니다. <br>
메시지 기능으로 소통이 가능하고, 리뷰를 통해 전문가에 대한 평가를 확인할 수 있습니다. 
 
 <br>
 
#### 사용기술
* HTML5 / CSS3
* SCSS(BEM 활용)
* JavaScript(ES6+)
* Java/JSP
* Spring
* OracleDB 
#### 구현기능사항
* scrollIntoView, 랜딩페이지 섹션이동 스크롤 버튼
* 회원가입/로그인/로그아웃
* 거래글 등록
* 거래 상세 페이지
* 입찰
* 낙찰
* 마이 페이지, 프로필
* 리뷰
* 메시지
<br>

---

<br>

### 🌟 scrollIntoView, 랜딩페이지 섹션이동 스크롤 버튼
![랜딩페이지](https://user-images.githubusercontent.com/74999421/115503645-bab0eb80-a2b1-11eb-9964-42e0926584f2.gif)

화살표 버튼에 **getBoundingClientRect** 을 이용해 애니메이션을 주어 사용자 눈에 띌 수 있도록  구현하고, 사용자가 화살표 버튼을 클릭하면 **scrollIntoView** 을 이용해 최상단으로 자동 스크롤 업을 할 수 있는 버튼을 구현하였습니다.
 
<br>
 
### 🌟 회원가입 / 로그인 / 로그아웃
![Authentication](https://user-images.githubusercontent.com/74999421/115509538-86412d80-a2b9-11eb-859b-1292e6bb5114.gif)
 
 <br>
 
 ### 🌟 거래글 등록
![역경매등록](https://user-images.githubusercontent.com/74999421/115650820-f48efa00-a364-11eb-8b4e-b8f6a303003f.gif)

 역경매등록 페이지에서 필수항목에 대한 내용을 기입한 후, 마지막 항목에서 더 추가하고 싶은 조건에 대해 자유롭게 작성합니다.
 
 <br>
 
### 🌟 거래 상세 페이지 / 입찰
![입찰](https://user-images.githubusercontent.com/74999421/115520473-29e40b00-a2c5-11eb-9919-c748ef77ab4b.gif)
 
거래글을 클릭하면 상세 페이지로 이동하고, **모달창(modal)** 을 이용해 입찰할 수 있도록 구현하였습니다. 모달창은 모달창의 닫기 버튼 말고도 모달창을 제외한 화면을 클릭해서 닫을 수 있도록 하여 사용자가 불편함 없이 사이트를 이용할 수 있습니다. <br>
모달창 외부를 클릭해서 닫는 방법은 다음과 같이 구현하였는데, window에 이벤트리스너를 추가해 클릭한 대상이 부모 태그인 경우 .show-modal 클래스를 제거하도록 합니다. 자식 태그는 css 속성에서 position: absolute;로 설정되었기 때문에 자식 태그 영역 내에서는 닫기 버튼을 클릭하지 않으면 닫히지 않습니다. 클릭한 타겟이 자식 태그 영역 밖이면서 부모 태그 영역 안이기 때문에 모달창은 꺼지게 됩니다.
```swift
window.addEventListener('click', (e) => {
    e.target === modal ? modal.classList.remove('show-modal') : false
});
```

<br>

### 🌟 낙찰 프로세스
![낙찰](https://user-images.githubusercontent.com/74999421/115652863-06729c00-a369-11eb-9439-962c95812a9d.gif)

마이페이지 -> 거래상태(진행전) -> 낙찰 상세페이지 순서로 이동합니다. 낙찰 상세페이지에서 원하는 입찰자를 선택하는 버튼을 클릭하면 거래가 성사됩니다. 그리고 낙찰 상세페이지에서 거래글 수정하기, 삭제하기, 모든 입찰 거절하기 기능 또한 이루어집니다. <br>
메뉴바에는 드롭다운 애니메이션을 주어 편하게 페이지 이동을 할 수 있습니다.
 
 <br>
 
### 🌟 리뷰 (리뷰작성, 리뷰보기)
![리뷰](https://user-images.githubusercontent.com/74999421/115520545-3b2d1780-a2c5-11eb-8e1f-30abae1f2ae5.gif)
 
소비자 입장에서는 리뷰작성과 리뷰보기가 가능하고 전문가 입장에서는 리뷰보기가 가능합니다. 페이지에서 깔끔하게 보이기 위해 리뷰작성과 리뷰보기 모두 모달창으로 구현했습니다. 

<br>
 
### 🌟 메시지 (받은 메시지함, 보낸 메시지함, 메시지쓰기)
![메시지](https://user-images.githubusercontent.com/74999421/115526990-95c97200-a2cb-11eb-8fb7-c8686f67cada.gif)

아이디를 클릭하면 모달창으로 프로필을 확인할 수 있고, 제목을 클릭해 메시지 상세 페이지로 이동이 가능합니다. <br>
메시지 쓰기와 답장하기 버튼을 통해 메시지 전송이 가능합니다.

<br>
