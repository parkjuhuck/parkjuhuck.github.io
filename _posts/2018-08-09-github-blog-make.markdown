---
layout: post
title:  "github + jekyll 개인블로그 생성"
date:   2018-08-09
---
 
<br>
<br>

<h3 style='width: 100%;'>목표</h3>
<div>
  <label style='font-size:25px;'>&nbsp;&nbsp; 1. github로 블로그 생성</label>
  <label style='font-size:25px;'>&nbsp;&nbsp; 2. jekyll 테마 적용</label>
</div>

<br> 
<hr>
<br>

<h3 style='width: 100%;'>준비물이 필요하다.</h3>
<div style='width: 100%;'>
  <label><strong>&nbsp;&nbsp; - Git 설치</strong> : <a href="http://msysgit.github.com/" target="_blank" > Windows(링크)</a>, <a href="http://sourceforge.net/projects/git-osx-installer/" target="_blank" >Mac(링크)</a></label>
  <label><strong>&nbsp;&nbsp; - Github 계정</strong></label>
  <label><strong>&nbsp;&nbsp; - Ruby </strong> : <a href="https://rubyinstaller.org/" target="_blank" > Windows(링크)</a></label>
  <label><strong>&nbsp;&nbsp; - Jekyll</strong></label>
  <label class="highlighter-rouge">
    <pre class="highlight"><code><strong>Mac -> </strong> sudo gem install jekyll bundler</code></pre>
    <pre class="highlight"><code><strong>Window -> </strong> gem install jekyll bundler</code></pre>
  </label>
</div>

<br>

Jekyll은 마크다운을 베이스로 정적 HTML 웹사이트를 만들어주는 툴이다.

Jekyll은 Ruby기반으로 만들어졌다.

로컬에서 테스트하기 위해서는 Ruby를 설치해야한다(필수는 아니다.)


<br>
<hr>
<br>


<div style='width: 100%;'>1. 레지파지토리를 생성하자</div>

<figure>
	<img style='width:1200px;' src="{{ '/assets/img/post/t1.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 새로운 레파지토리 생성</figcaption>
</figure>


주의 할 점은 이름은 반드시 [본인 Github 아이디].github.io 이어야 한다.

<p style='font-size:20px;'>
  필자의 Github 아이디는 parkjuhuck이기 때문에 parkjuhuck.github.io로 만들었다.
</p>


이로써 Github 블로그는 만들어졌다. 아무것도 안되어있을 뿐이다. 

<br>
<hr>
<br>

<div style='width: 100%;'>2. 본인 컴퓨터에 블로그 글들을 환경을 구축하자.</div>

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/t2.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 내 저장소 링크 </figcaption>
</figure>

필자는 윈도우환경이다. 

D:\project 폴더에 blog 폴더를 만들어 관리할것이다.

<p style='font-size:20px;'>
  아무것도 없기때문에 Quick 페이지가 뜰것이다. 이곳에 본인 저장소를 확인하자.
</p>


<pre class="highlight">
  <code>
    $cd D:\project\blog
    $git remote add origin [내 저장소 링크]
    $git add .
    $git commit -m "빈 저장소 불러오기"
    $git push origin master
  </code>
</pre>

<br>
<hr>
<br>

<div style='width: 100%;'>3. 간단한 테스트 ( index.html 생성 ) </div>

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/t3.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> index.html 생성 </figcaption>
</figure>


간단하게 html 파일을 만들어서 적용시켜보자 

본인 환경에 index.html을 만들고 git push를 한다.

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/t4.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 블로그 확인 </figcaption>
</figure>


<p style='font-size:20px;'>
  [본인 Github 아이디].github.io 입력하고 확인해보면 출력화면이 확인할 수 있다.
</p>


<br>
<hr>
<br>


<!-- 
{% highlight html %}
<figure>
	<img src="{{ '/assets/img/touring.jpg' | prepend: site.baseurl }}" alt=""> 
	<figcaption>Fig1. - This is an example figcaption</figcaption>
</figure>
{% endhighlight %}

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %} -->


<!-- Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll's GitHub repo][jekyll-gh].

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com -->



<!-- <blockquote>Aenean lacinia bibendum nulla sed consectetur. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Cras mattis consectetur purus sit amet fermentum. Nulla vitae elit libero, a pharetra augue. Curabitur blandit tempus porttitor. Donec sed odio dui. Cras mattis consectetur purus sit amet fermentum.</blockquote> -->



<!-- ## Unordered List
* List Item
* Longer List Item
  * Nested List Item
  * Nested Item
* List Item

## Definition List
<dl>
  <dt>Coffee</dt>
  <dd>Black hot drink</dd>
  <dt>Milk</dt>
  <dd>White cold drink</dd>
</dl> -->