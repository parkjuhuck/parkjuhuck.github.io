---
layout: post
title:  "jekyll로 블로그 만들기"
date:   2018-08-10
---

<title>{% if page.title %}{{ page.title | escape }}{% else %}{{ site.title | escape }}{% endif %}</title>
<meta name="description" content="{% if page.excerpt %}{{ page.excerpt | strip_html | strip_newlines | truncate: 160 }}{% else %}{{ site.description }}{% endif %}">
<meta property="og:jekyll로 블로그 만들기" content="{% if page.title %}{{ page.title | escape }}{% else %}{{ site.title | escape }}{% endif %}">
<meta property="og:jekyll로 블로그 만들기" content="{% if page.excerpt %}{{ page.excerpt | strip_html | strip_newlines | truncate: 160 }}{% else %}{{ site.description }}{% endif %">
<meta property="og:type" content="website">
<meta property="og:url" content="{{ page.url | replace:'index.html','' | prepend: site.baseurl | prepend: site.url }}"/>
<meta property="og:image" content="{{ site.url }}/images/songyunseop.jpeg"/>
<meta property="og:image:width" content="420" />
<meta property="og:image:height" content="420" />
<meta property="og:image:type" content="image/png">

<br>
<br>
<h3 style='width: 100%;'>들어가기 전</h3>
<br>
<p style='font-size:20px;'>지난 시간 우리는 Github로 블로그를 생성하고 테마를 적용시키는 작업을 했다.</p>
<p style='font-size:20px;'>그러면 이 블로그에 글을 어떻게 작성하는 것일까? </p>
<p style='font-size:20px;'>Jekyll의 블로그 직접 설치해서 어떻게 포스팅을 하는지 간략하게 알아보자</p>

<br>
<hr>
<br>

<h3 style='width: 100%;'>목표</h3>
<div>
  <label style='font-size:25px;'>&nbsp;&nbsp; 1. Jekyll로 블로그 생성 </label>
  <label style='font-size:25px;'>&nbsp;&nbsp; 2. 블로그 글 작성  </label>
</div>

<br> 
<hr>
<br>

<h3 style='width: 100%;'>준비물이 필요하다.</h3>
<div style='width: 100%;'>
  <label><strong>&nbsp;&nbsp; - Ruby </strong> : <a href="https://rubyinstaller.org/" target="_blank" > Windows(링크)</a></label>
  <label><strong>&nbsp;&nbsp; - Jekyll</strong></label>
</div>

Jekyll은 마크다운을 베이스로 정적 HTML 웹사이트를 만들어주는 툴이다.

Jekyll은 Ruby기반으로 만들어졌다.

로컬에서 테스트하기 위해서는 Ruby를 설치해야한다.

<br>
<hr>
<br>


<div style='width: 100%;'>1. Jekyll를 설치하자.</div>
<br>

Ruby를 설치했다면 Start Command Prompt with Ruby를 열자 

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t1.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 그림1 Start Command Prompt with Ruby </figcaption>
</figure>

새로운 작업환경을 만들자 필자는 D드라이브에 test폴더를 만들었다

이작은 단순 테스트이니 아무 디렉토리를 만들어서 따라해보자.

<div>
    <label class="highlighter-rouge">
        <pre class="highlight"><code><strong>Mac -> </strong> sudo gem install jekyll bundler</code></pre>
        <pre class="highlight"><code><strong>Window -> </strong> gem install jekyll bundler</code></pre>
    </label>
</div>

해당 디렉토리로 가서 jekyll 와 bundler를 설치한다.

<p style='font-size:20px;'>bundler는 패키지를 관리해주는 녀석이다. (블로그 실행하기 위한 도구라 생각하자)</p>

<br>
<hr>
<br>

<div style='width: 100%;'>2. jekyll로 블로그 생성하기.</div>
<br>
<div>
    <label class="highlighter-rouge">
        <pre class="highlight"><code>$ jekyll new '블로그이름'</code></pre>
    </label>
</div>

필자는 testBlog의 이름을 가진 블로그를 만들었다. 

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t2.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림2 블로그 생성 </figcaption>
</figure>

블로그 생성이 완료되었다.

testBlog 폴더안을 보면

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t3.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림3 생성된 블로그 폴더 내용 </figcaption>
</figure>

<br>
<hr>
<br>

<div style='width: 100%;'>3. 블로그 실행. </div>
<br>
<div>
    <label class="highlighter-rouge">
        <pre class="highlight"><code>$ bundle exec jekyll serve</code></pre>
    </label>
</div>

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t4.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림4 jekyll 블로그 실행  </figcaption>
</figure>

Prompt 화면에 보면  Server address: http://127.0.0.1:4000/ 부분이 있다.

