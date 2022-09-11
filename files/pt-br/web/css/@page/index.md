---
title: '@page'
slug: Web/CSS/@page
tags:
  - '@page'
  - CSS
  - pagina
translation_of: Web/CSS/@page
---
<div>{{CSSRef}}</div>

<h2 id="Resumo">Resumo</h2>

<p>A regra CSS <code>@page</code> é utilizada para modificar algumas propriedades CSS quando o documento for impresso.<strong> </strong>Você não pode mudar todas as propriedades CSS com @page. Você poderá somente mudar as margens, orphans, widows, e page breaks do documento. Na tentativa de mudar outra propriedade CSS, elas serão ignoradas.</p>

<p>A regra CSS <code>@page</code> pode ser acessada via interface do modelo de objeto {{domxref("CSSPageRule")}}.</p>

<div class="note"><strong>Nota:</strong> A W3C está analisando como lidar com unidades viewport-related {{cssxref("&lt;length&gt;")}}, <code>vh</code>, <code>vw</code>, <code>vmin</code>, and <code>vmax</code>. Enquanto isso, não use eles junto com a regra @page.</div>

<h2 id="Sintaxe">Sintaxe</h2>

<pre class="syntaxbox">@page :pseudo-class {
  margin:2in;
}
</pre>

<h2 id="Exemplos">Exemplos</h2>

<p>Podemos fazer referência a vários <a href="/en-US/docs/CSS/Pseudo-classes" title="Pseudo-classes">pseudo-classes</a> de <code>@page</code> por exemplo.</p>

<ul>
 <li>{{Cssxref(":first")}}</li>
 <li>{{Cssxref(":left")}}</li>
 <li>{{Cssxref(":right")}}</li>
</ul>

<h2 id="Especificações">Especificações</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Status</th>
   <th scope="col">Comment</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName('CSS3 Paged Media', '#at-page-rule', '@page')}}</td>
   <td>{{Spec2('CSS3 Paged Media')}}</td>
   <td>Sem mudanças para {{SpecName('CSS2.1')}}, though more CSS at-rules can be used inside a <code>@page</code>.</td>
  </tr>
  <tr>
   <td>{{SpecName('CSS2.1', 'page.html#page-selectors', '@page')}}</td>
   <td>{{Spec2('CSS2.1')}}</td>
   <td> </td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility">Compatibilidade com navegadores</h2>

{{Compat("css.at-rules.page")}}