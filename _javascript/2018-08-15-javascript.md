---
layout: post
title:  "함수형 프로그래밍 정의 , 순수함수"
date:   2018-08-15
---

<br>
<br>
<h3 style='width: 100%;'>함수형 프로그래밍이란</h3>
<br>

<p style='width: 100%;'>
    성공적인 프로그래밍을 위해 <strong style='color:red;'>부수효과</strong>를 피하고 <strong style='color:darkmagenta;'>조합성</strong>을 강조하는 프로그래밍 하는 것
</p>

<p style='width: 100%;'>
    부수효과를 피한다. -> 순수 함수를 만든다.<br>
    조합성을 강조 -> 모듈화 수준을 높인다. -> 생상성을 높인다 -> 성공적인 프로그래밍 
</p>

<br>
<hr>
<br>


<p><h4 style='width: 100%;'>순수함수란?</h4></p>
- 부수효과가 없는 함수 
- 동일한 인자가 같으면  항상 동일 한 결과를 리턴해주는 함수 
- 함수가 받은 인자외에 다른 어떤 외부의 상태에 영향을 끼치지 않는 함수
- 리턴값 외에는 외부와 소통 하는 것이 없는 함수

<p><h4 style='width: 100%;'>부수효과란?</h4></p>

함수가 리턴 값으로 결과를 만들어 내는 것 외에 외부의 상태에 <br>
영향을 미치는 것 

<br>
<hr>
<br>

<p><h4 style='width: 100%;'>예제</h4></p>

 <pre class="highlight">
  <code>
    /* 순수함수 예제 */
    function add(a,b) {
        return a + b ;
    }
    console.log( add(20,20) ); // 결과값 40
    console.log( add(20,20) ); // 결과값 40
    console.log( add(20,20) ); // 결과값 40
  </code>
</pre>
항상 동일한 인자를 넣으면 동일한 결과값을 리턴해준다.
<br><br>
<p><h4 style='width: 100%;'>순수함수가 아닌 조건 </h4></p>

<div style='width: 90%;'> 1. 동일한 인자를 주었을 떄 상황에 따라 다른 결과를 리턴해주는 함수 </div>

<pre class="highlight">
  <code>
    /* 예제 */
    var c = 20
    function add2(a,b) {
        return a + b + c ;
    }
    console.log( add2(20,20) ); // 결과값 60
    console.log( add2(20,21) ); // 결과값 61
    console.log( add2(20,22) ); // 결과값 62

    c = 40 

    console.log( add2(20,20) ); // 결과값 80
    console.log( add2(20,20) ); // 결과값 81
    console.log( add2(20,20) ); // 결과값 82
  </code>
</pre>

  변수 c가 상수 ( const ) 였다면 add2 함수는 순수함수 였을 것이다. <br>
  같은 인자를 받았지만 변수 c로 인해 add2 함수의 결과값이 달라졌기 때문에 <br>
  add2 함수는 순수함수가 아니다.

<p style='width: 100%;'> 2. 부수효과를 일으키는 함수 </p>

<div style='width: 100%;' > &emsp;2-1 외부의 상태를 변경하는 함수</div>

 <pre class="highlight">
  <code>
    /* 예제 */
    var c = 10;
    function add3(a,b) {
        c = b;
        return a + b ;
    }

    console.log( 'c :', c ); // 결과값 c: 10
    console.log( add3(20,20) ); // 결과값 40
    console.log( 'c :', c ); // 결과값 c: 20
  </code>
</pre>

add3 함수는 리턴 값 외에 외부의 변수 c값을 변경한다. <br>
부수효과를 일으키기 때문에 add3은 순수함수 아니다.
<br>

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
    값으로 만들어서 리턴을 하고 있다.<br>
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
</p>


 <!-- 자바스크립트는 일급함수이다 
 함수를 값으로 다룰수 있다 
 함수를 변수에 담을수도 있고 
 변수에 담은 함수는 값으로도 활용할수도있다.인자로도 사용할수있다.   -->






<br>
<hr>
<br>