Toggling visibility of elements is best done in jQuery like this. It is important to recursively show to avoid children staying invisible.
```js
<script type="text/javascript" src="//ajax.googleapis.com/ajax/libs/jquery/1.3/jquery.min.js"></script>
<script>
  google.load('jquery', '1.3.1');

  function toggleVisibility(id) {
    if($(id).is(":visible")) {
       $(id).hide();
    } else {
       $(id)
       .show()
       .children().show();
    }
  }
</script>
```