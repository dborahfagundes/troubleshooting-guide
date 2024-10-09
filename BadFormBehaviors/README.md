


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
