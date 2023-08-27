# vue.js 쇼핑몰 
### 1 개요
*  프로젝트명 :  vue.js 와 spring boot 활용한 쇼핑몰 어플리케이션 
*  개발인원 : 1
* 개발기간 : 2023.08.02 ~ 2023.08.11
* 내용 : SpringMVC 패턴을 로그인 게시판
* 주요 기능 : 
  * 쇼핑몰 - 로그인, 로그아웃, 주문하기, 주문목록조회, 장바구니 담기
  * 사용자 - Security 회원가입 및 로그인,  유효성 검사 및 중복 검사 <br>
* 개발언어 : JAVA 17
* 개발환경 : Spring boot 3.1.2, vue 3.3.4,  Bootstrap 
* 데이터베이스 : mariaDB 10.9.7
* 형광관리 : Git
### 2 요구사항 분석
  #### 1. 회원 가입 페이지
* 유효성 검사
  * 로그인 시 데이터를 토큰(Token)으로 치환하여 원본데이터 대신 토큰을 사용
* 중복확인
  * 데이터베이스에 존재하는 이름 또는 아이디를 입력한 채 회원가입 버튼을 누른 경우 "이미 사용중인 아이디입니다."의 메시지를 보여주기
  * 모든 검사가 통과되었다면 로그인 페이지로 이동시키기
 #### 2. 로그인 페이지
  * 로그인을 하지 않은 경우 아래 페이지만 이용가능
    * 회원가입 페이지
    * 로그인 페이지
    * 메인 페이지
    * 게시글 목록 조회 페이지
  * 로그인 검사
    * 아이디와 비밀번호가 일치하지 않을 시 "아이디 또는 비밀번호가 일치하지 않습니다. "의 메시지를 보여주기
    * 다른 아이디로 작성한 글 수정 불가능
 #### 3. 회원정보 수정
  * 회원정보 수정은 비밀번호만 가능
 #### 4. 게시판
  * 테이블 인덱스 번호에 따라 게시판 유형분류 (자유게시판, 공지사항, 고객상담,자료실)
  * 게시물 50개 씩 페이징처리
  * 해당 게시글 수정 후 수정 했던 해당 게시글 페이지로 이동
  * 다른 유저가 작성한 글은 수정하기 삭제하기 버튼 안보이게 처리
  
#### 1. 회원가입 유효성 및 중복체크 정보수정
<img width="80%" src="https://user-images.githubusercontent.com/72364856/236682499-da14adc0-7ad5-4952-aa3e-40dd5d9acd38.gif"/>

#### 2. 회원로그인 실패 로그인 성공시
<img width="80%" src="https://user-images.githubusercontent.com/72364856/236680981-1248a7f1-8812-4977-afe6-d4cecdf8173c.gif"/>

#### 3. 글쓰기 수정 및 삭제
<img width="80%" src="https://user-images.githubusercontent.com/72364856/236681967-9fc7da3d-216e-4f91-9467-1d3454c0d053.gif"/>



  


# fronted

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