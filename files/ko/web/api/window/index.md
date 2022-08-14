---
title: Window
slug: Web/API/Window
tags:
  - API
  - DOM
  - Interface
  - JavaScript
  - Reference
  - Window
translation_of: Web/API/Window
---
<div>{{APIRef("DOM")}}</div>

<p><span class="seoSummary"><strong><code>Window</code></strong> 인터페이스는 {{glossary("DOM")}} 문서를 담은 창을 나타냅니다.</span> <code>document</code> 속성이 창에 불러온 <a href="/ko/docs/Web/API/Document">DOM 문서</a>를 가리킵니다. 반대로, 주어진 문서의 창은 {{domxref("document.defaultView")}}를 사용해 접근할 수 있습니다.</p>

<p>JavaScript 코드에 노출된 전역 변수 <code>window</code>는 현재 스크립트가 작동 중인 창을 나타냅니다.</p>

<p><code>Window</code> 인터페이스는 다양한 함수, 이름공간, 객체, 생성자가 머무는 장소입니다. 그 중엔 사용자 인터페이스로서의 창 개념과는 직접 관련되지 않은 것도 존재하며, 대신 전역적으로 접근할 수 있어야 하는 항목에 적합합니다. 많은 수의 항목이 <a href="/ko/docs/Web/JavaScript/Reference">JavaScript 참고서</a>와 <a href="/ko/docs/Web/API/Document_Object_Model">DOM 참고서</a>에 문서화되어 있습니다.</p>

<p>탭 기능이 있는 브라우저에서는 각각의 탭을 각각의 <code>Window</code> 객체로 나타냅니다. 주어진 탭에서 동작 중인 JavaScript 코드의 전역 <code>window</code> 객체는 항상 자신의 탭을 나타냅니다. 그렇지만 {{domxref("Window.resizeTo", "resizeTo()")}}와 {{domxref("Window.innerHeight", "innerHeight")}}처럼, 일부 속성과 메서드는 탭이 아닌 창 전체에 적용됩니다. 보통 탭과 합리적으로는 연관 지을 수 없는 경우 창에 속합니다.</p>

<p>{{InheritanceDiagram}}</p>

<h2 id="생성자">생성자</h2>

<p><a href="/ko/docs/Web/API/Document_Object_Model#DOM_인터페이스" title="/en-US/docs/DOM/DOM_Reference">DOM 인터페이스</a>도 참고하세요.</p>

<dl>
 <dt>{{domxref("DOMParser")}}</dt>
 <dd><code>DOMParser</code>는 문자열에 저장한 XML 또는 HTML 소스 코드를 DOM {{domxref("Document")}}로 구문 분석할 수 있습니다. <code>DOMParser</code>는 <a href="https://w3c.github.io/DOM-Parsing/">DOM Parsing and Serialization</a> 명세의 일부입니다.</dd>
 <dt>{{domxref("Image")}}</dt>
 <dd>{{domxref("HTMLImageElement")}}를 생성할 때 사용합니다.</dd>
 <dt>{{domxref("Option")}}</dt>
 <dd>{{domxref("HTMLOptionElement")}}를 생성할 때 사용합니다.</dd>
 <dt>{{domxref("Window.StaticRange")}} {{experimental_inline}} {{readonlyinline}}</dt>
 <dd>{{domxref('StaticRange')}} 객체를 생성하는 {{domxref('StaticRange.StaticRange','StaticRange()')}} 생성자를 반환합니다.</dd>
 <dt>{{domxref("Worker")}}</dt>
 <dd><a href="/ko/docs/Web/API/Web_Workers_API/Using_web_workers">Web Worker</a> 생성에 사용합니다.</dd>
 <dt>{{domxref("Window.XMLSerializer")}}</dt>
 <dd>DOM 트리를 XML 또는 HTML 소스로 변환합니다.</dd>
</dl>

<h2 id="속성">속성</h2>

<p>{{domxref("EventTarget")}}의 속성을 상속하고, {{domxref("WindowOrWorkerGlobalScope")}}와 {{domxref("WindowEventHandlers")}} 믹스인의 속성을 구현합니다.</p>

