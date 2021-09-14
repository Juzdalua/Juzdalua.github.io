---
title: Login Session
subtitle: ES6, nodeJS, MongoDB
layout: post
category: study
tags: [Login Session]
---

ㅇ 

# nodeJS에서 Session을 활용한 Login

<br> 

## 1. install session

```
npm i express-session
```

출처 : https://www.npmjs.com/package/express-session

<br> 

## 2. server.js

```javascript
import session from "express-session";

app.use(session({
    secret: 'booyah',
    resave: false,
    saveUninitialized: false,
    cookie: { secure: false },
    store: MongoStore.create({ mongoUrl: `mongodb: ${your_url}` })
  }));
```

**secret**: 키값이다. 어떤걸로 해도 상관없으나 추후 보안을 위해 해쉬화 추천. <br>**resave**: 수정되지 않은 세션도 다시 저장한다. 세션의 만료날짜를 정한다면 true를 권장.<br>**saveUninitialized**: 접속하는 모든 사용자의 세션을 저장한다. 한 페이지에 새로고침을 5번한다면 5번 세션이 변한다. 로그인세션을 진행한다면 false 권장. <br>**cookie**: secure:true라면 브라우저에서도, 미들웨어에서도 session에 접근할 수 없다. false 권장. <br>**store**: 아래 설명하겠지만,  세션을 DB에 저장하기 위한 코딩. <br>

<br>

store 항목을 제외하고, 여기까지만 진행한다면 브라우저상에서만 활동하는 session을 구축했다.

<br> <br> 

## 3. DB에 저장하기.(with mongoDB)

```
npm i connect-mongo
```

출처: https://www.npmjs.com/package/connect-mongo <br>



```javascript
import MongoStore from "connect-mongo";
```

server.js에 import 해준 후, 2번 항목의 store까지 작성한다.<br>

```javascript
req.session.loggedIn = true;
req.session.user = loginUser;
```

userController의 postLogin에서 유저를 받아왔다면, 세션에 유저 정보와 로그인 여부를 저장한다.<br><br>

세션에 유저 정보가 저장되었다면, 어떤 페이지를 가더라도 유저를 기억해야한다. 우리가 평소 사용하는 웹사이트들처럼.

```javascript
export const localsMiddlewares = (req, res, next) => {
    //session
    res.locals.loggedIn = Boolean(req.session.loggedIn);
    res.locals.loggedInUser = req.session.user;
    next();
};
```

middlewares.js에 작성한 내용이다. session의 정보를 locals에 저장한다. res.locas를 사용한 이유는, 나는 view template을 PUG를 사용하기 때문.

```html
 nav.nav-topbar 
            ul.nav-topbar__main 
                li
                    a(href="/") Home
                if !loggedIn     
                    li
                        a(href="/login") Login 
                    li
                        a(href="/join") Join
                else
                    li 
                        a(href="#") #{loggedInUser.userid} 
                    li
                        a(href="/logout") Logout
```

아쉽게도 typora에서는 언어에 pug가 보이지 않는다. 눈이 침침해지지만, 이런 느낌을 주기 위해서.<br>

```javascript
app.use(localsMiddlewares);
app.use('/', rootRouter);
```

작성한 미들웨어를 사용하기 위해 server.js에 한 줄 작성해준다.<br><br>



## 완성

유저가 로그인 할 때 마다 DB에 세션과 유저의 정보가 저장된다. 페이지를 돌아다녀도 불필요한 세션은 계속해서 저장되지 않는다.<br>

session을 처음 설정할 때 **saveUninitialized를 true**로 작성해서, **cookie: {secure}를 true**로 작성해서 장시간 고생했다.<br>

브라우저: 유저 정보 및 세션 -> DB로 전송 -> 서버가 재부팅 되도 사라지지 않는 세션.