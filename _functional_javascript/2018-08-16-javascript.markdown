---
layout: post
title:  "일급함수, add_maker, 함수로 함수 실행하기"
date:   2018-08-16
---

<br>
<br>
<h3 style='width: 100%;'>일급함수란?</h3>
<br>
<p style='width: 100%;'>
    <label style='font-size: 30px; font-weight:blod; color:green;'><strong>정의</strong></label>
    <strong>&nbsp;&nbsp;&nbsp;- 프로그래밍에서 다른 값과 동일하게 처리되는 값.</strong> <br>
    <strong>&nbsp;&nbsp;&nbsp;- 함수를 값으로 다를수 있는 개념 </strong> <br>
    <strong>&nbsp;&nbsp;&nbsp;- 스스로 객체로 취급되는 함수 (일급객체) </strong> <br>
    <br> 
    <label style='font-size: 30px; font-weight:blod; color:green;'><strong>특징</strong></label>
    &nbsp;&nbsp;&nbsp; - 변수에 값(함수)을 할당 할 수 있다.<br>
    &nbsp;&nbsp;&nbsp; - 함수에 값(함수)을 전달한다.<br>
    &nbsp;&nbsp;&nbsp; - 함수에서 값(함수)을 반환한다.<br>
    <br>
    <strong style='font-size:20px;'>&nbsp;&nbsp;&nbsp;
    즉 함수를 변수에 할당할 수도 있고 객체에 추가할 수도 있으며  다른 함수에 인수로 전달하거나 함수에서 함수를 반환할 수도 있다. 참조 값을 쓸 수 있는 곳이라면 어디든 함수도 사용할 수 있다.
    </strong>    
</p>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>예제로 보는 일급함수 특징</h4></p>

<div style='width: 90%; font-weight:bold; '> 1. 변수에 값을 할당한다.</div>

<pre class="highlight">
  <code>
    var f1 = function(a) {
        return a *a;
    }

    console.log( f1) ); // 결과 function(a) { return a * a } 
  </code>
</pre>
  
<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;함수를 만들어 f1 변수에 저장 하였다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;출력을 해보면 정의한 함수가 값으로 출력됨을 확인 할 수 있다.<br>
  <br>
  &nbsp;&nbsp;&nbsp;첫번째 특징 변수에 함수를 할당 할 수 있다.
<p>

<div style='width: 90%; font-weight:bold; '> 2. 함수에 값(함수)을 전달한다. </div>
 <pre class="highlight">
  <code>
    function f2(f) {
      return f();
    }
    
    f2 ( function() { return 10; })

  </code>
</pre>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;f2 함수를 정의하고 파라미터로 함수를 받아 return 값을 함수를 호출하게 만들었다.<br>
  <br>
  &nbsp;&nbsp;&nbsp; 함수를 호출 할 때  인자로 함수를 전달한다. <br>
  <br>
  &nbsp;&nbsp;&nbsp; 전달받은 함수를 return으로 호출한다.  <br>
<p>

