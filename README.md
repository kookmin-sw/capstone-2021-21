# 오프라인 중고서점 검색엔진 - 책나와
<img width="236" alt="KakaoTalk_Photo_2021-04-04-22-16-25" src="https://user-images.githubusercontent.com/4518740/113510099-ee8ed000-9593-11eb-8e7f-c212e214500c.png">


* 팀페이지: [https://kookmin-sw.github.io/capstone-2021-21](https://kookmin-sw.github.io/capstone-2021-21)
* 팀저장소: [https://github.com/cappstone/offline_oldbook_searchengine](https://github.com/cappstone/offline_oldbook_searchengine)

---

# 프로젝트 소개

<img width="1324" alt="Untitled" src="https://user-images.githubusercontent.com/4518740/113510049-ab346180-9593-11eb-8b59-feeecea6ee1b.png">
<img width="1326" alt="Untitled2" src="https://user-images.githubusercontent.com/4518740/113510064-bedfc800-9593-11eb-896c-66f223c8fbea.png">

## 프로젝트의 간단한 소개

- 새책을 사기엔 비싸다.
- 택배로 배송 받기엔 오래걸린다.
- 1:1 개인간 거래는 무섭다.
- 책 상태와 내용을 미리 보고 싶다.

“책나와” 서비스를 활용하여 yes24와 알라딘 오프라인 중고매장 바로 검색하자!

## 배경 및 개요

대학생인 우리들은 항상 개강 후에 책을 강의 서적을 구매해야한다. 하지만 강의 서적은 비싸기 때문에 중고서점을 통해서 구매하게 된다. 대표적으로 ‘YES24’ 와 ‘알라딘’ 중고매장에서 주로 구매해야한다. 하지만 YES24는 한 책에 대한 통합검색을 지원하지 않아서 불편하고 알라딘은 통합검색을 지원하지만 불편한 UX로 인해 한눈에 정보를 얻는 어려움이 존재했다.
이번 기회로 내가 구매하고 싶은 중고책을 쉽게 구매할 수 있도록 두 서비스의 검색결과를 통합하고 내 위치 기준으로 가까운 서점을 알려줄 수 있도록 만들었다.

# 기능

- 알라딘 검색결과 제공
- YES24 검색결과 제공
- 알라딘 & YES24 통합검색결과 제공
- 현재 위치와 매장 위치 비교 하여 가장 가까운 위치순 검색결과 제공

# 프로젝트에 사용된 스텍

## Backend & Crawler

**Python 3.7+**

1. Flask
    - Flask 1.1.2
    - Flask-Cors 3.0.10
    - Flask-RESTful 0.3.0
2. Requests 2.25.1
3. Beautiful Soup 4.9.3

## FrontEnd

**Vue.js 2.6.11**

1. axios 0.21.1
2. vue-cli 4.5.11
3. node-sass 5.0.0
4. vue-fontawesome 5.10.0

# 구조
(추후 업데이트 예정임)
<img width="1680" alt="Untitled3" src="https://user-images.githubusercontent.com/4518740/113526916-bd93b700-95f6-11eb-912b-8e009dc54825.png">


# 사용방법

## 1. 세팅방법
### 원스크립트 세팅
1. 터미널에 ./env_setting.sh
### 수동세팅
1. 리눅스 또는 macOS에 npm, python 설치하기
2. frontend 디렉토리로 가서 npm install
3. pip install -r requirements.txt
4. npm run serve 하여 vue-cli실행
5. python api_server.py
### 주의사항
* 위의 세팅방법은 linux계열 및 macOS에서만 가능함
* api_server.py 들어가서 포트세팅 할 것 (기본: 7000)

## 2. 실행방법
### 원스크립트 실행
1. 터미널에 ./server_start.sh
### 수동 실행
1. python api_server.py
2. npm run serve
### 주의사항
* 이 실행방법은 vue-cli의 포트를 오픈하여 실행하는 방식임

## 3. webpack 배포방법
1. npm run build
2. /dist 에 있는 webpack을 nginX로 연동할것

## 4. 주소조합
http://{서버주소}:{포트}/search?word={검색어}&mode={검색모드}
### 예시
http://sc0nep.iptime.org:7000/search?word=스즈미야하루히의우울&mode=0
### 검색모드
0: 알라딘
1: yes24

## 5. Crawling 테스트 하기
1. python backend/test.py
2. 터미널에 나오는 내용에 따라 진행하기

# 팀원소개

```
이동형
Backend, Crawler, Project Management

INFO:
	ID: 20163135
	E-Mail: sc0_nep@yahoo.co.jp
	Github: github.com/dlehdgud2380
```

```
권순영
Team Leader, Frontend

INFO:
	ID: 20163419
	E-Mail: ssassaium@gmail.com
	Github: github.com/YJSNPIDISK
```

```
이동범
Frontend(Sub), QA, Support

INFO:
	ID: 20163134
	E-Mail: emfprhs1579@kookmin.ac.kr
	Github: github.com/DB-platform
```
