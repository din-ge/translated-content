---
title: contenteditable
slug: Web/HTML/Global_attributes/contenteditable
tags:
  - HTML
  - Глобальные атрибуты
  - Определение
translation_of: Web/HTML/Global_attributes/contenteditable
---
<p>{{HTMLSidebar("Global_attributes")}}</p>

<p><font> (Mozilla / 5.0 (Windows NT 6.3, WOW64; rv: 29.0) Gecko / 20100101 Firefox / 29.0) </font><br>
 Атрибут <code><strong>contenteditable</strong></code> <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes">global attribute</a> - это перечисляемый атрибут, указывающий, должен ли элемент редактироваться пользователем. Если это так, браузер изменит свой виджет, чтобы разрешить редактирование. Атрибут должен принимать одно из следующих значений:</p>

<ul>
 <li><span style="font-family: courier new;">true</span> или <em>пустую строку</em>, которое показывает, что элемент должен быть редактируемым;</li>
 <li><span style="font-family: courier new;">false</span>, которое показывает, что элемент должен быть нередактируемым.</li>
</ul>

<p>Если атрибут не указан, то его значение <em>наследуется</em> от своего родительского элемента.</p>

<p>Этот атрибут <em>принимает одно из определённых значений</em> и не является <em>булевским</em>. Это значит, что точное использование одного из значений <code>true, false</code> или пустая строка обязательно и такое сокращение, как <code>&lt;label contenteditable&gt;Пример метки&lt;/label&gt; </code>неразрешено. Верное использование — <code>&lt;label contenteditable="true"&gt;Пример метки&lt;/label&gt;</code>. </p>

<p>Вы можете установить цвет, используемый для вставки текста {{Glossary("caret")}}<br>
 со свойством CSS {{cssxref("caret-color")}}.  </p>

<h2 id="Спецификации">Спецификации</h2>

{{Specifications}}

<h2 id="Совместимость">Совместимость</h2>

<p>{{Compat}}</p>

<h2 id="Смотрите_также">Смотрите также</h2>

<ul>
 <li><a href="/ru/docs/Web/Guide/HTML/Editable_content">Создание контента для редактирования</a></li>
 <li>Все <a href="/ru/docs/Web/HTML/Общие_атрибуты">глобальные атрибуты</a></li>
 <li>{{domxref("HTMLElement.contentEditable")}} и {{domxref("HTMLElement.isContentEditable")}}</li>
</ul>