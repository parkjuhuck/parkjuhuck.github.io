---
layout: post
title:  "알고리즘의 기본"
date:   2018-08-25
---

<br>
<br>
<h3 style='width: 100%;'>알고리즘이란?</h3>
<br>
<p style='width: 100%;'>
    <label style='font-size: 30px; font-weight:blod; color:green;'><strong>정의</strong></label>
    <strong >&nbsp;&nbsp;&nbsp; 문제나 과제를 해결하기 위한 처리 절차.</strong> <br>
    <br> 
    <label style='font-size: 30px; font-weight:blod; color:green;'><strong>예시</strong></label>
    &nbsp;&nbsp;&nbsp; - 요리의 레시피<br>
    &nbsp;&nbsp;&nbsp; - 악보<br>
    &nbsp;&nbsp;&nbsp; - 사용설명서<br>
    &nbsp;&nbsp;&nbsp; - 프로그램<br>
    <br>
    <strong style='font-size:20px;'>&nbsp;&nbsp;&nbsp;
    '알고리즘' 처음 들었을 때 어렵다고 느꼈다. 하지만 알고리즘은 우리 일상생활에서 흔히 볼수 있다.  <br>
    알고리즘은 한마디로 '절차'다. 답이 정해져있지 않다.  문제를 해결하기위한 절차, 과정이라 볼수 있다. <br>
    프로그래밍 언어로 기술한 알고리즘이 프로그램이다.
    </strong>    

</p>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>프로그램 작성에 있어서의 알고리즘</h4></p>

<figure>
	<img style='width:900px;' src="{{ '/assets/img/post/al/p1/flow1.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 프로그램 작성의 흐름 </figcaption>
</figure>

<p style='width: 100%; font-weight:bold; '> 1. 프로그래밍의 시작은 요구 </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그램 작성의 계기가 되는 것은 바로 <strong style='color:red;'>요구</strong>(Needs)다.<br>
  <br>
  &nbsp;&nbsp;&nbsp;고객이 요구한 내용과 기능, 사양을 기록한 문서를 '요구사항 정의서'라고 한다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 2. 프로그램 설계 </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;요구사항 정의서나 기획서에 요구하는 바가 어느 정도 나타나 있다면,<br>
  <br>
  &nbsp;&nbsp;&nbsp;요구에 부응하기 위해서는 어떠한 기능이 필요하고 어떤 프로그램을 만들면<br>
  <br>
  &nbsp;&nbsp;&nbsp; 좋은지를 고려해야한다. 이를 <strong style='color:red;'>'프로그램의 설계'</strong>라 한다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 3. 프로그래밍하기 </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;알고리즘이 정해진 후에는 프로그래밍(<strong style='color:red;'>'코딩'</strong>)을 해야 한다. <br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 4. 프로그램 디버깅하기 </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그램이 완성되었다면 동작 테스트를 실시해야한다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;프로그램이 문제없이 동작하는지 확인 하고 프로그램이 정상적으로 <br>
  <br>
  &nbsp;&nbsp;&nbsp;동작하지 않는 경우에는 어디에 문제가 있는지 오류를 찾아 수정하야 하는 해야한다.<br>
  <br>
  &nbsp;&nbsp;&nbsp;이를 <strong style='color:red;'>'디버그'</strong>라 한다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 5.프로그램 문서 작성 </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그램을 완성한 후에는 <strong style='color:red;'>문서</strong>(Document)를 작성해야한다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;프로그래머를 위한 문서와 사용자를 위한 문서가 있다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;<strong style='color:red;'>프로그래머를 위한 문서</strong>가 필요한 이유는 프로그램을 만든 사람이 향후 보수 및 관리까지 <br>
  <br>
  &nbsp;&nbsp;&nbsp;반드시 담당한다고 말할 수 없기 때문이다. 프로그램의 오류를 수정하거나 새로운 기능을<br>
  <br>
  &nbsp;&nbsp;&nbsp; 추가할 때 문제없이 작업을 진행할수 있도록 준비해 두는 것이 좋다.<br>
  <br>
  &nbsp;&nbsp;&nbsp;<strong style='color:red;'>사용자를 위한 문서</strong>는 '사용 설명서'를 말한다. 사용자가 프로그램을 사용하기위한 메뉴얼이다.<br>
<p>
<br>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>좋은 알고리즘이란?</h4></p>

