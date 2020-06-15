---
layout: post
title: "렉시컬 스코핑(lexical scoping)"
date: 2020-06-13
---

<style>
  p {
    margin: 10px 0  !important;
    font-size:16px;
    width:100% !important;
  }
  li {
    list-style-type : none;
  }
 
  textarea {
    background : none;
    width:100%;
    height: 122px;
    font-size:15px;
  }
  .inline {
    display: inline!important;
  }
  h5 { 
    width: 100% !important;
  }
</style>

<style>
pre[class*="language-"].line-numbers.line-numbers { padding-left: 0; }
pre[class*="language-"].line-numbers { position: relative; padding-left: 3.8em; counter-reset: linenumber; }
:not(pre) > code[class*="language-"], pre[class*="language-"] {background-color: #fdfdfd;-webkit-box-sizing: border-box;-moz-box-sizing: border-box;box-sizing: border-box;margin-bottom: 1em; }
pre[class*="language-"] { position: relative; margin: .5em 0; overflow: visible; padding: 0; }
code[class*="language-"], pre[class*="language-"] { color: black; background: none; font-family: Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace; font-size: 1em; text-align: left; white-space: pre; word-spacing: normal; word-break: normal; word-wrap: normal; line-height: 1.5; -moz-tab-size: 4; -o-tab-size: 4; tab-size: 4; -webkit-hyphens: none; -moz-hyphens: none; -ms-hyphens: none; hyphens: none; }
pre[class*="language-"].line-numbers.line-numbers code { font-size:14px; }
pre[class*="language-"].line-numbers > code { position: relative; white-space: inherit; }
pre[class*="language-"]>code { position: relative; border-left: 10px solid #358ccb; box-shadow: -1px 0px 0px 0px #358ccb, 0px 0px 0px 1px #dfdfdf; background-color: #fdfdfd;  background-image: linear-gradient(transparent 50%, rgba(69, 142, 209, 0.04) 50%); background-size: 3em 3em; background-origin: content-box; background-attachment: local; font-size:14px;}
code[class*="language"] { max-height: inherit; height: inherit; padding: 0 1em; display: block; overflow: auto; }
pre[class*="language-"].line-numbers > code { position: relative; white-space: inherit; }
.token.selector, .token.attr-name, .token.string, .token.char, .token.function, .token.builtin, .token.inserted { color: #2f9c0a; }
.token.atrule, .token.attr-value, .token.keyword, .token.class-name { color: #1990b8; }
pre[class*="language-"]>code { position: relative; border-left: 10px solid #358ccb; box-shadow: -1px 0px 0px 0px #358ccb, 0px 0px 0px 1px #dfdfdf; background-color: #fdfdfd; background-image: linear-gradient(transparent 50%, rgba(69, 142, 209, 0.04) 50%); background-size: 3em 3em; background-origin: content-box; background-attachment: local;
}
</style>

<br>
<p>렉시컬 스코핑(lexical scoping)린 코드를 작성할때 변수를 어디에 작성하는가를 바탕으로 스코프가 결정되는 것 입니다.</p>
<hr/>

<h5>렉시컬 스코핑(lexical scoping)</h5>

<p><strong>스코프</strong>는 함수를 호출할 때가 아니라 <strong>선언</strong>할 때 생깁니다.</p>

<pre data-reactroot="" class=" line-numbers  language-jsx"><code class="  language-jsx"><span class="token keyword">var</span> name <span class="token operator">=</span> <span class="token string">'zero'</span><span class="token punctuation">;</span>
<span class="token keyword">function</span> <span class="token function">log</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">function</span> <span class="token function">wrapper</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  name <span class="token operator">=</span> <span class="token string">'nero'</span><span class="token punctuation">;</span>
  <span class="token function">log</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token function">wrapper</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span aria-hidden="true" class="line-numbers-rows"><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span></span></code></pre>

<p>console에 찍힌 값은 nero입니다. log를 호출하기 전에 name을 'nero'로 바꿨거든요. </p>

<pre data-reactroot="" class=" line-numbers  language-jsx"><code class="  language-jsx"><span class="token keyword">var</span> name <span class="token operator">=</span> <span class="token string">'zero'</span><span class="token punctuation">;</span>
<span class="token keyword">function</span> <span class="token function">log</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  console<span class="token punctuation">.</span><span class="token function">log</span><span class="token punctuation">(</span>name<span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>

<span class="token keyword">function</span> <span class="token function">wrapper</span><span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">var</span> name <span class="token operator">=</span> <span class="token string">'nero'</span><span class="token punctuation">;</span>
  <span class="token function">log</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span>
<span class="token function">wrapper</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span><span aria-hidden="true" class="line-numbers-rows"><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span></span></code></pre>

<p>console에 찍힌 값은 zero입니다. 스코프는 함수를 <strong>선언</strong>할 때 생긴다고 했죠? log 안의 name은 wrapper 안의 지역변수 name이 아니라, 전역변수 name을 가리키고 있는 겁니다. 이런 것을 <strong>lexical scoping(정적 스코프)</strong>이라고 합니다.</p>

함수를 처음 선언하는 순간, 함수 내부의 변수는 자기 스코프로부터 가장 가까운 곳(상위 범위에서)에 있는 변수를 계속 참조하게 됩니다. 위의 예시에서는 log 함수 안의 name 변수는 선언 시 가장 가까운 전역변수 name을 참조하게 됩니다. 그래서 wrapper 안에서 log를 호출해도 지역변수 name='nero'를 참조하는 게 아니라 그대로 전역변수 name의 값인 zero가 나오는 겁니다.
