---
layout: page
use-site-title: true
title: ""
subtitle: 백엔드 개발자 김준입니다.
---

백엔드 개발자 김준입니다.<br/>
NodeJS와 RDBMS, Linux에 흥미를 갖고 있습니다.<br/>
코드의 가시성, 재사용성을 위해 Layer Architecture를 사용하려 노력합니다.<br/>
강의보다 공식문서, 커뮤니티를 통해 새로 만들어보며 적용하는 스타일입니다.<br/>
본분에 충실하고 맡은바 최선을 다하는 개발자가 되고자 노력합니다.

---

<br/>
<!--## Work experience
- 2021.12 ~ 현재 / 뉴비즈스타트
	- PM 겸 백엔드 개발자   
		- ### [케어봄](https://www.junctionmed.com/) (시니어 돌봄 서비스 App)
			NodeJS, PostgreSQL, Sequelize
			- AWS Cloud
				- EC2/ Pm2를 이용한 무중단 서비스 배포.
			- Data 처리
				- Admin 페이지 구현. (회원관리, 건강정보관리 등)
			- 파일 관리
				- exceljs를 활용한 DB정보 다운로드 기능 구현.
				- multer / sharp를 활용한 이미지 리사이징, 용량 및 화질 조절 구현.
				- fs를 활용한 일자별 디렉토리 구성.


		- ### [Spoweek](http://www.spoweek.com) (스포츠 이벤트 서비스 Web)
			Typescript, PostgreSQL, TypeORM
			- AWS Cloud
				- crontab을 활용한 매월 DB 자동백업시스템 구현.
			- Data 처리
				- Admin 페이지 구현. (회원관리, 이벤트관리 등)
<br/> -->

## Skills
- Back-end
  - NodeJS
	- Java가 폐쇄적이라 생각하여 선택한 언어입니다. 함수형 프로그래밍을 선호합니다.
  - Typescript
	- Class와 Interface에 익숙하지 않습니다. 그래서 더 공부하고자 합니다.
  - Sequelize
	- 가장 능숙하게 활용할 수 있는 DB Tool입니다.
  - TypeORM
	- QueryBuilder, Repository를 주로 이용합니다.
- DevOps
  - PostgreSQL, MongoDB
	- RDB를 선호합니다. PostgreSQL을 자주 사용합니다.
  - Cloud
	- Linux를 좋아합니다. 해커가 된 느낌(?)이라 마우스 없는 코딩을 추구합니다.
	- AWS EC2, GCP를 활용하여 서버를 구축할 수 있습니다. pm2를 활용하여 무중단 서비스를 배포할 수 있습니다.
	
- Front-end
  - ReactJS
	- VanilaJS가 더욱 익숙합니다. 
		완벽히 이해하지는 못했지만, 어떻게 구현해야 Backend와 연결할 수 있는지 이해하고 있습니다. 
		state와 effect, redux까지 활용할 수 있습니다.
  - React-Native
	- 백엔드와 연동하기 위한 코드를 파악할 수 있습니다. 공식문서 Component와 커뮤니티 패키지를 활용할 수 있습니다.
  - ES6
	- 이전 문법들도 알고 있지만, 최신 문법을 선호합니다.

<br/>

## About me
- 김준 
- 1990년 6월 19일
- bearwcw@naver.com

<br/>

## Education
- 2017.07~2017.12 KH정보교육원 국비지원교육.
  - Based on Java, Oracle and  Spring framework.
  - Make a theater web site - CGV clone.
- 2010.03 ~ 2015.02 고려대학교 세종캠퍼스, 컴퓨터정보학과 졸업(학사). 
  - GPA 2.94

<br/>

## Certification
- OPic IM2 (2018.04)
- ~~정보처리기사 필기만 합격..(2017.08)~~





<!-- index.md -> index.html로 바꾸고 시작해라
---
layout: page
title: About me
subtitle: ""
permalink: "aboutme"
--- 

---
layout: page
title: Jun
subtitle: Way to be gorgeous developer
---

<div class="posts-list"> 
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h2 class="post-title">{{ post.title }}</h2>

	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>

    <div class="post-entry-container">
      {% if post.image %}
      <div class="post-image">
        <a href="{{ post.url | prepend: site.baseurl }}">
          <img src="{{ post.image }}">
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }}
        {% assign excerpt_word_count = post.excerpt | number_of_words %}
        {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
        {% endif %}
      </div>
    </div>

    {% if post.tags.size > 0 %}
    <div class="blog-tags">
      Tags:
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ site.baseurl }}/tag/{{ tag }}">{{ tag }}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    </div>
    {% endif %}

   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}
-->