본인 컴퓨터가 서버로 돌아가는 것이다.

주소를 복사에 브라우저에 붙여넣기를 한다.

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t5.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림5 브라우저 실행결과  </figcaption>
</figure>

블로그가 생성되었다. 

생성된 블로그를 내 블로그에 어떻게 적용 시킬까

여러분들은 알거라 믿는다.

그렇다. 
<p style='font-size:20px;'>
  1. 애초에 github 로컬환경에 블로그를 생성한다.
</p>
<p style='font-size:20px;'>
 2. 이미 github 로컬환경 파일이 있다면 지우고 그림3 생성된 파일을 넣는다. 
</p>


우리는 이미 Github에 jekyll 테마를 적용한 블로그를 보유하고 있다.

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t6.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림6 기존 블로그 jekyll 실행하기  </figcaption>
</figure>

bundle을 설치하고 실행을 시켜주자.

<div>
    <label class="highlighter-rouge">
        <pre class="highlight"><code>$ bundle exec jekyll serve</code></pre>
    </label>
</div>

그리고 브라우저로 다시 http://127.0.0.1:4000/ 를 입력해가 보면 

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t7.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림7 Github 블로그 jekyll 실행 화면  </figcaption>
</figure>

로컬 환경에서 github 블로그와 같은 화면이 출력이 됐음을 알수있다.

<p style='font-size:20px;'>
이 환경에서 블로그를 작성,수정해서 화면을 출력해보고 완료가 되면 git push하여
</p>
실제 블로그를 업데이트 하는것이다.

<br>
<hr>
<br>

<div style='width: 100%;'>4. 포스팅 하기.</div>
<br>
<figure>
	<img style='width:500px;' src="{{ '/assets/img/post/b2/t8.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림8 jekyll 블로그 구성요소 </figcaption>
</figure>

새 포스트를 생성하려면, _posts 디렉토리에 파일을 생성하면 된다. 

이 때 중요한 것은 생성하는 파일의 이름이다. Jekyll 이 이 파일을 블로그 

포스트로 인식하게 하려면 파일명을 다음 형식에 맞춰야 한다.

<strong>YEAR-MONTH-DAY-title.markdown</strong>
    
여기서 YEAR 는 네 자리의 숫자, MONTH 와 DAY 는 두 자리 숫자이고, 

확장자 부분의 markdown 은 파일에 사용된 마크다운 포맷이다

예로 들면 

2018-08-11-new-post.markdown

현재 6개의 게시글이있다. 다 지우고 새로운 포스트를 작성해보겠다.

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t9.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림9 포스트 작성 </figcaption>
</figure>

_post엔 하나의 글만 있다.

<figure>
	<img style='width:900px; height:500px;' src="{{ '/assets/img/post/b2/t10.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption>그림10 블로그 확인 </figcaption>
</figure>

방금 작성된 글이 업데이트 되었음을 확인할수 있다.


<hr>
<br>
<strong style='font-size:20px;'>앞으로는 독자들의 몫이다 ㅎㅎ </strong>

<strong style='font-size:20px;'>본인 스타일에 맞게 블로그를 꾸미거나 메뉴를 추가한다거나 할 일이 굉장히 많다. </strong>

<strong style='font-size:20px;'>본인이 직접 jekyll 사용법을 익혀 테마를 꾸밀수도 있고 </strong>

<strong style='font-size:20px;'>필자처럼 다른 사람이 만들어 놓은 테마를 가지고와 커스터마이징 할 수도있다. </strong>

<strong style='font-size:20px;'>다른사람의 jekyll 테마를 사용할 시 README를 꼭 참고하길 바란다.</strong>

<strong style='font-size:20px;'>jekyll 의 더 자세히 사용하려면   <a href=" https://jekyllrb-ko.github.io/docs/home/" target="_blank" > jekyll </a> 공식사이트를 참고는 필수다!. </strong> 
<br>


<!-- 주의 할 점은 이름은 반드시 [본인 Github 아이디].github.io 이어야 한다. -->

<!-- <p style='font-size:20px;'>
  필자의 Github 아이디는 parkjuhuck이기 때문에 parkjuhuck.github.io로 만들었다.
</p> -->


<!-- 이로써 Github 블로그는 만들어졌다. 아무것도 안되어있을 뿐이다.  -->

<!-- <br>
<hr>
<br> -->

<!-- <pre class="highlight">
  <code>
    $cd D:\project\blog
    $git remote add origin [내 저장소 링크]
    $git add .
    $git commit -m "빈 저장소 불러오기"
    $git push origin master
  </code>
</pre> -->

<!-- <a href=" http://jekyllthemes.org/" target="_blank" > 테마 페이지</a> 여기서 원하는 테마를 선택한다. -->
