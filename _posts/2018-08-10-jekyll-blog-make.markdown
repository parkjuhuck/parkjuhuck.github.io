---
layout: post
title:  "jekyll로 블로그 만들기"
date:   2018-08-10
---
<br>
<br>
<h3 style='width: 100%;'>들어가기 전</h3>
<br>
<p style='font-size:20px;'>지난 시간 우리는 Github로 블로그를 생성하고 테마를 적용시키는 작업을 했다.</p>
<p style='font-size:20px;'>그러면 이 블로그에 글을 어떻게 작성할까? </p>
<p style='font-size:20px;'>내 스타일에 맞게 블로그를 수정 해야하지 않겠는가 라는 의문이 든다.</p>
<p style='font-size:20px;'>Jekyll의 블로그 직접 설치해서 어떻게 글을 작성하고 블로그를 꾸미는지 간략하게 알아보자</p>

<br>
<br>

<h3 style='width: 100%;'>목표</h3>
<div>
  <label style='font-size:25px;'>&nbsp;&nbsp; 1. Jekyll로 블로그 생성 </label>
  <label style='font-size:25px;'>&nbsp;&nbsp; 2. 글 작성 및 테스트 </label>
</div>

<br> 
<hr>
<br>

<h3 style='width: 100%;'>준비물이 필요하다.</h3>
<div style='width: 100%;'>
  <label><strong>&nbsp;&nbsp; - Ruby </strong> : <a href="https://rubyinstaller.org/" target="_blank" > Windows(링크)</a></label>
  <label><strong>&nbsp;&nbsp; - Jekyll</strong></label>
</div>

<br>

Jekyll은 마크다운을 베이스로 정적 HTML 웹사이트를 만들어주는 툴이다.

Jekyll은 Ruby기반으로 만들어졌다.

로컬에서 테스트하기 위해서는 Ruby를 설치해야한다.

<br>
<hr>
<br>


<div style='width: 100%;'>1. Ruby와 Jekyll를 설치해야 한다.</div>
<br>

Ruby를 설치했다면 Start Command Prompt with Ruby를 열자 

<figure>
	<img style='width:1000px;' src="{{ '/assets/img/post/b2/t1.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 그림1 Start Command Prompt with Ruby </figcaption>
</figure>

<br>
새로운 작업환경을 만들자 필자는 D드라이브에 test폴더를 만들었다

이작은 단순 테스트이니 아무 디렉토리를 만들어서 따라해보자.

Jekyll를 설치하자 


<div>
    <label class="highlighter-rouge">
        <pre class="highlight"><code><strong>Mac -> </strong> sudo gem install jekyll bundler</code></pre>
        <pre class="highlight"><code><strong>Window -> </strong> gem install jekyll bundler</code></pre>
    </label>
</div>

해당 디렉토리로 가서 jekyll 와 bundler를 설치한다.

<p style='font-size:20px;'>bundler는 패키지를 관리해주는 녀석이다. (블로그 실행하기 위한 도구라 생각하자)</p>

다음은 블로그를 생성해보자. 

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

이제 이 블로그를 실행시켜보자 

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
