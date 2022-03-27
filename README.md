# EsoTalk_InfiniteScroll
Infinite Scroll For Main page

**Open: /core/views/default.master.php**

Add this right after ```<body>``` tag
  
 ```
  <script>
$(function(){ //on document ready
    $(document).scroll(function (e) { //bind scroll event

        var intBottomMargin = 10; //Pixels from bottom when script should trigger

        //if less than intBottomMargin px from bottom
        if ($(window).scrollTop() >= $(document).height() - $(window).height() - intBottomMargin) {
            $(".viewMore").click(); //trigger click
        }

    });
});
</script>
  ```
 ----------------- 

**Open: /core/views/conversations/list.php**

find: line 27
```
<li class='viewMore'>
<a href='<?php
```

Add: **class='viewMore'** to ```<a>```
```
<li class='viewMore'>
<a class='viewMore' href='<?php
```

**Done!**

----------------

For mobile edit: /addons/skins/YOUR_SKIN/views/mobile.master.php

And add same code after ```<body>``` tag:
  
  ```
  <script>
$(function(){ //on document ready
    $(document).scroll(function (e) { //bind scroll event

        var intBottomMargin = 10; //Pixels from bottom when script should trigger

        //if less than intBottomMargin px from bottom
        if ($(window).scrollTop() >= $(document).height() - $(window).height() - intBottomMargin) {
            $(".viewMore").click(); //trigger click
        }

    });
});
</script>
  ``` 