<div style='width: 90%; font-weight:bold; '> 3. 함수에서 값(함수)을 반환한다. </div>
 <pre class="highlight">
  <code>
    function add_maker(a) {
      return function(b){
        return a + b; 
    }
  
    var add20 = add_maker(10);

    console.log ( add20(20) );

    /* 
      add20 변수에 담긴 값은 

        function(b) {
          return 10 + b ;
        }

        add20(20)에 결과 값은 

        function(20) {
          return 10 + 20 ;
        }
        이므로 30이 출력되게 된다.
    */


  </code>
</pre>

<p style='width: 100%; font-size:20px; font-weight:bold;'>
  &nbsp;&nbsp;&nbsp;필자는 저 코드를 한번에 이해하지 못했다. 눈으로만 코드를 해석해서였고 코드자체가 생소했다. <br>
  <br>
  &nbsp;&nbsp;&nbsp;직접 코드를 치고 확인하고 나서야 이해가 됐다. <br>
  <br>
  &nbsp;&nbsp;&nbsp; add_maker 함수는 return 값으로 함수(값)를 호출하지 않고 반환! 한다.<br>
  <br>
  &nbsp;&nbsp;&nbsp; 반환한 함수를 변수에 저장해서 변수(함수)를 호출하는 것이다.   <br>
<p>


<!-- 일급함수 + 순수함수 + 클로져  -->
<!-- 
<div style='width: 100%;' > &emsp; 2-2 들어온 인자의 상태를 직접 변경하는 함수 </div>
 
<pre class="highlight">
  <code>
    /* 예제 */
    var obj1 = { value: 10 };
    function add4(obj, b) {
        obj.val += b;
    }
    console.log( obj.val ); //결과값 10
    add4(obj1,20);
    console.log( obj1.val ); // 결과값 30
  </code>
</pre>

add4 함수는 리턴값도 없고 인자로 들어온 값을 변경하는 부수를 일으키는<br>
함수이다.


<br>
<hr>
<br>

<p style='font-size:19px;'>
    add4 함수는 들어온 인자(객체)를 변경하였다. <br>
    <br>
    우리는 데이터를 다룰때 숫자와 문자 보다는 객체를 주로 다룬다. <br>
    <br>
    그렇다면 순수함수는 객체의 상태를 변경할수 없을까? <br> 
    <br>
    그리고 순수함수로 프로그래밍하는 함수프로그래밍에서는 이런 객체를 다룰수 없을까?  <br>
    <br>
    순수함수에서는 객체의 값들을 변형해 나가는데 그 방법을 다른 방법을 통해서 객체의 값<br>
    <br>
    을 변형해 나간다. <br>
    <br>
    <strong>원래있던 객체의 값은 그대로 두고 객체를 복사해서 <br>
    <br>
    원하는 형태로 변형시키고 그 값을 리턴한다. </strong><br>
    <br>
    add4와 동일한 역할을 하지만 외부상태에 영향을 미치지 않는 순수함수를 만들어보자.  
</p>

<br>
<hr>
<br>

<pre class="highlight">
  <code>
    /* 객체를 다루는 순수함수 예제 */
    var obj1 = { value: 10 };
    function add5(obj, b) {
        return { val: obj.val + b };
    }
    console.log( obj1.val ); //결과값 10
    var obj2 = add5(obj1,20);
    console.log( obj1.val ); //결과값 동일
    console.log( obj2.val ); // 객체를 새로 생성하여 저장
  </code>
</pre>


<p style='font-size:19px;'>
    add5 함수는 obj1객체를 참조만 할뿐 값을 직접 변경하는 곳은없다<br>
    <br>
    obj1 객체와 동일하게 생긴 새로운 객체를 리턴하면서 val에 해당하는 부분이 더해진 <br>
    값으로 만들어서 리턴을 하고있다.<br>
    <br>
    add5 함수는 받은 인자의 상태를 변경하거나 외부 상태에 어떠한 영향을 미치지 않는<br> 
    순수함수이다. <br> 
    <br>
    obj2 새로은 객체가 20을 더해진 값을 가진 객체가 된다.<br>
    <br>
    순수함수에서는 객체의 값들을 변형해 나가는데 그 방법을 다른 방법을 통해서 객체의 값<br>
    을 변형해 나간다. <br>
    <br>
</p>
<hr>

<p><h4 style='width: 100%;'>마무리</h4></p>

<p style='font-size:19px;'>
    <strong>함수형 프로그래밍은 데이터를 다룰때 원래 초기화되어있는 데이터를 건들지 않는다.<br>
    <br>
    모든 데이터(외부,인자)들에 대한 변화를 일으키지 않고<br>
    <br>
    인자로 받은값을  직접 변경하지 않으면서 데이터를 변형해 나가는 프로그래밍이다.<br></strong>
</p> -->


 <!-- 자바스크립트는 일급함수이다 
 함수를 값으로 다룰수 있다 
 함수를 변수에 담을수도 있고 
 변수에 담은 함수는 값으로도 활용할수도있다.인자로도 사용할수있다.   -->






<br>
<hr>
<br>