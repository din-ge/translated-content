---
title: element.length
slug: Web/API/NodeList/length
tags:
  - DOM
  - Gecko
  - Gecko DOM Reference
translation_of: Web/API/NodeList/length
---
<p>{{ ApiRef() }}</p>
<h3 id=".EC.9A.94.EC.95.BD" name=".EC.9A.94.EC.95.BD">요약</h3>
<p><code>length</code>는 <code>NodeList</code>의 항목수를 반환합니다.</p>
<h3 id=".EA.B5.AC.EB.AC.B8" name=".EA.B5.AC.EB.AC.B8">구문</h3>
<pre class="eval"><i>numItems</i> =<i>nodeList</i>.length
</pre>
<ul>
 <li><code>numItems</code>은 <code>NodeList</code>의 항목수를 나타내는 정수값입니다.</li>
</ul>
<h3 id=".EC.98.88" name=".EC.98.88">예</h3>
<pre>// 문서의 모든 paragraph
var items = document.getElementsByTagName("p");
// 목록의 각 항목에,
// HTML의 문자열로 전체 요소를 추가
var gross = "";
for (var i = 0; i &lt; items.length; i++) {
  gross += items[i].innerHTML;
}
// gross는 이제 모두 paragraph을 위한 HTML
</pre>
<h3 id=".EC.A3.BC.EC.9D.98" name=".EC.A3.BC.EC.9D.98">주의</h3>
<p>reference에서 이 페이지의 위치에도 불구하고, <code>length</code>는 <a href="ko/DOM/element">Element</a>의 프로퍼티가 아니고, <code>NodeList</code>의 프로퍼티입니다. NodeList 개체는 <a href="ko/DOM/document.getElementsByTagName">document.getElementsByTagName</a>과 같은 많은 DOM 메소드에서 반환됩니다.</p>
<p><code>length</code>는 DOM 프로그래밍에서 아주 흔한 프로퍼티입니다. 위 예에서처럼 목록의 길이(적어도 있는 지 보기 위해)를 조사하고 for 루프에서 훑개(반복자, iterator)로 널리 쓰입니다.</p>

<h3 id="명세">명세</h3>

{{Specifications}}