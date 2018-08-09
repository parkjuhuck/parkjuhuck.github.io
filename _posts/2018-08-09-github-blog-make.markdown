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


<div style='width: 100%;'>1.레지파지토리를 생성하자</div>

<figure>
	<img style='width:1200px;' src="{{ '/assets/img/post/t1.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 새로운 레파지토리 생성</figcaption>
</figure>


주의 할 점은 이름은 반드시 [본인 Github 아이디].github.io 이어야 한다.

필자의 Github 아이디는 parkjuhuck이기 때문에 parkjuhuck.github.io로 만들었다.

<br>
<hr>
<br>

<div style='width: 100%;'>2. 로컬에 환경을 구축하자</div>

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/t2.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 로컬 경로에 clone을 하자 </figcaption>
</figure>

지금은 아무 파일이 없다. 일단 로컬에 Clone 하자.

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



<blockquote>Aenean lacinia bibendum nulla sed consectetur. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Cras mattis consectetur purus sit amet fermentum. Nulla vitae elit libero, a pharetra augue. Curabitur blandit tempus porttitor. Donec sed odio dui. Cras mattis consectetur purus sit amet fermentum.</blockquote>

Nullam quis risus eget urna mollis ornare vel eu leo. Cras mattis consectetur purus sit amet fermentum. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor.

## Unordered List
* List Item
* Longer List Item
  * Nested List Item
  * Nested Item
* List Item

## Ordered List
1. List Item
2. Longer List Item
    1. Nested OL Item
    2. Another Nested Item
3. List Item

## Definition List
<dl>
  <dt>Coffee</dt>
  <dd>Black hot drink</dd>
  <dt>Milk</dt>
  <dd>White cold drink</dd>
</dl>