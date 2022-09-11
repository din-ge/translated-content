---
title: Especificidade
slug: Web/CSS/Specificity
translation_of: Web/CSS/Specificity
---
<h2 id="O_Conceito">O Conceito</h2>

<p>A especificação é a maneira de como os navegadores definem quais valores de propriedades são os mais relevantes para o elemento a ser utilizado. A especificação é baseada apenas nas regras impostas na composição de diferentes tipos de <a href="/en/CSS/CSS_Reference#Selectors" title="en/CSS/CSS_Reference#Selectors">seletores</a>.</p>

<h2 id="Como_isso_é_calculado">Como isso é calculado?</h2>

<p>A espeficicação é calculada na concatenação da contagem de cada tipo de seletor. Não é um peso aplicado na expressão correspondente.</p>

<p>No caso de igualdade de especificação, a última declaração encontrada no CSS é aplicada ao elemento.</p>

<div class="note">Note: O fato de elementos estarem próximos na árvore do documento não tem efeito sobre a especificação.</div>

<h3 id="Ordem_crescente_de_especificação">Ordem crescente de especificação</h3>

<p>A seguinte lista de seletores está incluida na especificação:</p>

<ul>
 <li>Seletores Universais</li>
 <li>Tipo de Seletores</li>
 <li>Classes seletoras</li>
 <li>Atributos Seletores</li>
 <li>Pseudo-classes</li>
 <li>Seletores ID</li>
 <li>Estilo Inline</li>
</ul>

<h3 id="A_exceção_!important">A exceção <code>!important</code></h3>

<p>Quando a regra <code>!important</code> é utilizada na declaração do estilo substitui qualquer outra declaração feita no CSS, onde quer que esteja na lista de declaração. Contudo, <code>!important</code> não tem nada a ver com especificação. </p>

<h3 id="A_exceção_not">A exceção <code>:not</code></h3>

<p>A pseudo-classe de negação <code>:not</code> não é considerada uma pseudo-classe no cálculo de especificação. Contudo, seletores colocados na pseudo-class de negação são entendidos como seletores normais.</p>

<p>Aqui está um trecho de CSS:</p>

<pre class="brush: css">div.outer p {
  color:orange;
}
div:not(.outer) p {
  color: lime;
}
</pre>

<p>Usado com o seguindo código HTML:</p>

<pre class="brush: html">&lt;div class="outer"&gt;
  &lt;p&gt;Esta é a div outer.&lt;/p&gt;
  &lt;div class="inner"&gt;
    &lt;p&gt;Este texto está na div inner.&lt;/p&gt;
  &lt;/div&gt;
&lt;/div&gt;
</pre>

<p>Irá aparecer na tela assim:</p>

<p>Esta é a div outer.</p>

<p>Este texto está na div inner.</p>

<h3 id="Especificação_Form-based">Especificação Form-based</h3>

<p>A especificação é baseada na forma de um seletor. No seguinte caso, o seletor contém os atributos no algoritmo de determinação de especificação, embora ele selecione um ID.</p>

<p>A seguir veja as declarações de estilo:</p>

<pre class="brush: css">* #foo {
  color: green;
}
*[id="foo"] {
  background: purple;
}
</pre>

<p>Usado com esta marcação:</p>

<pre class="brush: html">&lt;p id="foo"&gt;Eu sou um simples texto.&lt;/p&gt;
</pre>

<p>Vai acabar parecendo algo como:</p>

<p>Eu sou um simples texto.</p>

<p>Porque coincide com o mesmo elemento, mas o seletor de ID tem uma especificação superior.</p>

<h3 id="Estrutura_aproximada">Estrutura aproximada</h3>

<p>A seguir a declaração do estilo:</p>

<pre class="brush: css">body h1 {
  color: green;
}
html h1 {
  color: purple;
}
</pre>

<p>Com o HTML seguinte::</p>

<pre class="brush: html">&lt;html&gt;
&lt;body&gt;
  &lt;h1&gt;Aqui está o título!&lt;/h1&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>

<p>Vamos ter algo como:</p>

<p>Aqui está o título!</p>

<h2 id="Veja_Também">Veja Também</h2>

<ul>
 <li>Espcificação de Seletores CSS - <a class="external" href="http://www.w3.org/TR/selectors/#specificity" rel="freelink">http://www.w3.org/TR/selectors/#specificity</a></li>
 <li>{{ CSS_key_concepts() }}</li>
</ul>