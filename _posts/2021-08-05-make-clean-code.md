---
title: Clean Code 만들기
subtitle: 짧은 코드로 변경하기
layout: post
category: study
tags: [Clean Code]
image: https://user-images.githubusercontent.com/34051263/128224128-f5b809d8-0d65-4aeb-aae9-b3001246d80b.png
---


<br><br>

## 1. 삼항연산자 (Ternary Operator)

1학년 C언어 수업을 들을 때부터 조건문은 이렇게 작성해왔다.

```javascript
if(req.session.loggedIn){
	return next();
} else{
	return res.redirect("/");
}
```

초보자에게 가독성(?)은 좋을지라도 뭔가 간단한 내용이지만 코드가 길다. <br>

그래서 Clean Code로 바꿔보자.

```javascript
return req.session.loggedIn === true ? next() : res.redirect("/");
```

훨씬 깔끔하다.   <br>

##### 참고) https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Conditional_Operator
<br>  


## 2. ES6 Parameter 받아오기

Form 내부 Input 타입으로 변수를 받아 올 때,   <br>

GET method는 req.params과 req.query, POST method는 req.body로 받아온다.

```javascript
const id = req.body.id;
const password = req.body.password;
```

만약 유저가 로그인을 하고, 수많은 정보들을 불러와야 한다면 간단한 코드는 길어질 수 밖에 없다.   <br>

물론 이를 완화한게 객체지향, Object로 받아오면 되겠지만 조금 더 편리한 방법.  <br>

```javascript
const { id, password } = req.body;
```

끝이다.  
<br>  

## 3. 널 병합 연산자 (Nullish Coalescing Operator) ??

왼쪽 피연산자가 null, undefined라면 오른쪽 피연산자를 반환한다.

```javascript
function printMessage(text){
	const message = text ?? "hello";
	console.log(message);
}

printMessage('hi'); // hi
printMessage(null); // hello
printMessage(undefined); // hello
```

##### 참고) https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator   

<br>



## 4. 논리연산자 (Logical Operator) ||

널 병합 연산자와 비슷한 개념.<br>

왼쪽 피연산자가 falsy인 경우 오른쪽 피현산자를 반환한다.

### *falsy란?

* undefined

* null

* false

* 0

* -0

* NaN(Not a Number)

* "", '', `` (공백)

  <br>

## 5. 전개구문(Spread Syntax)

Array나 Object를 가져오거나 추가할 때, 업데이트 할 때 사용한다.

```javascript
let num = [1, 2, 3];
num = [..., 4];

const item = { type:'pants', size:'XL'};
const detail = { price:20, made:'Korea' };
const list = {...item, ...detail, price:40};
```

##### 참고)https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Spread_syntax  

<br>



## 6.Template Literals

변수와 String을 함께 사용할 때 유용하다.

```javascript
const year = new Date().getFullYear();
console.log(`year:${year}`); // year:2021
```

pug에서는 #{}도 사용한다.  <br>

단, 백틱(`) = 키보드 자판 1 왼쪽 ~(물결표)를 사용해야한다.

##### 참고) https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Template_literals

<br>



## 7. Loops 

Array를 조건에 맞게 재구성해주는 함수들

```javascript
const arr = [1, 2, 3, 4, 5, 6];
const even = arr.filter( (num) => num%2 === 0 ); /// [2, 4, 6]
const fouth = even.map( (x) => x*4 ); //[8, 32, 48];
```

<br>



## 8. Promise -> async / await

```javascript
fetchUser().then( (user) => {
	fetchProfile(user).then( (profile) => {
		updateUI(user, profile);
	});
});
```

URL을 호출하는 fetch() 함수. 사실 나도 잘 감이 오질 않지만, DB와 연동할 때 코드가 엄청 길어진다.

```javascript
async function displayUser(){
	const user = await fetchUser();
	const profile = await fetchProfile(user);
	updateUI(user, profile);
}
```

async/await을 함께 사용한다면 수월하다. Object가 변수로 들어간다면 객체를 String으로 변환해주는 .json()을 사용해주자.

<br>



## 9. Array - Remove Duplication

```javascript
const arr = [1, 2, 3, 1, 4, 2, 5];
console.log([...new Set(arr)]); // [1, 2, 3, 4, 5]
```

Set()은 중복을 허용하지 않는다.  

<br><br>



지금까지 모든 내용은 드림코딩 by 엘리님의 영상을 공부하고 정리한 내용이다.

##### 참고) https://youtu.be/BUAhpB3FmS4