<p style='width: 100%; font-weight:bold; '> 1. 알기쉽다. </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;다른사람들과 함께 작업할때 만든 알고리즘이 해석하기 쉽게 만들어야한다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;추후 기능을 수정하거나 추가할때 알고리즘이 난해하여 본인조차 이해하지 못하는 불상사가 일어날수 있다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 2.속도가 빠르다 </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그램 실행 후 그 결과가 나타날 떄까지의 시간이 짧다는 것을 의미한다. <br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 3. 효율적이다. </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그램을 실행할 때 사용하는 메모리의 영역이 작다.라는 것을 의미한다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 4. 재이용하기 쉽다. </p>
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;새로운 프로그램을 작성할때 과거에 작성한 프로그램('알고리즘')을 <br>
  <br>
  &nbsp;&nbsp;&nbsp;그대로 사용하거나 부분적으로 재사용하여 작성하는 시간을 줄일 수 있다.<br>
<p>
<br>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>왜 알고리즘을 공부해야 하는가?</h4></p>

&nbsp;&nbsp;&nbsp;<p style='width: 100%; font-weight:bold; '> 1. 좋은 프로램을 만들기 위해. </p>

&nbsp;&nbsp;&nbsp;<p style='width: 100%; font-weight:bold; '> 2.프로그램의 좋고 나쁨을 판단하기 위해 </p>

&nbsp;&nbsp;&nbsp;<p style='width: 100%; font-weight:bold; '> 3. 프로그램 작성 과정 전체를 효율화하기 위해 </p>

&nbsp;&nbsp;&nbsp;<p style='width: 100%; font-weight:bold; '> 4. 프로그래밍 기술을 향상시키기 위해</p>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>알고리즘이이기 위한 조건?</h4></p>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;알고리즘은 '절차'다. 하지만 절차라고 하여 무엇이든 알고리즘이라 할 수 없다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;알고리즘이 갖추어야 두가지 조건이 있다.<br>
<p>


<p style='width: 100%; font-weight:bold; '> 1. 정확한 결과를 얻을 수 있어야 한다. </p>

<p style='width: 100%; font-weight:bold; '> 2. 반드시 종료가 되어야 한다. </p>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>알고리즘의 세 가지 기본형</h4></p>

<figure>
	<img style='width:900px;' src="{{ '/assets/img/post/al/p1/al_type.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 알고리즘 기본 세가지 유형 </figcaption>
</figure>

<p style='width: 100%; font-weight:bold; '> 1. 순차 구조: 처음부터 순서대로 처리하는 절차 </p>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;실행하기 원하는 처리를 위에서부터 순서대로 작성하는 절차의 형태이다. <br>
<p>


<p style='width: 100%; font-weight:bold; '> 2. 선택 구조: 조건식으로 판단해 실행할 처리를 전환하는 절차 </p>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그래밍에서 if문 switch문과 같은 절차 형태이다. <br>
<p>

<p style='width: 100%; font-weight:bold; '> 3. 반복구조: 같은 처리를 반복하는 절차</p>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;프로그래밍에서 for믄, while문과 같이 동일한 처리를 반복하는 절차 형태이다. <br>
<p>

<br>
<hr>
<br>

<p><h4 style='width: 100%;'>알고리즘 기술 방법 - 순서도 </h4></p>

<p style='width: 100%; font-weight:bold; '> 순서도란?</p>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;순서도는 이름 그대로 알고리즘의 처리 흐름인 절차를 도형 기호를 사용하여 나타낸<br>
  <br>
  &nbsp;&nbsp;&nbsp;그림으로, '플로 차트'라고도 한다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 순서도에서 사용하는 주요 도형 기호  </p>

<figure>
	<img style='width:900px;' src="{{ '/assets/img/post/al/p1/flow_ex.png' | prepend: site.baseurl }}" alt=""> 
	<figcaption> 순서도 도형 설명 </figcaption>
</figure>

<br>
<hr>
<br>
<!-- 
<p><h4 style='width: 100%;'>알고리즘 기술 방법 - 의사언어 </h4></p>

<p style='width: 100%; font-weight:bold; '> 의사언어란??</p>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;의사언어는 순서도와 같이 기호를 사용 문자를 사용하여 알고리즘을 나타내는 프로그래밍 언어이다.<br>
<p>
<br>

<p style='width: 100%; font-weight:bold; '> 의사언어 작성 법  </p> -->

