---
layout: default
title: 자바스크립트
---

<div class="home" id="home">
  <h1 class="pageTitle"> 자바스크립트 </h1>
  
  <ul class="posts noList">
    <br><br><div>  
      <strong style='font-size:20px;'>필자는 요즘 이직준비중이다.

몇번의 면접을 보고나서 느꼈다 정말 정말 많이 부족하구나..

면접준비 + 개인공부를 하면서 봤던거 보고 보고 또 보고..뒤돌아서면 까먹고

안되겠다 싶어 블로그에 남기고자 2년만에.. 블로그를 다시 시작했다. 나는 할수있다. 아자!!!!
</strong>

</div><br><br><hr><br>
{% for post in site.javascript %}
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
