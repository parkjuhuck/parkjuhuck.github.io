---
layout: post
title: "let,const,var"
date: 2020-06-14
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
<p>let,const,var의 차이를 알고있느냐? 라는 면접질문을 여러번 받았었다. 이건 자바스크립트 개발자라면 100퍼센트 알거라고 생각한다. 
요즘 자바스크립트 개념 공부 및 블로그를 작성해보니 이 질문을 건넨 면접자의 의도는 단순히 개념을 알고있는냐가 아닌 스코프와 호이스팅의 개념을 어느정도 깊이있게 알고있는가 라는 생각이 들었다.
</p>
<hr/>

<h5>렉시컬 스코핑(lexical scoping)</h5>

<p><strong>스코프</strong>는 함수를 호출할 때가 아니라 <strong>선언</strong>할 때 생깁니다.</p>
