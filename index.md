---
layout: page
use-site-title: true
title: 김준
subtitle: NodeJS  
---

<!-- 
---
layout: page
title: About me
subtitle: ""
permalink: "aboutme"
--- 
-->

4년간 다른 분야에서 활동했습니다.
그리고 이루지 못한 꿈을 다시 찾기 위해 돌아왔습니다.
내 기술로 기업 하나는 운영할만한 능력을 만들자.

--- 

<br/>
# 인적사항

* 김준 
* 1990년 6월 19일
* bearwcw@naver.coåm

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

<br/>
# Skill Sets
* Back-end
  + MongoDB
  + NodeJS
* Front-end
  + HTML, CSS
  + JS


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