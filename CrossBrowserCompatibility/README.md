# Cross-Browser Compatibility 💻

**The Problem:**

Different browsers (like Chrome, Firefox, Safari, and Internet Explorer) can be pretty picky about how they read HTML, CSS, and JavaScript. 
This can lead to your website looking or working differently depending on the browser. 
For example, a cool feature like Flexbox might work perfectly in modern browsers but could be a total flop in older ones, like Internet Explorer 11.

**Solutions:**

*Modernizr* is a handy JavaScript library that helps you figure out what features a browser supports. Here’s how you might use it

``` html
<script src="https://cdnjs.cloudflare.com/ajax/libs/modernizr/2.8.3/modernizr.min.js"></script>

<script>
if (Modernizr.flexbox) {
  // Code for browsers that support Flexbox
  document.getElementById('flex-container').classList.add('flex-supported');
} else {
  // Fallback for browsers that don't support Flexbox
  document.getElementById('flex-container').classList.add('flex-not-supported');
  // You can add alternative code here, like using floats or grids
}
</script>

```
