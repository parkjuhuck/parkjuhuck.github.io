---
layout: post
title:  "github 블러그 만들기 + jekyll 테마 적용"
date:   2018-08-09
---
 
<br>
<br>
<h3 style='width: 100%;'>들어가기 전</h3>
<br>
필자의 첫 블로그 글이다.

포스트를 작성하기 전 직접 블로그를 만들기 전까지

필자는 많은 삽질을 하고나서 이 글을 작성하였다.

포스트를 작성하면서도 이 부분을 넣어야 되나 빼야되나 

생각이 많았다.

금방 쓸줄알았는데 생각보다 훨훨훨 씬 많은 시간이 걸렸다.

필자는 git을 잘 모른다. 그냥 commit, push, branch 사용법 정도

그리고 소스트리를 쓴다.

이 글을 보는 사람들 중 git을 모르는 사람이 있으면 어쩌지 

소스트리를 사용안하는 사람들은..? 

터미널이 뭔지 모르는 사람이면..?

어느정도 수준으로 써야 되는거지 감이 잘 오지않았다.

이 글을 이해하려면 최소한 git을 사용해 본 사람  clone,commit,push 

로컬환경, github를 왜 사용하는지 정도 알아야하지 싶다.

<br> 
<hr>
<br>




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
</div>

<br>
<hr>
<br>


<div style='width: 100%;'>1. 레지파지토리를 생성하자</div>

<figure>
	<img style='width:1200px;' src="{{ '/assets/img/post/b1/t1.png' | prepend: site.baseurl }}" alt=""> 
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

<div style='width: 100%;'>2. 본인 컴퓨터에 블로그를 관리할 환경을 구축하자.</div>

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/b1/t2.png' | prepend: site.baseurl }}" alt=""> 
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
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/b1/t3.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> index.html 생성 </figcaption>
</figure>


간단하게 html 파일을 만들어서 적용시켜보자 

본인 환경에 index.html을 만들고 git push를 한다.

<pre class="highlight">
  <code>
    $git status
    $git add *
    $git commit -m "템플릿 적용"
    $git push origin master
  </code>
</pre>

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/b1/t4.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 블로그 확인 </figcaption>
</figure>


<p style='font-size:20px;'>
  [본인 Github 아이디].github.io 입력하고 확인해보면 출력화면이 확인할 수 있다.
</p>

<br>
<hr>
<br>

<div style='width: 100%;'>4. Jekyll 테마를 적용시켜보자</div>
<br>

<a href=" http://jekyllthemes.org/" target="_blank" > 테마 페이지</a> 여기서 원하는 테마를 선택한다.

<figure>
	<img style='width:1200px; height:600px;' src="{{ '/assets/img/post/b1/t5.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> jekyllthemes 메인화면 </figcaption>
</figure>

<p style='font-size:20px;'>
수많은 테마들이 있다 필자는 <a href="http://jekyllthemes.org/themes/long-haul/" target="_blank" > Long Haul </a> 테마를 선택하였다. (딱히 이유는 없다.)
</p>

<figure>
	<img style='width:1200px; height:600px;' src="{{ '/assets/img/post/b1/t6.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> Long Haul 메인화면 </figcaption>
</figure>

테마를 선택하고 Demo를 클릭! 

Detail한 화면을 확인하고 최종적으로 고르길 바란다.

최종적으로 선택했다면 적용시키는 방법은 여러가지가 있다. 

1. fork 
2. download 

원리는 둘다 똑같다. 본인 로컬환경에 clone 하여 적용시키는 것이다.

<br>
<div style='width: 100%;'>4-1. fork</div>

Long Haul 메인화면에 HomePage를 클릭하여 페이지에 들어간다.

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/b1/t7.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> Long Haul Github 페이지 </figcaption>
</figure>

빨간색 표시되어있는 fork를 클릭.

<figure>
	<img style='width:1200px; height:200px;' src="{{ '/assets/img/post/b1/t8.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> Long Haul Github 페이지 </figcaption>
</figure>

빨간색 표시되어있는 setting를 클릭.


<figure>
	<img style='width:1200px; height:300px;' src="{{ '/assets/img/post/b1/t9.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> setting 페이지 </figcaption>
</figure>

<strong> 1.레파지토리 생성 </strong> 했을떄 이름과 같이 설정해주면 된다.

필자는 이미 같은 이름을 가진 레파지토리가 있다.

레파지토리 생성전에 사용하는 방식이다 

필자도 블로그를 작성하면서 알게되었다. 

그래서 쓸까말까 하다 추가하게 되었다. 알아두자.

가장 간단한 방법이다.

레파지토리 이름 ->   [본인 Github 아이디].github.io 설정 후 

블로그를 확인해보면 테마가 적용된 것을 확인할 수 있다.

<div style='width: 100%;'>4-2. download</div>
<br>

Long Haul 메인화면에서 소스를 다운받아 로컬 환경에 붙여넣고

 git push를 하면 끝이다. 정말 간단하다. 


<hr>
<br>
<strong>다음 장엔 jekyll로 블로그 생성 및  어떻게 글을 작성하고 </strong> 
<br>
<strong>테스트 하는지에 대해 알아보겠다. </strong> 


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