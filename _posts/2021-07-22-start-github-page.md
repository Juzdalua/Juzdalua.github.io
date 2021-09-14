---
title: "Github Page 만들기"
subtitle: "테마 적용하기"
layout: "post"
category: "diary"
tags: [Github Blog]
image: https://user-images.githubusercontent.com/34051263/133181312-31c4a43c-5136-462f-b696-9f1023cacca0.png
---

남들 다 만드는 minimal-mistakes 테마를 적용했다.

![blog](https://user-images.githubusercontent.com/34051263/126591169-1e8fdf49-84ad-4e70-bb0e-0a973ee0f879.png)

Fork만 누르면 바로 적용되다니... 너무 신세계다.

근데 이 테마는 너무 흔하다.

fixed bar를 좋아하는 나에게 beautiful-jekyll이 딱이었다.

근데 이 테마는 한글로 된 블로그 가이드라인이 별로 없다는 것. ~~(내가 못찾는건가...)~~

<br/>

---

<br/>

# Difference of beautiful-jekyll

_config.yml은 모두가 알겠지만

내가 이틀동안 찾아보며 찾은 핵심은

**<mark style='background-color: #ffdce0'>category folder와 pages folder.</mark>**

<br/>

*minimal-mistakes*에서 **\_pages** 폴더를 사용했다면

*beautiful-jekyll*에서는 **pages** 폴더를 사용해야한다.

이유는 나도 모르겠다.

**<mark style='background-color: #ffdce0'>하위링크가 없는 단일 page라면 permalink를 지정해주자.</mark>**

![image](https://user-images.githubusercontent.com/34051263/126595900-606d3f44-d646-4336-b779-e6d464f5dcb0.png)

---

  <br/>

# Add Category

Github Blog는 기본적으로 Categoty 또는 Sitemap을 제공하지 않는다고 한다.

**<mark style='background-color: #ffdce0'>그래서 따로 만들어줘야한다.</mark>**

![image](https://user-images.githubusercontent.com/34051263/126595558-1f146f39-dc31-4688-8623-35746ba2bedf.png)

---

   <br/>

# Write Category in post

**<mark style='background-color: #ffdce0'>post를 작성할 때 category 입력해주기!</mark>**

![image](https://user-images.githubusercontent.com/34051263/126595827-16d59dc2-4d51-4f2e-862d-0cae1a3798c1.png)

---

  <br/>

# Write Category.html

**<mark style='background-color: #ffdce0'>_layout/category.html을 만들어준다</mark>**

```html
---
layout: default
---

<ul class="posts-list">
  {% assign category = page.category | default: page.title %}
  <h4>Posts in {{ category }} ({{ site.categories[category].size }})</h4>
  {% for post in site.categories[category] %}
  <li>
    <a class="post-title" href="{{ site.baseurl }}{{ post.url }}"
      >{{ post.title }}</a
    >
    <small
      ><time>
        {{ post.date | date:"%F" }} {{ post.date | date: "%a" }}.
      </time></small
    >
  </li>
  {% endfor %}
</ul>
```

![image](https://user-images.githubusercontent.com/34051263/126598602-c6eb71fa-7537-4861-94cc-6c94746c2b7d.png)

짜잔 완성~
