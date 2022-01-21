---
layout: page
use-site-title: true
title: About me
subtitle: ""
---

<!-- 
---
layout: page
title: About me
subtitle: ""
permalink: "aboutme"
--- 
-->

본분에 충실하고 맡은바 최선을 다하는 개발자입니다.

--- 

<br/>

# 경력
* 2021.12 ~ 현재 / 뉴비즈스타트
  + PM 겸 백엔드 개발자

<br/>
# Skill
* Back-end
  + NodeJS
  + Sequelize
* DevOps
  + PostgresQL, MongoDB
  + AWS EC2
* Front-end
  + ReactJS
  + ES6

<br/>
# 역량
* AWS Cloud
  + EC2/ Pm2를 이용한 무중단 서비스 배포
  + crontab을 활용한 매월 DB 자동백업시스템 구현
* 파일 관리
  + exceljs를 활용한 DB정보 다운로드 기능 구현
  + multer / sharp를 활용한 이미지 리사이징 및 용량조절
  + fs를 활용한 일자별 디렉토리 구성

<br/>
# 인적사항
* 김준 
* 1990년 6월 19일
* bearwcw@naver.com

<br/>
# 학력
* 2010.03 ~ 2015.02 고려대학교 세종캠퍼스, 컴퓨터정보학과 졸업(학사). 
  + GPA 2.94

<br/>
# 교육
* 2017.07~2017.12 KH정보교육원 국비지원교육.
  * Based on Java, Oracle and  Spring framework.
  * Make a theater web site - CGV clone.

<br/>
# 자격
* OPic IM2 (2018.04)




<!-- index.md -> index.html로 바꾸고 시작해라
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
