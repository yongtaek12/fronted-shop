# vue.js 쇼핑몰 
### 1 개요
*  프로젝트명 :  vue.js 와 spring boot 활용한 쇼핑몰 어플리케이션 
*  개발인원 : 1
* 개발기간 : 2023.08.02 ~ 2023.08.11
* 내용 : SpringMVC 패턴을 로그인 게시판
* 주요 기능 : 
  * 쇼핑몰 - 주문하기, 주문목록조회, 장바구니 담기
  * 사용자 - 로그인, 로그아웃, 유효성 검사 및 중복 검사 <br>
* 개발언어 : JAVA 17
* 개발환경 : Spring boot 3.1.2, vue 3.3.4,  Bootstrap 
* 데이터베이스 : mariaDB 10.9.7
* 형광관리 : Git
### 2 요구사항 분석
  #### 1. 로그인 페이지
* 유효성 검사
  * 로그인 시 데이터를 토큰(Token)으로 치환하여 원본데이터 대신 토큰을 사용
  ![image](https://github.com/yongtaek12/fronted-shop/assets/72364856/d7cbbf52-9106-4dc6-a274-2c149dcf55f6)
* 중복확인
  * 데이터베이스에 존재하는 이름 또는 아이디를 입력한 채 회원가입 버튼을 누른 경우 "이미 사용중인 아이디입니다."의 메시지를 보여주기
  * 모든 검사가 통과되었다면 로그인 페이지로 이동시키기
 #### 2. 로그인 페이지
  * 로그인을 하지 않은 경우 아래 페이지만 이용가능
    * 로그인 페이지
    * 메인 페이지
  * 로그인 검사
    * 아이디와 비밀번호가 일치하지 않을 시 "아이디 또는 비밀번호가 일치하지 않습니다. "의 메시지를 보여주기
    * 다른 아이디로 작성한 글 수정 불가능
 #### 3. ERD
  ![image](https://github.com/yongtaek12/fronted-shop/assets/72364856/ae6ef56a-3632-4a35-a835-7d29b2c0c14a)

  
#### 1. 로그인 주문상품 장바구니 담기
![뷰쇼핑몰1]()
<img width="80%" src="[https://github.com/yongtaek12/fronted-shop/assets/72364856/7ddb54d6-4da5-4ddc-ab0a-cf0ee82cdefc.gif](https://github.com/yongtaek12/fronted-shop/assets/72364856/18a5c329-b68d-4b2e-a200-bb73426d5ad4)"/>

#### 2. 주문하기
<img width="80%" src="https://github.com/yongtaek12/fronted-shop/assets/72364856/8a7d6665-9e38-46fa-a587-2847803e550c.gif"/>




 
# vue.js 셋팅

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
