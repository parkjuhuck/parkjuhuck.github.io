---
layout: default
title: 자바스크립트
---

<div class="home" id="home">
  <h1 class="pageTitle"> 자바스크립트 </h1>
  
  <ul class="posts noList">
    <br><br><div>  
      <strong style='font-size:20px;'>이직을 준비하면서 공부를 하다보니 정리가 되지않았다.
      했던거 또 보고 뒤돌아서면 까먹고 그래서 큰맘먹고 블로그에 남기기로 마음먹았다</strong>
    </div><br><br><hr><br>
    {% for post in site.functional_javascript %}
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
