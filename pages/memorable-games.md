---
title: "Memorable-games"
subtitle: "기억에 남는 게임을 공유하는 페이지"
layout: "page"
permalink: "memorable-games"
tags: [memorable-games, portfolio]
toc: true
toc_sticky: true

---



## Url
* 홈페이지

  <a href="https://memorable-games.herokuapp.com/">https://memorable-games.herokuapp.com/ </a>

* Github Repository 

  <a href="https://github.com/Juzdalua/memorable-games">https://github.com/Juzdalua/memorable-games</a>

<br> <br>

<br> <br> 

## Language & Tool

Back-end : Nodejs, MongoDB

Front-end : PUG

Server : AWS, Mongo-atlas

<br> <br> 

## User authorize

nodejs의 express-session을 사용했습니다. session을 활용하여 브라우저의 정보를 mongo-store에 저장하고 불러왔습니다. 사용자 인증에 있어 쿠키와 세션을 이용하면 개발상 편리하지만, 개인적으로 노출의 위험이 크다고 생각했습니다.<br>

DB의 session collection에 유저의 정보가 저장되기 때문에, DB가 해킹당한다면 상상하기도 싫네요. 이를 개선하기 위한 방법은 서버를 이용한 JWT가 있다고 찾았습니다. 아직 구현하지는 못했지만, 공부할 계획입니다.<br>

DB를 해킹당했을 경우를 대비한 방법은 hash입니다. bcrypt를 사용하여 비밀번호는 사용자만 알 수 있도록 구현했습니다. 비밀번호 수정, 로그인은 기존 암호와 compare 하는 방식으로 구현했습니다.

<br>

<br>



## Design

개인적으로 공부하며, Front-end part는 Webpack으로 공부했습니다. 허나 이는 실무에서 사용하지 않는다하여 이번 포트폴리오에는 구성하지 않았습니다. <br>

유저가 접근할 수 있는 static 폴더를 구성하고, css파일을 분리하여 분업에 유리하도록 공부했지만 실현시키지 않았습니다. 그리하여 하나의 css파일에 모든 것을 담았습니다.<br>

미적감각이 떨어져 가장 덜 중요하게 생각했던 파트입니다.<br>

아직 구현하지 못한 점, 개선해야 할 사항은 다음과 같습니다.<br>

***해상도에 따른반응형 디자인**<br>

***배경화면을 설정 시, 페이지의 크기마다 적용이 되지 않음.**<br>

<br>

<br>



## 게시판

공지사항, 게임, 커뮤니티 게시판은 같은 틀에서 조금만 방향성을 바꿨습니다.<br>

***가장 심플한 공지사항**<br>

***Yotube 형식의 썸네일을 추가한 게임 게시판**<br>

***기존의 게시판 형식을 이어 받은 커뮤니티 게시판**<br>

<br>

게임, 커뮤니티 게시판은 각각 이미지와 동영상, 이미지를 첨부할 수 있습니다. local에서는 multer를 사용했는데, AWS와 연동시 s3-multer를 사용해야 했습니다. <br>

local-multer에서 게임게시판의 동영상을 업로드한다면, ffmpeg를 사용하여 썸네일을 자동제작 후 업로드 되는 형식으로 구현했습니다.<br>

aws-s3 multer에서 게임게시판의 동영상을 업로드한다면, 자동제작된 썸네일은 local에 저장되기에 이는 아직 구현하지 못했습니다.

<br>

<br>



## 느낀점 

21년 6월 말에 퇴사하고, 다시 코딩 공부를 시작했습니다. 과거 Spring framework 기반 JAVA와 Oracle 기반 Mybatis를 공부했었지만, 이번에는 JS와 mongoose를 공부했습니다. <br>

약 2개월간 개인적으로 공부를 마친 후, 9월부터 프로젝트를 시작했습니다. 여행도 다녀오고 친구들도 만나며 쉬엄쉬엄 진행했습니다. 약 한 달 반만에 heroku를 이용하여 배포하였고, 오류를 찾으며 개선중입니다.<br>

돌아보며, 정말 빡쌔게 한다면 1~2주안에 마무리 할 수 있었을 것 같습니다. 잠시 그동안의 burnout을 해소하고자 시간이 꽤 걸렸습니다.<br>

팀프로젝트만 경험했던 저에게, full-stack이라 하기에도 애매하지만 처음부터 끝까지 혼자 완주한 프로젝트였습니다. back-end 파트에서 근무한다면 front-end와 이런점이 겹치겠구나를 느꼈습니다. 어떻게 코드를 구현하고 파트를 구분해야 협업에 도움이 될 지 많은 생각을 하게 해준 결과물이었습니다.





