---
title: Frequently used coffeescript
author: ytbryan
layout: page
---
<pre class="lang:default decode:true">$ -&gt;
  console.log("DOM is ready")</pre>

<pre class="lang:default decode:true ">$(".submit").click -&gt;
  console.log("submitted!")</pre>

<pre class="lang:default decode:true">$(".button").on "click", -&gt; console.log("button clicked!")</pre>

<pre class="lang:default decode:true  ">$(document).on "click", ".button2", -&gt;
  console.log("delegated button click!")
</pre>

<pre rel="CoffeeScript" class="language-javascript">$.ajax 
 url: "some.html" 
 dataType: "html" 
 error: (jqXHR, textStatus, errorThrown) -&gt; 
  $('body').append "AJAX Error: #{textStatus}" 
success: (data, textStatus, jqXHR) -&gt; 
  $('body').append "Successful AJAX call: #{data}"</pre>

<pre class="lang:default decode:true">$.ajax 
url: "some.html" 
dataType: "html" 
error: (jqXHR, 
textStatus, errorThrown) -&gt; 
  $('body').append "AJAX Error: #{textStatus}" 
success: (data, textStatus, jqXHR) -&gt; 
  $('body').append "Successful AJAX call: #{data}"

</pre>

<pre class="lang:default decode:true  ">div.animate 
 color: red 2000 -&gt; 
 doSomething()

</pre>

<pre class="lang:default decode:true">div.animate {width: 200}, 2000 
div.animate width: 200 height: 200 2000

</pre>

<pre class="lang:default decode:true">$("input") 
.val("") 
.css 'z-index': 5 
.removeClass "fart"

</pre>

<pre class="lang:default decode:true ">$(".button").click -&gt;
  setTimeout ( =&gt;
    $(@).slideUp()
  ), 500</pre>

&nbsp;

Source: https://css-tricks.com/jquery-coffeescript/