<dl>
 <dt>{{domxref("Window.closed")}} {{readOnlyInline}}</dt>
 <dd>현재 창이 닫혔는지 나타냅니다.</dd>
 <dt>{{domxref("Window.console")}} {{readOnlyInline}}</dt>
 <dd>브라우저 디버깅 콘솔에 접근할 수 있는 콘솔 객체를 반환합니다.</dd>
 <dt>{{domxref("Window.controllers")}} {{ReadOnlyInline}} {{non-standard_inline}}</dt>
 <dd>현재 크롬 창의 XUL 컨트롤러 객체를 반환합니다.</dd>
 <dt>{{domxref("Window.customElements")}} {{ReadOnlyInline}}</dt>
 <dd>새로운 사용자 지정 요소를 등록하거나, 이전에 등록한 요소에 대한 정보를 얻을 수 있는 {{domxref("CustomElementRegistry")}} 객체를 반환합니다.</dd>
 <dt>{{domxref("Window.crypto")}} {{readOnlyInline}}</dt>
 <dd>브라우저 암호화 객체를 반환합니다.</dd>
 <dt>{{domxref("Window.devicePixelRatio")}} {{ReadOnlyInline}}</dt>
 <dd>현재 화면에서의 물리적 픽셀과 CSS 픽셀의 비율을 반환합니다.</dd>
 <dt>{{domxref("Window.document")}} {{ReadOnlyInline}}</dt>
 <dd>창이 포함하는 문서로의 참조를 반환합니다.</dd>
 <dt>{{domxref("Window.DOMMatrix")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMMatrix")}} object, which represents 4x4 matrices, suitable for 2D and 3D operations.</dd>
 <dt>{{domxref("Window.DOMMatrixReadOnly")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMMatrixReadOnly")}} object, which represents 4x4 matrices, suitable for 2D and 3D operations.</dd>
 <dt>{{domxref("Window.DOMPoint")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMPoint")}} object, which represents a 2D or 3D point in a coordinate system.</dd>
 <dt>{{domxref("Window.DOMPointReadOnly")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMPointReadOnly")}} object, which represents a 2D or 3D point in a coordinate system.</dd>
 <dt>{{domxref("Window.DOMQuad")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMQuad")}} object, which provides represents a quadrilaterial object, that is one having four corners and four sides.</dd>
 <dt>{{domxref("Window.DOMRect")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMRect")}} object, which represents a rectangle.</dd>
 <dt>{{domxref("Window.DOMRectReadOnly")}} {{readOnlyInline}} {{experimental_inline}}</dt>
 <dd>Returns a reference to a {{domxref("DOMRectReadOnly")}} object, which represents a rectangle.</dd>
 <dt>{{domxref("Window.event")}} {{ReadOnlyInline}}</dt>
 <dd>Returns the <strong>current event</strong>, which is the event currently being handled by the JavaScript code's context, or <code>undefined</code> if no event is currently being handled. The {{domxref("Event")}} object passed directly to event handlers should be used instead whenever possible.</dd>
 <dt>{{domxref("Window.frameElement")}} {{readOnlyInline}}</dt>
 <dd>이 창을 삽입했을 때 사용한 요소를 반환합니다. 창이 문서 내에 삽입된 것이 아니면 {{jsxref("null")}}을 반환합니다.</dd>
 <dt>{{domxref("Window.frames")}} {{readOnlyInline}}</dt>
 <dd>현재 창의 하위 프레임을 배열로 반환합니다.</dd>
 <dt>{{domxref("Window.fullScreen")}}</dt>
 <dd>현재 창을 전체 화면으로 보여주고 있는지 나타냅니다.</dd>
 <dt>{{domxref("Window.history")}} {{ReadOnlyInline}}</dt>
 <dd>Returns a reference to the history object.</dd>
 <dt>{{domxref("Window.innerHeight")}} {{readOnlyInline}}</dt>
 <dd>Gets the height of the content area of the browser window including, if rendered, the horizontal scrollbar.</dd>
 <dt>{{domxref("Window.innerWidth")}} {{readOnlyInline}}</dt>
 <dd>Gets the width of the content area of the browser window including, if rendered, the vertical scrollbar.</dd>
 <dt>{{domxref("Window.isSecureContext")}} {{experimental_inline}} {{readOnlyInline}}</dt>
 <dd>Indicates whether a context is capable of using features that require secure contexts.</dd>
 <dt>{{domxref("Window.length")}} {{readOnlyInline}}</dt>
 <dd>Returns the number of frames in the window. See also {{domxref("window.frames")}}.</dd>
 <dt>{{domxref("Window.location")}}</dt>
 <dd>Gets/sets the location, or current URL, of the window object.</dd>
 <dt>{{domxref("Window.locationbar")}} {{ReadOnlyInline}}</dt>
 <dd>Returns the locationbar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.localStorage")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the local storage object used to store data that may only be accessed by the origin that created it.</dd>
 <dt>{{domxref("Window.menubar")}} {{ReadOnlyInline}}</dt>
 <dd>Returns the menubar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.messageManager")}}</dt>
 <dd>Returns the <a href="/en-US/docs/The_message_manager">message manager</a> object for this window.</dd>
 <dt>{{domxref("Window.mozInnerScreenX")}} {{ReadOnlyInline}} {{non-standard_inline}}</dt>
 <dd>Returns the horizontal (X) coordinate of the top-left corner of the window's viewport, in screen coordinates. This value is reported in CSS pixels. See <code>mozScreenPixelsPerCSSPixel</code> in <code>nsIDOMWindowUtils</code> for a conversion factor to adapt to screen pixels if needed.</dd>
 <dt>{{domxref("Window.mozInnerScreenY")}} {{ReadOnlyInline}} {{non-standard_inline}}</dt>
 <dd>Returns the vertical (Y) coordinate of the top-left corner of the window's viewport, in screen coordinates. This value is reported in CSS pixels. See <code>mozScreenPixelsPerCSSPixel</code> for a conversion factor to adapt to screen pixels if needed.</dd>
 <dt>{{domxref("Window.name")}}</dt>
 <dd>Gets/sets the name of the window.</dd>
 <dt>{{domxref("Window.navigator")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the navigator object.</dd>
 <dt>{{domxref("Window.opener")}}</dt>
 <dd>현재 창을 열었던 다른 창의 참조를 반환합니다.</dd>
 <dt>{{domxref("Window.outerHeight")}} {{readOnlyInline}}</dt>
 <dd>브라우저 창 외곽 높이를 반환합니다.</dd>
 <dt>{{domxref("Window.outerWidth")}} {{readOnlyInline}}</dt>
 <dd>브라우저 창 외곽 너비를 반환합니다.</dd>
 <dt>{{domxref("Window.scrollX","Window.pageXOffset")}} {{readOnlyInline}}</dt>
 <dd>An alias for {{domxref("window.scrollX")}}.</dd>
 <dt>{{domxref("Window.scrollY","Window.pageYOffset")}} {{readOnlyInline}}</dt>
 <dd>An alias for {{domxref("window.scrollY")}}</dd>
 <dt>{{domxref("Window.parent")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the parent of the current window or subframe.</dd>
 <dt>{{domxref("Window.performance")}} {{readOnlyInline}}</dt>
 <dd>Returns a {{domxref("Performance")}} object, which includes the {{domxref("Performance.timing", "timing")}} and {{domxref("Performance.navigation", "navigation")}} attributes, each of which is an object providing <a href="/en-US/docs/Navigation_timing">performance-related</a> data. See also <a href="/en-US/docs/Web/API/Navigation_timing_API/Using_Navigation_Timing">Using Navigation Timing</a> for additional information and examples.</dd>
 <dt>{{domxref("Window.personalbar")}} {{readOnlyInline}}</dt>
 <dd>Returns the personalbar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.screen")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the screen object associated with the window.</dd>
 <dt>{{domxref("Window.screenX")}} and {{domxref("Window.screenLeft")}} {{readOnlyInline}}</dt>
 <dd>Both properties return the horizontal distance from the left border of the user's browser viewport to the left side of the screen.</dd>
 <dt>{{domxref("Window.screenY")}} and {{domxref("Window.screenTop")}} {{readOnlyInline}}</dt>
 <dd>Both properties return the vertical distance from the top border of the user's browser viewport to the top side of the screen.</dd>
 <dt>{{domxref("Window.scrollbars")}} {{readOnlyInline}}</dt>
 <dd>Returns the scrollbars object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.scrollMaxX")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>The maximum offset that the window can be scrolled to horizontally, that is the document width minus the viewport width.</dd>
 <dt>{{domxref("Window.scrollMaxY")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>The maximum offset that the window can be scrolled to vertically (i.e., the document height minus the viewport height).</dd>
 <dt>{{domxref("Window.scrollX")}} {{readOnlyInline}}</dt>
 <dd>Returns the number of pixels that the document has already been scrolled horizontally.</dd>
 <dt>{{domxref("Window.scrollY")}} {{readOnlyInline}}</dt>
 <dd>Returns the number of pixels that the document has already been scrolled vertically.</dd>
 <dt>{{domxref("Window.self")}} {{ReadOnlyInline}}</dt>
 <dd>Returns an object reference to the window object itself.</dd>
 <dt>{{domxref("Window.sessionStorage")}}</dt>
 <dd>Returns a reference to the session storage object used to store data that may only be accessed by the origin that created it.</dd>
 <dt>{{domxref("Window.sidebar")}} {{non-standard_inline}} {{ReadOnlyInline}}</dt>
 <dd>Returns a reference to the window object of the sidebar.</dd>
 <dt>{{domxref("Window.speechSynthesis")}} {{ReadOnlyInline}}</dt>
 <dd>Returns a {{domxref("SpeechSynthesis")}} object, which is the entry point into using <a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a> speech synthesis functionality.</dd>
 <dt>{{domxref("Window.status")}}</dt>
 <dd>Gets/sets the text in the statusbar at the bottom of the browser.</dd>
 <dt>{{domxref("Window.statusbar")}} {{readOnlyInline}}</dt>
 <dd>Returns the statusbar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.toolbar")}} {{readOnlyInline}}</dt>
 <dd>Returns the toolbar object, whose visibility can be toggled in the window.</dd>
 <dt>{{domxref("Window.top")}} {{readOnlyInline}}</dt>
 <dd>Returns a reference to the topmost window in the window hierarchy. This property is read only.</dd>
 <dt>{{domxref("Window.visualViewport")}} {{readOnlyInline}}</dt>
 <dd>Returns a {{domxref("VisualViewport")}} object which represents the visual viewport for a given window.</dd>
 <dt>{{domxref("Window.window")}} {{ReadOnlyInline}}</dt>
 <dd>Returns a reference to the current window.</dd>
 <dt><code>window[0]</code>, <code>window[1]</code>, etc.</dt>
 <dd>Returns a reference to the <code>window</code> object in the frames. See {{domxref("Window.frames")}} for more details.</dd>
</dl>

<h3 id="Properties_implemented_from_elsewhere">Properties implemented from elsewhere</h3>

<dl>
 <dt>{{domxref("WindowOrWorkerGlobalScope.caches")}} {{readOnlyinline}}</dt>
 <dd>Returns the {{domxref("CacheStorage")}} object associated with the current context. This object enables functionality such as storing assets for offline use, and generating custom responses to requests.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.indexedDB")}} {{readonlyInline}}</dt>
 <dd>Provides a mechanism for applications to asynchronously access capabilities of indexed databases; returns an {{domxref("IDBFactory")}} object.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.isSecureContext")}} {{readOnlyinline}}</dt>
 <dd>Returns a boolean indicating whether the current context is secure (<code>true</code>) or not (<code>false</code>).</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.origin")}} {{readOnlyinline}}</dt>
 <dd>Returns the global object's origin, serialized as a string. (This does not yet appear to be implemented in any browser.)</dd>
</dl>

<div class="hidden">
<h3 id="Deprecated_properties">Deprecated properties</h3>

<dl>
 <dt>{{domxref("Window.content")}} and <code>Window._content</code> {{Non-standard_inline}} {{deprecated_inline}} {{ReadOnlyInline}}</dt>
 <dd>Returns a reference to the content element in the current window. Since Firefox 57 (initially Nightly-only), both versions are only available from chrome (privileged) code, and not available to the web anymore.</dd>
 <dt>{{domxref("Window.defaultStatus")}} {{deprecated_inline}}</dt>
 <dd>Gets/sets the status bar text for the given window.</dd>
 <dt>{{domxref("Window.directories")}} {{deprecated_inline}}</dt>
 <dd>Synonym of {{domxref("window.personalbar")}}</dd>
 <dt>{{domxref("Window.globalStorage")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Multiple storage objects that were used for storing data across multiple pages.</dd>
 <dt>{{domxref("Window.mozAnimationStartTime")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>The time in milliseconds since epoch at which the current animation cycle began. Use {{domxref("Animation.startTime")}} instead.</dd>
 <dt>{{domxref("Window.mozPaintCount")}} {{non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Returns the number of times the current document has been rendered to the screen in this window. This can be used to compute rendering performance.</dd>
 <dt>{{domxref("Window.orientation")}} {{readOnlyInline}} {{deprecated_inline}}</dt>
 <dd>Returns the orientation in degrees (in 90 degree increments) of the viewport relative to the device's natural orientation.</dd>
 <dt>{{domxref("Window.pkcs11")}} {{deprecated_inline}}</dt>
 <dd>Formerly provided access to install and remove PKCS11 modules.</dd>
 <dt>{{domxref("Window.returnValue")}} {{deprecated_inline}}</dt>
 <dd>The return value to be returned to the function that called {{domxref("window.showModalDialog()")}} to display the window as a modal dialog.</dd>
</dl>
</div>

<h2 id="메서드">메서드</h2>

<p>{{domxref("EventTarget")}}의 메서드를 상속하고, {{domxref("WindowOrWorkerGlobalScope")}}와 {{domxref("WindowEventHandlers")}} 믹스인의 메서드를 구현합니다.</p>

<dl>
 <dt>{{domxref("Window.alert()")}}</dt>
 <dd>경고 대화 상자를 표시합니다.</dd>
 <dt>{{domxref("Window.blur()")}}</dt>
 <dd>Sets focus away from the window.</dd>
 <dt>{{domxref("Window.cancelAnimationFrame()")}} {{experimental_inline}}</dt>
 <dd>Enables you to cancel a callback previously scheduled with {{domxref("Window.requestAnimationFrame")}}.</dd>
 <dt>{{domxref("Window.cancelIdleCallback()")}} {{experimental_inline}}</dt>
 <dd>Enables you to cancel a callback previously scheduled with {{domxref("Window.requestIdleCallback")}}.</dd>
 <dt>{{domxref("Window.clearImmediate()")}}</dt>
 <dd>Cancels the repeated execution set using <code>setImmediate</code>.</dd>
 <dt>{{domxref("Window.close()")}}</dt>
 <dd>Closes the current window.</dd>
 <dt>{{domxref("Window.confirm()")}}</dt>
 <dd>Displays a dialog with a message that the user needs to respond to.</dd>
 <dt>{{domxref("Window.dispatchEvent()")}}</dt>
 <dd>Used to trigger an event.</dd>
 <dt>{{domxref("Window.dump()")}} {{Non-standard_inline}}</dt>
 <dd>Writes a message to the console.</dd>
 <dt>{{domxref("Window.find()")}}</dt>
 <dd>Searches for a given string in a window.</dd>
 <dt>{{domxref("Window.focus()")}}</dt>
 <dd>Sets focus on the current window.</dd>
 <dt>{{domxref("Window.getComputedStyle()")}}</dt>
 <dd>Gets computed style for the specified element. Computed style indicates the computed values of all CSS properties of the element.</dd>
 <dt>{{domxref("Window.getDefaultComputedStyle()")}} {{Non-standard_inline}}</dt>
 <dd>Gets default computed style for the specified element, ignoring author stylesheets.</dd>
 <dt>{{domxref("Window.getSelection()")}}</dt>
 <dd>Returns the selection object representing the selected item(s).</dd>
 <dt>{{domxref("Window.matchMedia()")}}</dt>
 <dd>Returns a {{domxref("MediaQueryList")}} object representing the specified media query string.</dd>
 <dt>{{domxref("Window.maximize()")}}</dt>
 <dd>{{todo("NeedsContents")}}</dd>
 <dt>{{domxref("Window.minimize()")}} (top-level XUL windows only)</dt>
 <dd>Minimizes the window.</dd>
 <dt>{{domxref("Window.moveBy()")}}</dt>
 <dd>Moves the current window by a specified amount.</dd>
 <dt>{{domxref("Window.moveTo()")}}</dt>
 <dd>Moves the window to the specified coordinates.</dd>
 <dt>{{domxref("Window.open()")}}</dt>
 <dd>Opens a new window.</dd>
 <dt>{{domxref("Window.postMessage()")}}</dt>
 <dd>Provides a secure means for one window to send a string of data to another window, which need not be within the same domain as the first.</dd>
 <dt>{{domxref("Window.print()")}}</dt>
 <dd>Opens the Print Dialog to print the current document.</dd>
 <dt>{{domxref("Window.prompt()")}}</dt>
 <dd>Returns the text entered by the user in a prompt dialog.</dd>
 <dt>{{domxref("Window.requestAnimationFrame()")}}</dt>
 <dd>Tells the browser that an animation is in progress, requesting that the browser schedule a repaint of the window for the next animation frame.</dd>
 <dt>{{domxref("Window.requestIdleCallback()")}} {{experimental_inline}}</dt>
 <dd>Enables the scheduling of tasks during a browser's idle periods.</dd>
 <dt>{{domxref("Window.resizeBy()")}}</dt>
 <dd>Resizes the current window by a certain amount.</dd>
 <dt>{{domxref("Window.resizeTo()")}}</dt>
 <dd>Dynamically resizes window.</dd>
 <dt>{{domxref("Window.scroll()")}}</dt>
 <dd>Scrolls the window to a particular place in the document.</dd>
 <dt>{{domxref("Window.scrollBy()")}}</dt>
 <dd>Scrolls the document in the window by the given amount.</dd>
 <dt>{{domxref("Window.scrollByLines()")}} {{Non-standard_inline}}</dt>
 <dd>Scrolls the document by the given number of lines.</dd>
 <dt>{{domxref("Window.scrollByPages()")}} {{Non-standard_inline}}</dt>
 <dd>Scrolls the current document by the specified number of pages.</dd>
 <dt>{{domxref("Window.scrollTo()")}}</dt>
 <dd>Scrolls to a particular set of coordinates in the document.</dd>
 <dt>{{domxref("Window.setCursor()")}} {{Non-standard_inline}} (top-level XUL windows only)</dt>
 <dd>Changes the cursor for the current window</dd>
 <dt>{{domxref("Window.setImmediate()")}}</dt>
 <dd>Executes a function after the browser has finished other heavy tasks</dd>
 <dt>{{domxref("Window.setResizable()")}} {{Non-standard_inline}}</dt>
 <dd>Toggles a user's ability to resize a window.</dd>
 <dt>{{domxref("Window.sizeToContent()")}} {{Non-standard_inline}}</dt>
 <dd>Sizes the window according to its content.</dd>
 <dt>{{domxref("Window.stop()")}}</dt>
 <dd>This method stops window loading.</dd>
 <dt>{{domxref("Window.updateCommands()")}} {{Non-standard_inline}}</dt>
 <dd>Updates the state of commands of the current chrome window (UI).</dd>
</dl>

<h3 id="Methods_implemented_from_elsewhere">Methods implemented from elsewhere</h3>

<dl>
 <dt>{{domxref("EventTarget.addEventListener()")}}</dt>
 <dd>Register an event handler to a specific event type on the window.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.atob()")}}</dt>
 <dd>Decodes a string of data which has been encoded using base-64 encoding.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.btoa()")}}</dt>
 <dd>Creates a base-64 encoded ASCII string from a string of binary data.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.clearInterval()")}}</dt>
 <dd>Cancels the repeated execution set using {{domxref("WindowOrWorkerGlobalScope.setInterval()")}}.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.clearTimeout()")}}</dt>
 <dd>Cancels the delayed execution set using {{domxref("WindowOrWorkerGlobalScope.setTimeout()")}}.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.createImageBitmap()")}}</dt>
 <dd>Accepts a variety of different image sources, and returns a {{domxref("Promise")}} which resolves to an {{domxref("ImageBitmap")}}. Optionally the source is cropped to the rectangle of pixels originating at <em>(sx, sy)</em> with width sw, and height sh.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.fetch()")}}</dt>
 <dd>Starts the process of fetching a resource from the network.</dd>
 <dt>{{domxref("EventTarget.removeEventListener")}}</dt>
 <dd>Removes an event listener from the window.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.setInterval()")}}</dt>
 <dd>Schedules a function to execute every time a given number of milliseconds elapses.</dd>
 <dt>{{domxref("WindowOrWorkerGlobalScope.setTimeout()")}}</dt>
 <dd>Schedules a function to execute in a given amount of time.</dd>
</dl>

<div class="hidden">
<h3 id="deprecated_methods">deprecated methods</h3>

<dl>
 <dt>{{domxref("Window.back()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Moves back one in the window history. This method is deprecated; you should instead use {{domxref("History.back", "window.history.back()")}}.</dd>
 <dt>{{domxref("Window.captureEvents()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Registers the window to capture all events of the specified type.</dd>
 <dt>{{domxref("Window.forward()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Moves the window one document forward in the history. This method is deprecated; you should instead use {{domxref("History.forward", "window.history.forward()")}}.</dd>
 <dt>{{domxref("Window.getAttention()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Flashes the application icon.</dd>
 <dt>{{domxref("Window.home()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Returns the browser to the home page.</dd>
 <dt>{{domxref("Window.openDialog()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Opens a new dialog window.</dd>
 <dt>{{domxref("Window.releaseEvents()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Releases the window from trapping events of a specific type.</dd>
 <dt>{{domxref("Window.showModalDialog()")}} {{Non-standard_inline}} {{deprecated_inline}}</dt>
 <dd>Displays a modal dialog.</dd>
</dl>
</div>

<h2 id="이벤트_처리기">이벤트 처리기</h2>

<p>These are properties of the window object that can be set to establish event handlers for the various things that can happen in the window that might be of interest.</p>

<p><em>This interface inherits event handlers from the {{domxref("EventTarget")}} interface and implements event handlers from {{domxref("WindowEventHandlers")}}.</em></p>

<dl>
 <dt>{{domxref("Window.onappinstalled")}}</dt>
 <dd>Called when the page is installed as a webapp. See {{event('appinstalled')}} event.</dd>
 <dt>{{domxref("Window.onbeforeinstallprompt")}}</dt>
 <dd>An event handler property dispatched before a user is prompted to save a web site to a home screen on mobile.</dd>
 <dt>{{domxref("Window.ondevicelight")}}</dt>
 <dd>An event handler property for any ambient light levels changes</dd>
 <dt>{{domxref("Window.ondevicemotion")}}</dt>
 <dd>Called if accelerometer detects a change (For mobile devices)</dd>
 <dt>{{domxref("Window.ondeviceorientation")}}</dt>
 <dd>Called when the orientation is changed (For mobile devices)</dd>
 <dt>{{domxref("Window.ondeviceorientationabsolute")}} {{non-standard_inline}}</dt>
 <dd>An event handler property for any device orientation changes.</dd>
 <dt>{{domxref("Window.ondeviceproximity")}}</dt>
 <dd>An event handler property for device proximity event</dd>
 <dt>{{domxref("Window.ongamepadconnected")}}</dt>
 <dd>Represents an event handler that will run when a gamepad is connected (when the {{event('gamepadconnected')}} event fires).</dd>
 <dt>{{domxref("Window.ongamepaddisconnected")}}</dt>
 <dd>Represents an event handler that will run when a gamepad is disconnected (when the {{event('gamepaddisconnected')}} event fires).</dd>
 <dt>{{domxref("Window.onmozbeforepaint")}}</dt>
 <dd>An event handler property for the <code>MozBeforePaint</code> event, which is sent before repainting the window if the event has been requested by a call to the {{domxref("Window.mozRequestAnimationFrame()")}} method.</dd>
 <dt>{{domxref("Window.onpaint")}}</dt>
 <dd>An event handler property for paint events on the window.</dd>
 <dt>{{domxref("Window.onrejectionhandled")}} {{experimental_inline}}</dt>
 <dd>An event handler for handled {{jsxref("Promise")}} rejection events.</dd>
 <dt>{{domxref("Window.onuserproximity")}}</dt>
 <dd>An event handler property for user proximity events.</dd>
 <dt>{{domxref("Window.onvrdisplayconnect")}}</dt>
 <dd>Represents an event handler that will run when a compatible VR device has been connected to the computer (when the {{event("vrdisplayconnected")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplaydisconnect")}}</dt>
 <dd>Represents an event handler that will run when a compatible VR device has been disconnected from the computer (when the {{event("vrdisplaydisconnected")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplayactivate")}}</dt>
 <dd>Represents an event handler that will run when a display is able to be presented to (when the {{event("vrdisplayactivate")}} event fires), for example if an HMD has been moved to bring it out of standby, or woken up by being put on.</dd>
 <dt>{{domxref("Window.onvrdisplaydeactivate")}}</dt>
 <dd>Represents an event handler that will run when a display can no longer be presented to (when the {{event("vrdisplaydeactivate")}} event fires), for example if an HMD has gone into standby or sleep mode due to a period of inactivity.</dd>
 <dt>{{domxref("Window.onvrdisplayblur")}}</dt>
 <dd>Represents an event handler that will run when presentation to a display has been paused for some reason by the browser, OS, or VR hardware (when the {{event("vrdisplayblur")}} event fires) — for example, while the user is interacting with a system menu or browser, to prevent tracking or loss of experience.</dd>
 <dt>{{domxref("Window.onvrdisplayfocus")}}</dt>
 <dd>Represents an event handler that will run when presentation to a display has resumed after being blurred (when the {{event("vrdisplayfocus")}} event fires).</dd>
 <dt>{{domxref("Window.onvrdisplaypresentchange")}}</dt>
 <dd>represents an event handler that will run when the presenting state of a VR device changes — i.e. goes from presenting to not presenting, or vice versa (when the {{event("vrdisplaypresentchange")}} event fires).</dd>
</dl>

<h3 id="Event_handlers_implemented_from_elsewhere">Event handlers implemented from elsewhere</h3>

<dl>
 <dt>{{domxref("GlobalEventHandlers.onabort")}}</dt>
 <dd>Called when the loading of a resource has been aborted, such as by a user canceling the load while it is still in progress</dd>
 <dt>{{domxref("WindowEventHandlers.onafterprint")}}</dt>
 <dd>Called when the print dialog box is closed. See {{event("afterprint")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onbeforeprint")}}</dt>
 <dd>Called when the print dialog box is opened. See {{event("beforeprint")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onbeforeunload")}}</dt>
 <dd>An event handler property for before-unload events on the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onblur")}}</dt>
 <dd>Called after the window loses focus, such as due to a popup.</dd>
 <dt>{{domxref("GlobalEventHandlers.onchange")}}</dt>
 <dd>An event handler property for change events on the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onclick")}}</dt>
 <dd>Called after the ANY mouse button is pressed &amp; released</dd>
 <dt>{{domxref("GlobalEventHandlers.ondblclick")}}</dt>
 <dd>Called when a double click is made with ANY mouse button.</dd>
 <dt>{{domxref("GlobalEventHandlers.onclose")}}</dt>
 <dd>Called after the window is closed</dd>
 <dt>{{domxref("GlobalEventHandlers.oncontextmenu")}}</dt>
 <dd>Called when the RIGHT mouse button is pressed</dd>
 <dt>{{domxref("GlobalEventHandlers.onerror")}}</dt>
 <dd>Called when a resource fails to load OR when an error occurs at runtime. See {{event("error")}} event.</dd>
 <dt>{{domxref("GlobalEventHandlers.onfocus")}}</dt>
 <dd>Called after the window receives or regains focus. See {{event("focus")}} events.</dd>
 <dt>{{domxref("WindowEventHandlers.onhashchange")}}</dt>
 <dd>An event handler property for {{event('hashchange')}} events on the window; called when the part of the URL after the hash mark ("#") changes.</dd>
 <dt>{{domxref("GlobalEventHandlers.oninput")}}</dt>
 <dd>Called when the value of an &lt;input&gt; element changes</dd>
 <dt>{{domxref("GlobalEventHandlers.onkeydown")}}</dt>
 <dd>Called when you begin pressing ANY key. See {{event("keydown")}} event.</dd>
 <dt>{{domxref("GlobalEventHandlers.onkeypress")}}</dt>
 <dd>Called when a key (except Shift, Fn, and CapsLock) is in pressed position. See {{event("keypress")}} event.</dd>
 <dt>{{domxref("GlobalEventHandlers.onkeyup")}}</dt>
 <dd>Called when you finish releasing ANY key. See {{event("keyup")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onlanguagechange")}}</dt>
 <dd>An event handler property for {{event("languagechange")}} events on the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onload")}}</dt>
 <dd>Called after all resources and the DOM are fully loaded. WILL NOT get called when the page is loaded from cache, such as with back button.</dd>
 <dt>{{domxref("WindowEventHandlers.onmessage")}}</dt>
 <dd>Is an {{event("Event_handlers", "event handler")}} representing the code to be called when the {{event("message")}} event is raised.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmousedown")}}</dt>
 <dd>Called when ANY mouse button is pressed.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmousemove")}}</dt>
 <dd>Called continously when the mouse is moved inside the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmouseout")}}</dt>
 <dd>Called when the pointer leaves the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onmouseover")}}</dt>
 <dd>Called when the pointer enters the window</dd>
 <dt>{{domxref("GlobalEventHandlers.onmouseup")}}</dt>
 <dd>Called when ANY mouse button is released</dd>
 <dt>{{domxref("WindowEventHandlers.onoffline")}}</dt>
 <dd>Called when network connection is lost. See {{event("offline")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.ononline")}}</dt>
 <dd>Called when network connection is established. See {{event("online")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onpagehide")}}</dt>
 <dd>Called when the user navigates away from the page, before the onunload event. See {{event("pagehide")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onpageshow")}}</dt>
 <dd>Called after all resources and the DOM are fully loaded. See {{event("pageshow")}} event.</dd>
 <dt>{{domxref("WindowEventHandlers.onpopstate")}}</dt>
 <dd>Called when a back button is pressed.</dd>
 <dt>{{domxref("GlobalEventHandlers.onreset")}}</dt>
 <dd>Called when a form is reset</dd>
 <dt>{{domxref("GlobalEventHandlers.onresize")}}</dt>
 <dd>Called continuously as you are resizing the window.</dd>
 <dt>{{domxref("GlobalEventHandlers.onscroll")}}</dt>
 <dd>Called when the scroll bar is moved via ANY means. If the resource fully fits in the window, then this event cannot be invoked</dd>
 <dt>{{domxref("GlobalEventHandlers.onwheel")}}</dt>
 <dd>Called when the mouse wheel is rotated around any axis</dd>
 <dt>{{domxref("GlobalEventHandlers.onselect")}}</dt>
 <dd>Called after text in an input field is selected</dd>
 <dt>{{domxref("GlobalEventHandlers.onselectionchange")}}</dt>
 <dd>Is an {{event("Event_handlers", "event handler")}} representing the code to be called when the {{event("selectionchange")}} event is raised.</dd>
 <dt>{{domxref("WindowEventHandlers.onstorage")}}</dt>
 <dd>Called when there is a change in session storage or local storage. See {{event("storage")}} event</dd>
 <dt>{{domxref("GlobalEventHandlers.onsubmit")}}</dt>
 <dd>Called when a form is submitted</dd>
 <dt>{{domxref("WindowEventHandlers.onunhandledrejection")}} {{experimental_inline}}</dt>
 <dd>An event handler for unhandled {{jsxref("Promise")}} rejection events.</dd>
 <dt>{{domxref("WindowEventHandlers.onunload")}}</dt>
 <dd>Called when the user navigates away from the page.</dd>
</dl>

<h2 id="이벤트">이벤트</h2>

<p>Listen to these events using <code><a href="/en-US/docs/Web/API/EventTarget/addEventListener">addEventListener()</a></code> or by assigning an event listener to the <code>on<em>eventname</em></code> property of this interface.</p>

<dl>
 <dt>{{domxref("Window/error_event", "error")}}</dt>
 <dd>Fired when when a resource failed to load, or can't be used. For example, if a script has an execution error or an image can't be found or is invalid.<br>
 Also available via the {{domxref("GlobalEventHandlers/onerror", "onerror")}} property.</dd>
 <dt>{{domxref("Window/languagechange_event", "languagechange")}}</dt>
 <dd>Fired at the global scope object when the user's preferred language changes.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/WindowEventHandlers/onlanguagechange">onlanguagechange</a></code> property.</dd>
 <dt>{{domxref("Window/orientationchange_event", "orientationchange")}}</dt>
 <dd>Fired when the orientation of the device has changed.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/onorientationchange">onorientationchange</a></code> property.</dd>
 <dt>{{domxref("Window/devicemotion_event", "devicemotion")}}</dt>
 <dd>Fired at a regular interval, indicating the amount of physical force of acceleration the device is receiving and the rate of rotation, if available.</dd>
 <dt>{{domxref("Window/deviceorientation_event", "deviceorientation")}}</dt>
 <dd>Fired when fresh data is available from the magnetometer orientation sensor about the current orientation of the device as compared to the Earth coordinate frame.</dd>
 <dt>{{domxref("Document/defaultView/resize_event", "resize")}}</dt>
 <dd>Fired when the window has been resized.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onresize">onresize</a></code> property.</dd>
 <dt>{{domxref("Document/defaultView/storage_event", "storage")}}</dt>
 <dd>Fired when a storage area (<code>localStorage</code> or <code>sessionStorage</code>) has been modified in the context of another document.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/WindowEventHandlers/onstorage">onstorage</a></code> property.</dd>
</dl>

<h3 id="Animation_events">Animation events</h3>

<dl>
 <dt>{{domxref("Window/animationcancel_event", "animationcancel")}}</dt>
 <dd>Fired when an animation unexpectedly aborts.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationcancel">onanimationcancel</a></code> property.</dd>
 <dt>{{domxref("Window/animationend_event", "animationend")}}</dt>
 <dd>Fired when an animation has completed normally.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationend">onanimationend</a></code> property.</dd>
 <dt>{{domxref("Window/animationiteration_event", "animationiteration")}}</dt>
 <dd>Fired when an animation iteration has completed.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationiteration">onanimationiteration</a></code> property.</dd>
 <dt>{{domxref("Window/animationstart_event", "animationstart")}}</dt>
 <dd>Fired when an animation starts.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/onanimationstart">onanimationstart</a></code> property.</dd>
</dl>

<h3 id="Clipboard_events">Clipboard events</h3>

<dl>
 <dt>{{domxref("Window/clipboardchange_event", "clipboardchange")}}</dt>
 <dd>Fired when the system clipboard content changes.</dd>
 <dt>{{domxref("Window/copy_event", "copy")}}</dt>
 <dd>Fired when the user initiates a copy action through the browser's user interface.<br>
 Also available via the <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/oncopy"><code>oncopy</code></a> property.</dd>
 <dt>{{domxref("Window/cut_event", "cut")}}</dt>
 <dd>Fired when the user initiates a cut action through the browser's user interface.<br>
 Also available via the <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/oncut"><code>oncut</code></a> property.</dd>
 <dt>{{domxref("Window/paste_event", "paste")}}</dt>
 <dd>Fired when the user initiates a paste action through the browser's user interface.<br>
 Also available via the <a href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/onpaste"><code>onpaste</code></a> property.</dd>
</dl>

<h3 id="Connection_events">Connection events</h3>

<dl>
 <dt>{{domxref("Window/offline_event", "offline")}}</dt>
 <dd>Fired when the browser has lost access to the network and the value of <code>navigator.onLine</code> has switched to <code>false</code>.<br>
 Also available via the {{domxref("WindowEventHandlers.onoffline", "onoffline")}} property.</dd>
 <dt>{{domxref("Window/online_event", "online ")}}<code><a href="/en-US/docs/Web/API/Window/online_event"> </a></code></dt>
 <dd>Fired when the browser has gained access to the network and the value of <code>navigator.onLine</code> has switched to <code>true</code>.<br>
 Also available via the {{domxref("WindowEventHandlers.ononline", "ononline")}} property.</dd>
</dl>

<h3 id="Focus_events">Focus events</h3>

<dl>
 <dt>{{domxref("Window/blur_event", "blur")}}</dt>
 <dd>Fired when an element has lost focus.<br>
 Also available via the <a href="https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onblur"><code>onblur</code></a> property.</dd>
 <dt>{{domxref("Window/focus_event", "focus")}}</dt>
 <dd>Fired when an element has gained focus.<br>
 Also available via the <a href="https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onfocus"><code>onfocus</code></a> property</dd>
</dl>

<h3 id="Gamepad_events">Gamepad events</h3>

<dl>
 <dt>{{domxref("Window/gamepadconnected_event", "gamepadconnected")}}</dt>
 <dd>Fired when the browser detects that a gamepad has been connected or the first time a button/axis of the gamepad is used.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/ongamepadconnected">ongamepadconnected</a></code> property.</dd>
 <dt>{{domxref("Window/gamepaddisconnected_event", "gamepaddisconnected")}}</dt>
 <dd>Fired when the browser detects that a gamepad has been disconnected.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/Window/ongamepaddisconnected">ongamepaddisconnected</a></code> property</dd>
</dl>

<h3 id="History_events">History events</h3>

<dl>
 <dt>{{domxref("Window/hashchange_event", "hashchange")}}</dt>
 <dd>Fired when the fragment identifier of the URL has changed (the part of the URL beginning with and following the <code>#</code> symbol).<br>
 Also available via the <code><a href="/en-US/docs/Web/API/WindowEventHandlers/onhashchange">onhashchange</a></code> property.</dd>
 <dt>{{domxref("Window/pagehide_event", "pagehide")}}</dt>
 <dd>Sent when the browser hides the current document while in the process of switching to displaying in its place a different document from the session's history. This happens, for example, when the user clicks the Back button or when they click the Forward button to move ahead in session history.<br>
 Also available through the <code><a href="/en-US/docs/Mozilla/Tech/XUL/Attribute/onpagehide">onpagehide</a></code> event handler property.</dd>
 <dt>{{domxref("Window/pageshow_event", "pageshow")}}</dt>
 <dd>Sent when the browser makes the document visible due to navigation tasks, including not only when the page is first loaded, but also situations such as the user navigating back to the page after having navigated to another within the same tab.<br>
 Also available using the <code><a href="/en-US/docs/Mozilla/Tech/XUL/Attribute/onpageshow">onpageshow</a></code> event handler property.</dd>
 <dt>{{domxref("Window/popstate_event", "popstate")}}</dt>
 <dd>Fired when the active history entry changes.<br>
 Also available using the <code><a href="/en-US/docs/Web/API/WindowEventHandlers/onpopstate">onpopstate</a></code> event handler property.</dd>
</dl>

<h3 id="Load_unload_events">Load &amp; unload events</h3>

<dl>
 <dt>{{domxref("Window/beforeunload_event", "beforeunload")}}</dt>
 <dd>Fired when the window, the document and its resources are about to be unloaded.<br>
 Also available via the {{domxref("WindowEventHandlers/onbeforeunload", "onbeforeunload")}} property.</dd>
 <dt>{{domxref("Window/DOMContentLoaded_event", "DOMContentLoaded")}}</dt>
 <dd>Fired when the document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading.</dd>
 <dt>{{domxref("Window/load_event", "load")}}</dt>
 <dd>Fired when the whole page has loaded, including all dependent resources such as stylesheets images.<br>
 Also available via the {{domxref("GlobalEventHandlers/onload", "onload")}} property.</dd>
 <dt>{{domxref("Window/unload_event", "unload")}}</dt>
 <dd>Fired when the document or a child resource is being unloaded.<br>
 Also available via the {{domxref("WindowEventHandlers/onunload", "onunload")}} property.</dd>
</dl>

<h3 id="Manifest_events">Manifest events</h3>

<dl>
 <dt>{{domxref("Window/appinstalled_event", "appinstalled")}}</dt>
 <dd>Fired when the browser has successfully installed a page as an application.<br>
 Also available via the {{domxref("Window/onappinstalled", "onappinstalled")}} property.</dd>
 <dt>{{domxref("Window/beforeinstallprompt_event", "beforeinstallprompt")}}</dt>
 <dd>Fired when a user is about to be prompted to install a web application.<br>
 Also available via the {{domxref("Window/onbeforeinstallprompt", "onbeforeinstallprompt")}} property.</dd>
</dl>

<h3 id="Messaging_events">Messaging events</h3>

<dl>
 <dt>{{domxref("Window/message_event", "message")}}</dt>
 <dd>Fired when the window receives a message, for example from a call to {{domxref("Window/postMessage", "Window.postMessage()")}} from another browsing context.<br>
 Also available via the {{domxref("WindowEventHandlers/onmessage", "onmessage")}} property.</dd>
 <dt>{{domxref("Window/messageerror_event", "messageerror")}}</dt>
 <dd>Fired when a <code>Window</code> object receives a message that can't be deserialized.<br>
 Also available via the {{domxref("WindowEventHandlers/onmessageerror", "onmessageerror")}} property.</dd>
</dl>

<h3 id="Print_events">Print events</h3>

<dl>
 <dt>{{domxref("Window/afterprint_event", "afterprint")}}</dt>
 <dd>Fired after the associated document has started printing or the print preview has been closed.<br>
 Also available via the {{domxref("WindowEventHandlers/onafterprint", "onafterprint")}} property.</dd>
 <dt>{{domxref("Window/beforeprint_event", "beforeprint")}}</dt>
 <dd>Fired when the associated document is about to be printed or previewed for printing.<br>
 Also available via the {{domxref("WindowEventHandlers/onbeforeprint", "onbeforeprint")}} property.</dd>
</dl>

<h3 id="Promise_rejection_events">Promise rejection events</h3>

<dl>
 <dt>{{domxref("Window/rejectionhandled_event", "rejectionhandled")}}</dt>
 <dd>Sent every time a JavaScript {{jsxref("Promise")}} is rejected, regardless of whether or not there is a handler in place to catch the rejection.<br>
 Also available through the <code><a href="/en-US/docs/Web/API/WindowEventHandlers/onrejectionhandled">onrejectionhandled</a></code> event handler property.</dd>
 <dt>{{domxref("Window/unhandledrejection_event", "unhandledrejection")}}</dt>
 <dd>Sent when a JavaScript {{jsxref("Promise")}} is rejected but there is no handler in place to catch the rejection.<br>
 Also available using the <code><a href="/en-US/docs/Web/API/WindowEventHandlers/onunhandledrejection">onunhandledrejection</a></code> event handler property.</dd>
</dl>

<h3 id="Transition_events">Transition events</h3>

<dl>
 <dt>{{domxref("Window/transitioncancel_event", "transitioncancel")}}</dt>
 <dd>Fired when a <a href="https://developer.mozilla.org/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> is canceled.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitioncancel">ontransitioncancel</a></code> property.</dd>
 <dt>{{domxref("Window/transitionend_event", "transitionend")}}</dt>
 <dd>Fired when a <a href="https://developer.mozilla.org/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> has completed.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitionend">ontransitionend</a></code> property.</dd>
 <dt>{{domxref("Window/transitionrun_event", "transitionrun")}}</dt>
 <dd>Fired when a <a href="https://developer.mozilla.org/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> is first created.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitionrun">ontransitionrun</a></code> property.</dd>
 <dt>{{domxref("Window/transitionstart_event", "transitionstart")}}</dt>
 <dd>Fired when a <a href="https://developer.mozilla.org/en-US/docs/CSS/Using_CSS_transitions">CSS transition</a> has actually started.<br>
 Also available via the <code><a href="/en-US/docs/Web/API/GlobalEventHandlers/ontransitionstart">ontransitionstart</a></code> property.</dd>
</dl>

<h3 id="WebVR_events">WebVR events</h3>

<dl>
 <dt>{{domxref("Window/vrdisplayactivate_event", "vrdisplayactivate")}}</dt>
 <dd>Fired when a VR display becomes available to be presented to, for example if an HMD has been moved to bring it out of standby, or woken up by being put on.<br>
 Also available via the {{domxref("Window/onvrdisplayactivate", "onvrdisplayactivate")}} property.</dd>
 <dt>{{domxref("Window/vrdisplayblur_event", "vrdisplayblur")}}</dt>
 <dd>Fired when presentation to a VR display has been paused for some reason by the browser, OS, or VR hardware.<br>
 Also available via the {{domxref("Window/onvrdisplayblur", "onvrdisplayblur")}} property.</dd>
 <dt>{{domxref("Window/vrdisplayconnect_event", "vrdisplayconnect")}}</dt>
 <dd>Fired when a compatible VR display is connected to the computer.<br>
 Also available via the {{domxref("Window/onvrdisplayconnect", "onvrdisplayconnect")}} property.</dd>
 <dt>{{domxref("Window/vrdisplaydeactivate_event", "vrdisplaydeactivate")}}</dt>
 <dd>Fired when a VR display can no longer be presented to, for example if an HMD has gone into standby or sleep mode due to a period of inactivity.<br>
 Also available via the {{domxref("Window/onvrdisplaydeactivate", "onvrdisplaydeactivate")}} property.</dd>
 <dt>{{domxref("Window/vrdisplaydisconnect_event", "vrdisplaydisconnect")}}</dt>
 <dd>Fired when a compatible VR display is disconnected from the computer.<br>
 Also available via the {{domxref("Window/onvrdisplaydisconnect", "onvrdisplaydisconnect")}} property.</dd>
 <dt>{{domxref("Window/vrdisplayfocus_event", "vrdisplayfocus")}}</dt>
 <dd>Fired when presentation to a VR display has resumed after being blurred.<br>
 Also available via the {{domxref("Window/onvrdisplayfocus", "onvrdisplayfocus")}} property.</dd>
 <dt>{{domxref("Window/vrdisplaypresentchange_event", "vrdisplaypresentchange")}}</dt>
 <dd>Fired when the presenting state of a VR display changes — i.e. goes from presenting to not presenting, or vice versa.<br>
 Also available via the {{domxref("Window/onvrdisplaypresentchange", "onvrdisplaypresentchange")}} property.</dd>
 <dt>{{domxref("Window/vrdisplaypointerrestricted_event", "vrdisplaypointerrestricted")}}</dt>
 <dd>Fired when the VR display's pointer input is restricted to consumption via a <a href="/en-US/docs/Web/API/Pointer_Lock_API">pointerlocked element</a>.<br>
 Also available via the {{domxref("Window/onvrdisplaypointerrestricted", "onvrdisplaypointerrestricted")}} property.</dd>
 <dt>{{domxref("Window/vrdisplaypointerunrestricted_event", "vrdisplaypointerunrestricted")}}</dt>
 <dd>Fired when the VR display's pointer input is no longer restricted to consumption via a <a href="/en-US/docs/Web/API/Pointer_Lock_API">pointerlocked element</a>.<br>
 Also available via the {{domxref("Window/onvrdisplaypointerunrestricted", "onvrdisplaypointerunrestricted")}} property.</dd>
</dl>

<h2 id="인터페이스">인터페이스</h2>

<p><a href="/ko/docs/Web/API/Document_Object_Model#DOM_인터페이스" title="/en-US/docs/DOM/DOM_Reference">DOM 인터페이스</a>를 참고하세요.</p>

<h2 id="브라우저_호환성">브라우저 호환성</h2>



<p>{{Compat("api.Window")}}</p>