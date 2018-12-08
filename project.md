---
layout: default
title: 프로젝트 
---

<div class="home" id="home">
  <h1 class="pageTitle"> 프로젝트 </h1>
  
  <ul class="posts noList">
    <br><br><div>  
      <strong style='font-size:20px;'>앞으로 진행될 프로젝트의 대한 기록</strong>
    </div><br><br><hr><br>
    {% for post in site.project %}
      <li>
        <span class="date">{{ post.date | date: '%B %d, %Y' }}</span>
        <h3><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>

        <p>{% if post.description %}{{ post.description }}{% else %}{{ post.excerpt | strip_html }}{% endif %}</p>
      </li>
    {% endfor %}
  </ul>
  <!-- Pagination links -->
  <div class="pagination">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | prepend: site.baseurl }}" class="previous button__outline">이전 페이지</a> 
    {% endif %}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | prepend: site.baseurl }}" class="next button__outline">다음 페이지</a>
    {% endif %}
  </div>
</div>