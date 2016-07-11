# Feedify
Feedify is a JQuery plugin inspired by Instagram's "stick to top then drop" effect.
While scrolling your feed, the header remains stuck to top, then is pushed away by the new item.

It comes with a beautiful yet optional theme which is everything you need to build a good-looking, functional feed of whatever you want.

Please visit: <a href="http://demos.sarahdayan.com/feedify" target="_blank">http://demos.sarahdayan.com/feedify</a>

## Features

### Fully responsive

The web is responsive now, there's no turning back.
Feedify goes with the flow.

### Cross-browser

Feedify works on all the most recent browsers,
and degrades gracefully down to IE9.

### Feedify theme

You don't need to be a front-end genius to make pretty things. Feedify comes with an optional theme.

### Flexible

Whatever your coding style is, Feedify respects it. Just add the right classes on your markup to make it work.

## How to use Feedify

### Include JQuery and Feedify

Feedify works with JQuery, so you'll need to add JQuery then Feedify for it to work properly. Be careful if you use multiple JavaScript libraries: Feedify is made to avoid conflicts, but you never know what might happen.

<pre>&lt;script src=&quot;http://code.jquery.com/jquery-latest.min.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;js/feedify.min.js&quot;&gt;&lt;/script&gt;</pre>

### Build your feed

As developers, we like to remain totally free with our code. Some of us will rather keep things awfully simple, while others need extra markup. Some are totally sold with HTML5, while others are hardcorde <code>div</code> users.

Whatever your style is, Feedify got you covered by using classes on key elements.
Just make sure they're all here and you'll be good to go.

Note: Feedify is based on scrolling, so make sure you create enough items so there's something to scroll.

<pre>&lt;div class=&quot;feedify&quot;&gt;
  &lt;div class=&quot;feedify-item&quot;&gt;
   &lt;div class=&quot;feedify-item-header&quot;&gt;
    This is the header of my item.
    It will remain stuck to top while scrolling.
   &lt;/div&gt;
   &lt;div class=&quot;feedify-item-body&quot;&gt;
    This is the body of my item.
    I can put whatever I want in here.
   &lt;/div&gt;
  &lt;/div&gt;
&lt;/div&gt;</pre>

### Add some style

You're free to use the Feedify theme or not, but it still needs a few lines of CSS to work properly. Either include <code>feedify.min.css</code> in your page, or copy-paste the code in your own CSS stylesheet.

<pre>.feedify .feedify-item {
  position: relative;
}
.feedify .feedify-item .feedify-item-header {
  z-index: 100;
}
.feedify .feedify-item.fixed .feedify-item-header {
  position: fixed;
  top: 0;
}
.feedify .feedify-item.bottom .feedify-item-header {
  position: absolute;
  bottom: 0;
}</pre>

### Unleash the beast

Everything is set up, now you just need to pull the trigger. To fire Feedify, just add the following piece of code within a <code>&lt;script&gt;</code> tag in your page (or directly in your script page if you have one) and voilà!

<pre>$(function() {
  $('.feedify').feedify();
});</pre>

### Optional — Offset headers

In the case where the header isn't located at the top of your page, there is an optional parameter that can be used before pulling the trigger

<pre>$(function() {
  $('.feedify').feedify(offset);
});</pre>

Where offset is an integer pixel value, for instance in the case of 100px offset header:

<pre>$(function() {
  $('.feedify').feedify(100);
});</pre>

### Optional — Feedify theme

Feedify theme uses <a href="http://getbootstrap.com/" target="_blank">Bootstrap</a>. You need to make sure you include at least version 3.3.4 of Bootstrap if you intend to use it.

<pre>&lt;link href=&quot;http://maxcdn.bootstrapcdn.com/bootstrap/3.3.4/css/bootstrap.min.css&quot; rel=&quot;stylesheet&quot;&gt;
&lt;link href=&quot;css/feedify.min.css&quot; rel=&quot;stylesheet&quot;&gt;
&lt;link href=&quot;css/feedify-theme.min.css&quot; rel=&quot;stylesheet&quot;&gt;</pre>


## Credits

### Feedify

My name is Sarah Dayan and I'm the one behind Feedify. This project was a way to combine my two passions (<a href="http://resume.sarahdayan.com/" target="_blank">coding</a> and <a href="http://www.sarahdayan.com/" target="_blank">lettering</a>).

### Icons

The beautiful icons used in Feedify theme are part of a free collection called <a href="http://www.kyleadams.me/thinlines/" target="_blank">Thinlines</a>. They were created by my friend and awesome icon designer <a href="http://kyleadams.me/" target="_blank">Kyle Adams</a>.

### Images

The portraits I used are all free to share and licensed under Creative Commons, please visit <a href="http://demos.sarahdayan.com/feedify/#credits" target="_blank">Feedify website</a> for a complete list of their authors. All the other images were taken from <a href="http://unsplash.com/" target="_blank">Unsplash</a>.

